---
layout: post
title: "Programming Language    Notes 1"
description: ""
category: Course Notes 
tags: [programming language, haskell]
---
{% include JB/setup %}
*Note that this is just some scattered pieces taken at Programming Language course.*

The course is taught by Prof. Huang, course website is at: [http://acl.cs.qc.edu/~lhuang/teaching/PL/](http://acl.cs.qc.edu/~lhuang/teaching/PL/). At the beginning of class, we are brainwashed that c/c++ is the worst of all the programming languages, java is also bad, Python is best, but we will use Haskell. In another course of Huang, we are brainwashed that all products of Microsoft ( Windows, Office..) are awful, and serious computer scientist should use Mac, or Linux. Unfortunately, I don’t have Mac though always want one.
<!--more-->

Anyway, the course is about viewing programs as mathematical objects and it’s linguistics of programming languages. Programming languages can be categorized as functional and imperative where functional ones have recursion as the primary control structure (note the edge conditions when you program) and heavily use higher-order functions.

Good Haskell tutorial can be found at [http://learnyouahaskell.com/chapters](http://learnyouahaskell.com/chapters). Haskell lists are linked lists, so its random access operation takes linear time. 

An important concept is tail recursion, which is the recursive call appears at and only at the last step in a function call and it’s optimized by compiler to a loop. ( See more at [http://stackoverflow.com/questions/33923/what-is-tail-recursion](http://stackoverflow.com/questions/33923/what-is-tail-recursion))

A piece of code in haskell that I like is quicksort which is very elegant, I would end this post with the code below:

{% highlight haskell %}
qsort [] = []
qsort (p:xs) = qsort left ++ [p] ++ qsort right
    where
        left  = [x|x<-xs, x<p]
        right = [x|x<-xs, x>=p]
{% endhighlight %}

