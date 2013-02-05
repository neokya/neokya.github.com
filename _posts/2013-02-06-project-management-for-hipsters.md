---
layout: post
title: "Project Management for hipsters"
category:
tags: [project-management, team]

meta_description: Using Git and Github to manage projects.
---
This is more about Git, than project management. I am not going to write anything new, and everything I am going to write is basics. But I know we overlook the basics, most of times. In fact, this is about how to use git and git hosting services to manage projects nicely.

I have been using Git as main VCS for quite a long time. Github is always there for code hosting, but I also tried Bitbucket for some time. (FYI, Bitbucket provides five private repositories for free. That is nice.)

For people new to Git, go to [Try Git][0]

All the non-hipsters, read this great post - [A successful Git branching model][1] 

Ok, let's get real.

1. Use imperative commit messages. Initially, I used to write adjetive commit messages, like this `added feature x` and I defended my stand. Yes, it made sense when I was working on some toy project and I used to push on `master` branch. But, when you work with other team members and project gets bigger, the commit doesn't do anyting until it is merged. So, it makes a lot sense to write `add feature x` Also, refer to this [Use the imperative, Luke][2]  

2. Above post on branching is great for active project with a team more than a couple of developers. But for small projects, that level of complexity is not really needed IMO. Keep a `master` banch for production and a `feature` branch for development. And create as many branches as needed. But, always delete the branch after it is merged back to feature branch. Otherwise, it gets too messy.  

3. Use Github issues and milestones extensively. I and my team started to use this since not long, but I can't stress this enough. This is the true way of working, and it's comes for free. I feel these two replaces many paid softwares made for project management. (Yeah, I am pointing out to you, Basecamp)

4. Use `.gitignore` One of the headache is when git tracks unwanted files. There are global and project level use of the feature. If stack is same in project one is working, setting everything in global is fine. Otherwise, use project level setting.  

5. Do code review - pull reqeusts. I think not merging yourself even if you can, and allowing a team member to review pull request is good thing to stick on. Like people say, team work.

Well, that's it. All basics. I told you, this is for hipsters.

[0]: http://try.github.com
[1]: http://sanacl.wordpress.com/2011/03/01/use-the-imperative-luke/
[2]: http://nvie.com/posts/a-successful-git-branching-model/
  