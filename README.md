# Hosting a Resume on GitHub Pages

![](resume.gif)

## Purpose

You will acquire the skills to host a resume online using GitHub Pages and Markdown. Furthermore, you will learn about static-site generators, Git, and why markdown is so darn good.

## Summary

- [Prerequisites](#prerequisites)
- [Instructions](#instructions)
    - [Creating a Repository](#step-1-creating-a-repository)
    - [Cloning a Repository](#step-2-cloning-a-repository)
    - [Adding a Resume to a Repository](#step-3-adding-a-resume-to-a-repository)
    - [Launching the Website](#step-4-launching-the-website)
- [Customization](#customization)
- [More Resources](#more-resources)
- [Authors and Acknowledgements](#authors-and-acknowledgments)
- [FAQ](#faq)

## Prerequisites

- A resume formatted in markdown

- A GitHub account

- Some command line experience

## Instructions

The following steps are based on the GitHub Pages [website](https://pages.github.com/).

If you run into issues, refer to the [FAQ](#faq).

### Step 1. Creating a Repository

Creating a repository will take place on the GitHub landing page, _after_ you have logged in.

1. Press the green **New** button.
2. Make the **Repository name**, `username.github.io`
    - Ensure `username` is your GitHub username.
3. Ensure **Public** is checked
4. Click the green **Create repository** button.

### Step 2. Cloning a Repository
 
1. In a command line, run the following:
    ```
    git clone https://github.com/username/username.github.io
    ```
    * This will copy the online repository to your local files.
    * The command line is a quicker way to execute tasks that would take a long time  with a GUI.

The reason Git is used is because it's a powerful tool used for distributed version-control. In brief, this means that files can be hosted and maintained in an online repository like GitHub. Furthermore, Git tracks previous versions of those files and catalogs the differences. Andrew Etter says that version control is "one of the most important functions of a technical writer" and Git will do all version control behind the scenes for you. Etter adds that Git has a legitimate appeal as "documentation and code branches [can] stay in sync" and that "developers are more likely to contribute". All in all, Git makes it easy for many people to work on the same project while keeping track of past versions. 

### Step 3. Adding a Resume to a Repository
 
1. Create an `index.md` file in the local repository.
    * **This file is your resume formatted in markdown.**
    <br/>

2. Push `index.md` to your GitHub repository

    * In a command line, run the following:
    ```
    git add *
    git commit -m "Added index.md"
    git push -u origin master
    ```

Your resume should be named `index.md`. This _exact_ name is important.

Markdown is one of many lightweight markup languages. By far, Markdown is the most used lightweight markup language as it is simple, human-readable, and free. Etter favours Markdown over XML for these reasons. Moreover, Markdown and other lightweight markup languages are easy ways to get content on a webpage. Most lightweight markup languages can be easily converted to HTML, which is subsequently used by web technologies to render the content. In terms of this guide, coordination between a static-site generator and a Markdown file can easily create a website hosting a resume. Additionally, using these tools with Git allows for Markdown files to be easily managed, versioned, and tracked.

### Step 4. Launching the Website

1. In a browser, go to `https://username.github.io`.
    * Again, `username` is your GitHub username.

As Etter says, building a website like the one in this README is an easy way of distributing a variety of information. Furthermore, static websites provide fast and simple ways to get started as they require minimal overhead and have low coupling to other web technologies. Moreover, static websites provide a base level of setup, just enough for a website to look good. Static websites also make documents readily available. Instead of emailing PDFs or using snail mail to get documents to the users, static websites make documents easily accessible to anybody, anywhere, all the time.

## Customization

GitHub Pages comes with some built-in Jekyll templates to change the style and layout of your site. To do this:

1. In your repository, click the **Settings** button

2. Scrolling down, find the **GitHub Pages** section

3. Click the **Change theme** button

4. Choose a theme from the list

5. Press the green **Select theme** button

These steps can be seen in the gif below. It may take a few minutes for the theme changes to appear.

![](customize.gif)

Customizing your GitHub Pages site can be simple or become incredibly complex. The reason being is that GitHub Pages uses Jekyll, a tool used to create static websites. How your site looks can be changed by using Jekyll, but alas, that won't be covered here. If you want to know more, check out the Jekyll tutorial in [More Resources](#more-resources).

## More Resources

- [Andrew Etter's _Modern Technical Writing: An Introduction to Software Documentation_](https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS)
- [Markdown tutorial](https://www.markdowntutorial.com/)

- [Jekyll tutorial](https://jekyllrb.com/tutorials/video-walkthroughs/)
## Authors and Acknowledgments

* This project uses the [Cayman Jekyll theme](https://github.com/pages-themes/cayman).

* Discussions in the README are bolstered by the book, _Modern Technical Writing_ by Andrew Etter.

* Thanks to Adam Azarov, Tommy Wu, and Mostafa Kamal for providing feedback.

## FAQ

_Why is Markdown better than a word processor?_
- Markdown is better than word processors at making fast and legible documents. Markdown files are flexible that can be easily converted to other widely used file types including: XML, HTML, and JSON. Moreover, these file types can be easily rendered by websites without the required overhead when using DOCX or PDF file types.

_Why is my resume not showing up?_
- It can be a few things:
    - The filename of your resume must be either `index.md` or `README.md`. GitHub Pages prioritizes displaying `index.md`. If you want a README, your resume should be named `index.md`.
    - Ensure the GitHub Pages site is being built from the correct source branch on GitHub. This option can be found in the **GitHub Pages** section of your repository settings.

_Why am I using Git for this?_

- Yes, this is only a static page. Instead, a file could be updated on the website and that's that. However, as outlined in Etter's book, using Git to manage files has many benefits. It allows for offline work and enables teams to concurrently work on the same project. In terms of documentation, Etter says that technical writers should use Git because developers generally like it more than other methods.

_What are the benefits of static websites over traditional websites?_

- Traditional websites built using Angular, React, or any other web language, require a certain level expertise. Also, there may be databases, a server, or dependencies required. In comparison, static websites are a breeze. There are a variety of tutorials online, but static websites typically deal with the entire setup process. The user only needs to add files or modify existing files to change the content. With traditional web technologies, developers would need to create _everything_, which is a waste of time when a static website will do the job.
