---
layout: post
title: "Use of .sort() and Python built-in function sorted()"
category:
tags: [programming, python]

meta_description: Differences in Python .sort() and sorted()
---
Well, the differences between `.sort()` and Python built-in functions `sorted()` are quite simple. But again I felt like putting short note here.

I had a special requirement. Something like I needed to show posts according to date addeded. If it was simple demo blog engine, I would just do it in Django Model using Meta option like this `ordering = ['-pub_date']`. But real world applications are not as easy.

I want to show all stream of latest posts an user is subscribed to sorted by publication date.

So, I get the list of posts an user is subscribed to say `posts`. Now I can sort the posts in two different ways.

1. `posts.sort(key=lambda x: x.pub_date, reverse=True)`
2. `sorted_lists = sorted(posts, key=lambda x: [x.pub_date], reverse=True)`

The above two give exactly same output. Only difference is internal operation. The `sort()` method modifies the same list for economy of space. Whereas, `sorted()` returns a new sorted list from the items in iterable.

In the given case, option one is the way to go as it will be fast.

Also, see this [StackOverlow][1] discussion about the topic.

Thanks to [PD][2] for some help :)

[1]: http://stackoverflow.com/questions/1436962
[2]: https://twitter.com/pdvyas