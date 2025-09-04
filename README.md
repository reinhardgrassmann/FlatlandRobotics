# README.md


This README.md file is written in [Markdown](https://www.markdownguide.org/getting-started/).
The purpose of this readme file is to have a brief recap in order to re-setup this project. 

The current Status of the [FlatlandRobotics](https://reinhardgrassmann.github.io/FlatlandRobotics/) page is

[![pages-build-deployment](https://github.com/reinhardgrassmann/FlatlandRobotics/actions/workflows/pages/pages-build-deployment/badge.svg)](https://github.com/reinhardgrassmann/FlatlandRobotics/actions/workflows/pages/pages-build-deployment)
[![Deploy Hugo site to Pages](https://github.com/reinhardgrassmann/FlatlandRobotics/actions/workflows/hugo.yml/badge.svg)](https://github.com/reinhardgrassmann/FlatlandRobotics/actions/workflows/hugo.yml)

(See: Short tutorial on how to [add a workflow status badge](https://docs.github.com/en/actions/how-tos/monitor-workflows/add-a-status-badge))

## Prerequisites

I assume you use a Linux machine. 
More specific, Ubuntu or [Pop!_OS](https://system76.com/pop/) is the distribution.
Before you begin working on the website you must install several packages and libraries.

### Packages
You should have the following packages installed in your system

- [npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)
- [snap](https://snapcraft.io/docs/installing-snap-on-ubuntu) (Note that its package name is slightly different)
- [git](https://git-scm.com/downloads/linux)


Before starting to install packages with `apt` let's update it.


````
sudo apt update
````

Install any of the missing packages.


````
sudo apt install npm
````


````
sudo apt install snapd
````

````
sudo apt install git
````


### Hugo and dependencies 

In this part, hugo specific stuff are mentioned.
You need [Go](https://go.dev/doc/install), [Dart Sass](https://gohugo.io/functions/css/sass/#dart-sass), and [Hugo](https://gohugo.io/installation/linux/).

For the language Go, download the latest go version, e.g., [go 1.25 for linux](https://go.dev/dl/go1.25.1.linux-amd64.tar.gz).
Removing previous version of Go and unzip the file via

````
 rm -rf /usr/local/go && tar -C /usr/local -xzf go1.25.1.linux-amd64.tar.gz
````

Afterward, add the PATH to the environment via

````
export PATH=$PATH:/usr/local/go/bin
````

Detail instruction are given on [their webpage](https://go.dev/doc/install).


Finally, hugo...

````
sudo snap install hugo
````

Note if you install Hugo as a Snap package there is no need to install Dart Sass. 
The Hugo Snap package includes Dart Sass.
For completeness, it is `sudo snap install dart-sass`.

It's not over yet.
We also need to install [PostCSS](https://www.npmjs.com/package/postcss).
To install PostCSS, you typically use a package manager like npm or yarn in a Node.js project.

````
npm install --save-dev postcss postcss-cli
````

(You might want to run this in the root folder after downloading this repro.)


## Repro of Flatland Robotics
Let's download this git repro.

Choice a suitable folder and clone this repro.
````
https://github.com/reinhardgrassmann/FlatlandRobotics.git
````

Since we are using the [TeXtify-3](https://themes.gohugo.io/themes/hugo-texify3/) as hugo theme and git submodule, we make sure it's properly initialized.
Execute the following code in the root folder.
````
git submodule update --init --recursive
````

We are ready to run hugo on the machine.
````
hugo server
````

The output should look like

````
                  │ EN  
──────────────────┼─────
 Pages            │  18 
 Paginator pages  │   0 
 Non-page files   │   0 
 Static files     │ 158 
 Processed images │   0 
 Aliases          │   0 
 Cleaned          │   0 

Built in 1320 ms
Environment: "development"
Serving pages from disk
Running in Fast Render Mode. For full rebuilds on change: hugo server --disableFastRender
Web Server is available at http://localhost:1313/FlatlandRobotics/ (bind address 127.0.0.1) 
Press Ctrl+C to stop
````

You might get a link like http://localhost:1313/FlatlandRobotics/ or a similar one with a different number combination.
Now you can click on the link or copy it and paste it in your favourite browser.
