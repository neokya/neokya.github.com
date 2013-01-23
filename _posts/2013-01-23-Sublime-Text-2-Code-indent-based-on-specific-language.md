---
layout: post
title: "Sublime Text 2 - Language specific code indentation"
category:
tags: [Programming, Editors]

meta_description: Code indentation on Sublime Text 2.
---

There are many reasons why I use Sublime Text 2. I love it. I was trying different text editors sometime last year or so. I didn't really like Emacs. The other great editor Vi or Vim, I somehow liked it. Thing I didn't use it is because it has too much customization. Also, I have really bad memory. I mean my mind memory. And remembering all those commands, especially when I take break from using these tools for quite a long, is not really ideal, IMO. 

Well, these might not be the real reason that I don't use Vim. But, one thing I am sure is that I like things simple. I hate too much customization.

So, Sublime is editor for me. I haven't customized it much. However, I faced a specific problem today. I am Python/Django developer, which means I am forced to use tab size 4. That's alright for all the `Python` code. But, a project contains many file types, along with HTML and Javascript. My template files looked horrible in tab size 4. I like cleanly indenting the code, but tab size 4 makes template code to go out of space. 

So, all I needed was tab size 4 for Python and tab size 2 for everything else. This is how it can be done.

1. Change default setting to tab size 2, which should look like this. Sublime setting is just JSON file.   
 `{
    "tab_size": 2,  
    "translate_tabs_to_spaces": true
}`
2. Change/create file `Python.sublime-settings` inside your User directory. 
`{
    "tab_size": 4,
    "translate_tabs_to_spaces": true
}`  
Location of the file varies according to OS.

That's it. Back to awesomeness ;)
  