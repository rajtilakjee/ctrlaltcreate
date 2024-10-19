+++
title = 'Install Papermod Hugo Theme'
date = 2024-10-19T13:45:58+05:30
draft = false
tags = ["hugo", "papermod", "theme"]
categories = ["post"]
+++

The Hugo Papermod theme is a lightweight, minimalist theme suitable for blogs and portfolios. It's the same theme that I have used in this blog. The Papermod theme is based on the Hugo Paper theme and can be found [here](https://github.com/adityatelange/hugo-PaperMod).

However, when I tried installing it following the instructions given in their official wiki, the theme didn't install properly. I had to go back and forth between the [Hugo documentation](https://gohugo.io/documentation/) and the Papermod wiki to successfully install the theme. So I thought it's best to document the steps here, just in case someone else or I myself need to refer to it in future.

# Steps for installing Hugo Papermod theme

1. Install Hugo and Git on your system
2. Use the following command to create a new Hugo site: `hugo new site MyHugoWebsite --format yaml`. You need to replace `MyHugoWebsite` with the name of your site. This will create a new folder with the same name with all the required files for the site inside this folder
3. Now change the directory to that of your site: `cd MyHugoWebsite`
4. Initialize Git for your site: `git init`
5. Clone the Papermod theme into the `themes` directory, adding it to your project as a Git submodule: `git submodule add https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod`
6. Locate `hugo.yaml` file in the root of your project and add the following line to it: `theme = 'PaperMod'`. This will ensure that your site uses the Papermod theme
7. Now you can use the [sample configuration](https://github.com/adityatelange/hugo-PaperMod/wiki/Installation#sample-configyml) given in the Papermod wiki to configure your site
8. Once done, you can either host your site on [GitHub pages](https://gohugo.io/hosting-and-deployment/hosting-on-github/) or on [Netlify](https://gohugo.io/hosting-and-deployment/hosting-on-netlify/) like I did. Both are free, however, Netlify comes with a few bells and whistles

Hope this helps in setting up your site using Hugo Papermod theme.