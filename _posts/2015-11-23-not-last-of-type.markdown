---
layout: post
title: Not Last of Type
date: 2015-11-23 17:16
tags: [css, tip]
---
I always enjoy finding little ways to simplify writing CSS whenever possible. One common pattern when creating an inline navigation is to have spacing between the navigation items.

The basic code is usually written out below. Add the spacing to all items and then remove it from the last item using the `last-of-type` selector:

{% highlight scss linenos %}
.nav {

    a {
        margin-right: 1rem;

        &:last-of-type {
            margin-right: 0;
        }
    }
}
{% endhighlight %}

One way to get around having to specify a `margin-right` declaration for all navigation items is to add that `margin-right` to every item *except* the last item in one declaration. You can achieve this with the code below:

{% highlight scss linenos %}
.nav {

    a:not(:last-of-type) {
        margin-right: 1rem;
    }
}
{% endhighlight %}
