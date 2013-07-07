---
layout: post
title: "Please don't use my package"
category:
tags: [Django, Open Source]

meta_description: Asynchronous thumbnail in django with celery
---
I registered my fist ever package in Python Package Index. And this is I guess first open source code I wrote (I have sent few patches here and there in past though) apart form some sample apps obviously. But I am telling people not to use it.

Ok, here is short background. It's about small thumbnailing app in django. There is one app which I have used in past, [sorl-thumbnail]. It is good piece of software which does the job. But in some cases it doesn't. In my case, we have media heavy project and we use AWS S3 to store images. sorl-thumbnail is very slow here cause it starts to thumbnail at the time when user requests page.

So, we decided to fork sorl-thumbnail to make it work for us. Basically what we decided is,

1. Pregenerate thumbnail while image is uploaded via worker process with celery.
2. Define all the thumbnail options in settings insted of passing it in templates.
3. Cache it and serve the cahed thumbnail.

So, I forked it accordingly and it works. But since original sorl-thumbnail design is different, I had to make hacks to make it work.

So far so good. I added separate app in our django project called thumbnail. I didn't find any work/package to address above issues, so thought of putting it in PyPi or github so that other people might find it useful.

After doing so, I went to #django IRC channel just to give shoutout. The first reply I got was 'Have you tried easy_thumbnails?'. I was like, hey it doesn't solve above issues right?

Then I got another reply from Chris Beaven, creator of 'easy_thumbnails' saying 'I think I know a app which does exactly same'. Then I head over to github '[easy_thumbnails]' and it's exactly what I want. I also came to know sorl-thumbnail is not maintained anymore. See the pull requests, they are there since one year without review. Maintainer doesn't seem to be active anymore.

I did some research before spending hours hacking wrong package. Somehow I missed the solution that was alredy there. Thanks IRC and the community. Please use 'easy_thumbnails'. And please don't use my package.

In case if still you want to see the repo, it's here '[sorl-thumbnail-async]'. 

[sorl-thumbnail]: https://github.com/sorl/sorl-thumbnail
[easy_thumbnails]: https://github.com/SmileyChris/easy-thumbnails
[sorl-thumbnail-async]: https://github.com/neokya/sorl-thumbnail-async 

 
  