---
layout: post
title:      " .each, .map, .collect, .WHAT??"
date:       2019-11-13 23:03:25 +0000
permalink:  each_map_collect_what
---


Well, i learned a thing today!  Sooooo, while i was going through my first project assessment, I came to the conclusion that I wasn't very good in my explainations of some of the Ruby terminology. Well, this needed to change.  I stumbled over myself with .each.  So after some good old fashion Googling, i now have a good understanding of .each, .map, and .collect!  These are all methods on objects. AND to my surprise, .map and .collect are the same thing! 

*.Each example:*

numbers = [1,2,3]
numbers.each { |num| num * 2 }
 => [1, 2, 3]


*.Map/.Collect example:*

numbers = [1,2,3]
numbers.map { |num| num * 2 }
=> [2, 4, 6]

.Each is like a loop, it returns the original array.

.Map/.Collect return an array of values returned by the block.  It creates a new array as the return value after performing the block on each item!

If i can now understand how to explain this, i'm sure you can too!
