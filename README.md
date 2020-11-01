# Hosting a Resume on GitHub Pages

## Audience (TAKE OUT TAKE OUT)

Audience: CS Student
Venue: README in GitHub Pages
Prupose: Explain how to host a resume on GitHub Pages
Additional purpose: Introduce and demo principles of Andrew Etter's book _Modern Technical Writing_
Desired Reaction:
Vocabulary:
Tone:

## Purpose

The purpose of this README is to describe and outline some methods that one can take to host their resume online. Over the course of the README you will learn about static-site generators, what makes good documentation, and why markdown is so darn good. Andrew Etter's book _Modern Technical Communication_ will prove as this guides "bible". 

## Summary

- [Setup](#setup)
- [Customization](#customization)
- [More Resources](#more-resources)
- [Authors and Acknowledgements](#authors-and-acknowledgments)
- [FAQ](#faq)

## Prerequisites

- A resume formatted in markdown

- A GitHub account

- Basic knowledge of GitHub

- Basic command line navigation

## Setup

The following steps are based on the steps provided at the [GitHub Pages website](https://pages.github.com/).

These steps assume that you're creating a brand new repository.

1. Create a public repository on GitHub.

    * Name your repository `username.github.io` where "username" is your actual GitHub username. For example, my repository is called `justinband.github.io`.

    * You may ask, "Why use git?". The reason we use Git is because it's a powerful tool used for distributed version-control. This means that you can host and maintain files on an online repository (in our case this is on GitHub) and be able to see previous versions of those files. Git allows many people to work on the same project at once.
    <br/>

2. Using a command line, clone the repository. 

    ```
    git clone https://github.com/username/username.github.io
    ```

    * The command line is an easy way to perform tasks that would take longer with a GUI.

3. Create an `index.md` file.
    
    * `index.md` will be your resume formatted in markdown. _This name is important._ This `index.md` file is what GitHub Pages will render to the static-site.

    * Create this file in your local copy of the repository.

    * Why are we using markdown? 
    <br/>

4. Get `index.md` into your GitHub repository

    * Git commands will commit, and then push your file into your online GitHub repository.

    * In a command line, navigate to your local repository.

    * Next, run the following commands.
    ```
    git add *
    git commit -m "Added index.md"
    git push -u origin master
    ```

5. In a browser, go to `https://username.github.io`.

After following these steps your resume will be hosted on GitHub Pages. If you run into issues please refer to the [FAQ](#faq)

## Customization

Customizing your GitHub Pages site can be simple or become incredibly complex. The reason being is that GitHub Pages uses Jekyll, a tool used to create static websites. How your site looks can be changed by using Jekyll, but alas, I won't cover that here. If you want to know more I recommend checking out the Jekyll tutorial in the [more resources section](#more-resources).

However, GitHub Pages comes with some built-in Jekyll templates to change the style and layout of your site. To do this:

1. Go to the repository settings

2. Scrolling down, find the **GitHub Pages** section and click **Change theme**

3. Choose a theme from the list and then press **Select theme**

It may take a few minutes for your site to change themes.

![](customize.gif)

After following these steps you will notice that a `_config.yml` file is added to your repository. This is a file used by Jekyll to define which theme should be used.

## More Resources

- There are a variety of markdown tutorials online, however, I recommend this [one](https://www.markdowntutorial.com/)

- [Andrew Etter's _Modern Technical Writing: An Introduction to Software Documentation_](https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS)

- [Jekyll tutorial](https://jekyllrb.com/tutorials/video-walkthroughs/)
## Authors and Acknowledgments

## FAQ

_Why is Markdown better than a word processor?_
- Markdown is better than word processors at making fast and legible documents. Markdown files are flexible that can be easily converted to other widely used filetypes including: XML, HTML, and JSON. Moreover, these filetypes can be easily rendered by websites without the required overhead when using DOCX or PDF filetypes.

_Why is my resume not showing up?_
- It can be a few things:
    - Ensure that the filename of your resume is `index.md` or `README.md`. GitHub Pages prioritizes displaying `index.md` (`index.html` works too) so if you want a README your resume should be `index.md`.
    - Ensure that the source for your GitHub Pages site is being built from the correct branch. This option can be found in the **GitHub Pages** section of your repository settings.Change the name of your resume to `index.md`. If preferred, `index.html` will also work.

_Why am I using Git for this?_

- Yes, I know, it's only a static page. A file could be uploaded and that's that. However, as outlined in Etter's book, Git has quickly become the standard version-control tool for software and documentation management. Git brings many benefits. In terms of documentation, Git reduces reliance on the traditional documentation approach and can allow the users themselves can make changes to the documentation (assuming the Git repository is public). All in all, Git usage is good practice.