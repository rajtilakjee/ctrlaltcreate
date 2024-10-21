+++
title = 'Libraries Installed Colab'
date = 2024-10-21T20:34:58+05:30
draft = false
tags = ["python", "colab"]
categories = ["post"]
+++

I was trying to create a notebook for fine-tuning an LLM on Google Colab. However, after every another line I was getting an error that some library or the other was not installed. What did I do? Well, I wrote a quick Python script to check if a set of libraries are already installed on Colab, so that if they are not installed I can install them beforehand.

Here's the Python script to check if a set of libraries are pre-installed on Colab:

```python
libraries = ['numpy', 'pandas', 'matplotlib', 'scikit-learn']  # Add your libraries here

for lib in libraries:
    try:
        __import__(lib)
        print(f"{lib} is installed")
    except ImportError:
        print(f"{lib} is NOT installed")
```

You can go ahead and change the libraries in the `libraries` variable as per your requirement. This saved me a lot of time and headache, hope you find it useful too.