---
layout: post
title:  "Shortcuts and Helpers"
date:   2014-10-16 15:34:42
categories: jekyll update
---

My goal with this post is to provide you with a few of the best shortcuts to get you to start using some of the capabilities of vim.

I am going to start with traversing the file structure. "cd" .. is great for moving back a file, but generally you are moving back a file to get somewhere else. Did you know that you can put the whole path in one line? I am going to use a project that I am currently working on in class. The project is "jessicafraines.github.io". Here is a small snippet of the file structure that I will be referring to.

    /code/jessicafraines.github.io  
                                  _includes
                                    footer.html
                                    head.html
                                    header.html

                                  _layouts
                                    default.html
                                    page.html
                                    post.html

                                  _sass
                                    _base.scss
                                    _layout.scss


Let's say I am in my _layouts folder, but now I need to be in my _sass folder. It would look something like this:
    
    ~/code/jessicafraines.github.io/_layouts > cd ../_sass

The "cd" is to change the directory, the "../" means to move back one directory, in this case to jessicafraines.github.io and the "_sass" is the folder that I want to be in once it's all said and done.

Now if I am in my _layouts folder, but I want to work in my footer.html file in the _includes folder I would do this:

    ~/code/jessicafraines.github.io/_layouts > mvim ../_includes/footer.html
