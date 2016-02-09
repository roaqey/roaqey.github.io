---
layout: post
title:  "Interview: Harry Roberts of CSS Wizardry"
date:   2014-01-06 09:00:00
tags: [interview]
---

### Whats the easiest thing a front-end dev can start doing to write better CSS?

Start writing CSS like you’re writing it in a big team and on a big project. A lot of people treat CSS as ‘making a page look like a design’, but this short-sighted view leads to a lot of problems. Start thinking about how and where CSS fits into wider areas such performance, architecture, scalability, maintainability, team working.

The biggest shift I think I made with CSS was approaching it like a software engineer might. Borrow from other schools of thought and see how that can help you.

Too many developers work in their own little bubble, and that leads to poor CSS
CSS is easy, really easy, but it’s just as easy to mess up. I think a lot of the reasons CSS has got a bad name is because it’s not been taken or treated seriously enough. It’s an incredibly easy syntax, which is why I feel people have become more lazy with it, but we need to start thinking about the bigger picture. Instead of stopping coding once something renders properly, stop once you’ve documented, tested, refactored, and improved everything. Make sure it’s stable, robust, performant, and understandable. Too many developers work in their own little bubble, and that leads to poor CSS.

### Seems BEM syntax for naming classes is catching on. Can you expand upon the ideas and benefits?

BEM is great for a number of reasons. I guess its elevator pitch is that it’s an explicit, transparent, meaningful, and descriptive way of naming things in order to make code nicer to work with in larger teams over longer periods.

BEM stands for block, element, and modifier, where a block is the top level of a discrete object, module or component; an element is a constituent part of that block; a modifier is a different variation or state of the block. Each of the three types of thing have a different syntax:

{% highlight scss linenos %}
.a-block {}

.a-block__an-element {}

.a-block--a-modifier {}
{% endhighlight %}

A block is simply a hyphen delimited string; an element is a hyphen delimited string appended to the block, and delimited by two underscores (__); a modifier is a hyphen delimited string appended to the block, and delimited by two hyphens (--). To use an example:

{% highlight scss linenos %}
.search {}

.search__field {}

.search--products {}
{% endhighlight %}

These example classes tell us a lot of things about themselves:

What is it? Straight away we can see that this related to a search block, with a search field and a product search being involved. We can also see that the product search is a variation, or modifier, of an existing search block, and that the search field is a descendant element of the search block (we glean this from the and respectively)

What it does? As a continuation of the above, we can see from the double hyphen/underscore delimiters what each of the bits of code do: one modifies and the other composes.

This prevents developers from using classes in areas they’re not supposed to be used in: a developer would struggle to use a .search--form class on a contact form, for example
Where it should be used. By having a namespace of sorts, we are told where and how we should use the classes. This prevents developers from using classes in areas they’re not supposed to be used in: a developer would struggle to use a .search--form class on a contact form, for example.

How is it related to other things? The namespace also allows developers to see which classes are related to one another, and which ones aren’t. This becomes more obviously useful when you have a section of the DOM with many classes relating to different pieces of functionality; a namespace helps group the common classes.

BEM basically gives developers a much more useful, bulletproof, and manageable way of naming things. I would strongly recommend that everyone tries it out at least once on a project.

### What piece of work of yours are you most proud of?

It’s really hard to say. Really hard. I don’t really get that proud, because it’s just my job, and I could probably always do it better (and I often wish I had). inuitcss is something that I am proud of on the whole—there are certain implementation details that I would like to change, but I think I’ve done a pretty good job of packaging up the OOCSS way of thinking into a framework that people seem to be using quite a lot.

### Any thoughts on SUIT CSS from Nicolas Gallagher?

I love it, I want to move inuitcss to a more dependency managed codebase, and I think SUIT does that really well. I’ve always been a fan of OOCSS, and of Nicolas’ work, so SUIT is a winner in my eyes. There are things in there I would do differently, of course, but that’s an implementation-level concern.

### Lastly, what to do you hope to see in the near future from CSS community?

I’d really like to see people finally stop clinging to misguided notions like ‘semantic classes’ and ‘clean markup’; the web has grown up, our approach needs to grow up too.
