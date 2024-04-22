---
author: "Yiyi"
date: 2022-09-06
title: "Github Page build Personal Website"
tags: [
 
]
categories: [notes

]
---

GitHub Pages is a static site hosting service that hosts a person, organization, or project's pages directly in a GitHub repository or repository.
Hugo is a static site generator written in Go that is optimized for speed, ease of use, and configurability. It's fast and flexible

## error I met

*error: Push some references to 'github.com: '*
solution: 
    git commit -m ""

*error: You've added another git repository inside your current repository.*
solution:  
    git rm -r --cached log  //Delete the track for log
    git submodule add url //Add log to the subdirectory
    git submodule add --depth=1 https://github.com/xianmin/hugo-theme-jane.git themes/jane   --depth 

*error: build and deploy all jobs have failed*
solution: 
    hugo -d docs
    Then select docs in the Settings section of the repository.
    This approach has the advantage of separating the source files from the compiled files.

*fatal: unable to access "...github"*
solution: 
    Use SSH, not HTTP.
    Also note if SSH is already connected to another account.If so, remove it.

*TOCSS: failed to transform "/sass/jane.scss" (text/x-scss). Check your Hugo installation; you need the extended version to build SCSS/SASS with transpiler set to 'libsass'.: this feature is not available in your current Hugo version, see https://goo.gl/YMrWcn for more information *
solution: 
    brew install //the right one
    conda install
    pip install
    There are three methods to download source on MacOS so we need to figure out 
    the right version.

## Other command
git command
    
    git remote -v //remote repo
    git init //initiate repo
    git clean
    git add .
    git commit -m "doc"
    git push origin master

hugo command

    hugo new site site_name

directory structure
personal-site

├── archetypes

├── config.toml   //Hugo configuration doc

├── content       //store the Markdown journals

├── data

├── layouts

├── static

└── themes        //themes downloads

compiler the website
    hugo -d 
    hugo -d docs //new version of hugo 0.125.2
Will generate the web file in /docs

