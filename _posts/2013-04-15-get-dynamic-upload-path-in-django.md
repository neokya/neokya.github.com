---
layout: post
title: "Get Dynamic Upload Path in Django"
category:
tags: [Django, Notes]

meta_description: Dynamic upload path in django
---
Hard coding sucks. Being as dynamic as possible is only way. 

One of the thing not to hard code in Django is 'upload path' for files. I posted a gist which I used in one project. 

<script src="https://gist.github.com/neokya/5370749.js"></script>

This doesn't only give dynamic url, it slugifies (which is useful in url), and preserves the extension while doing so.

To quote django docs for `slugify()`

>Converts to lowercase, removes non-word characters (alphanumerics and underscores) and converts spaces to hyphens. Also strips leading and trailing whitespace.

So, basically it if a file named 'ââ The 24.doc' is uploaded, it will give dynamic url which will look something like this 'documents/01/aa-the-24.doc'.

Notice the character â, it will break the url if used, so we need to change it to something else, in above case nicely slugified ASCII characters.

Note:
>Any characters in your URL other than A-Z, a-z, 0-9, and /.=?-+%&* (and the : in "http:") should probably be URL encoded.

For details, [read more][1]

[1]: http://meta.stackoverflow.com/questions/21147/non-ascii-characters-in-external-links  

 
  