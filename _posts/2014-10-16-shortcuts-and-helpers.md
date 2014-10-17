---
layout: post
title:  "Shortcuts and Helpers"
date:   2014-10-16 15:34:42
categories: jekyll update
---

My goal with this post is to provide you with a few shortcuts that will help you navigate through vim more efficiently.

I am going to start with traversing the file structure. "cd .." is great for moving back a file, but generally you are moving back a file to get somewhere else. Did you know that you can put the whole path in one line? I am going to use a project that I am currently working on in class. The project is "jessicafraines.github.io". Here is a small snippet of the file structure that I will be referring to.

    ~/code/jessicafraines.github.io  
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

The command begins after the ">" symbol. The "cd" is to change the directory, the "../" means to move back one directory, in this case to jessicafraines.github.io and the "_sass" is the folder that I want to be in once it's all said and done.

Now if I am in my _layouts folder, but I want to work in my footer.html file in the _includes folder I would do this:

    ~/code/jessicafraines.github.io/_layouts > mvim ../_includes/footer.html (in this example I am using MacVim, that is where the "mvim" comes from.)

On the same note, once you are in your text editor Vim you can utilize these same shortcuts. For example:

    :e _includes/footer.html

  or

    :split ../_layouts/default.html

  or
    
    :tabe ../_includes/header.html

In the first example you are in the root directory and want to open footer.html that lives in the _includes folder.

In the second example you are already in a file and want to split the window so your current file and the _layouts/default.html file will be in seperate panes in the same window. You are moving back one directory, then into _layouts and then into default.html.

The third example opens a new tab in the same screen. The new file was one directory back. This is very helpful so you don't have a bunch of windows open. 

This might not seem so important right now, but as our projects become more complex and we have files, inside of folders, inside of other folders this will be handy.

The following list is a few of the shortcuts used while editing a file that will save you time and get you used to keeping your fingers on the keyboard - like a real live programmer. I know these are available in the tutorial, but since they are the most used, I thought they would be worth mentioning. 

Make sure to hit **esc** before using any of these shortcuts.

    x - delete one letter

    dt" - delete every letter until it reaches an apostrophe (replace the apostrophe with whatever character you want to delete up to)

    dd - delete one line

    3dd - delete three lines

    yy - copy one line

    2yy - copy two lines

    p - paste in the line you copied below the line your cursor is on

    5p - paste the copied line five times below the line your cursor is on

    r - replace one letter

    cw - change one word

    3cw - change three words

    :gg=G - corrects indention errors (this applys to JavaScript files only)

    5(shift key)>> - indents the five lines below your cursor

    5(shift key)<< - outdents the five lines below your cursor
        
    . - repeats the previous command - very helpful with multiple indents or outdents

    :set paste i - use when pasting code from an external source into JavaScript file

    :set nopaste - when you are done pasting (if you don't do this, your indents will be messed up)

That is all I can think of right now. As we go along I will try to update this blog so check back regularly if you are looking for a new shortcut. 


