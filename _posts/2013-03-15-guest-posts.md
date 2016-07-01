---
title: Guest Posts

author:
  name: George Michael
  info: (@<a href="https://twitter.com/georgemichael">GeorgeMichael</a>)

summary: If you want to create a guest post that will appear as if written by another author, simply add an <code>author</code> attribute to the front matter of your blog post.
---

If you want to create a guest post that will appear as if written by another author, simply add an `author` attribute to the front matter of your blog post. This will be picked up in the template and displayed in the meta-section both on the front page as well as on the individual post pages.

This post's front matter looks like this:

{% highlight YAML %}
---
title: Guest Posts

author:
  name: George Michael
  info: (@<a href="https://twitter.com/georgemichael">GeorgeMichael</a>)

summary: If you want to create a guest post that will appear as if written by another author, simply add an `author` attribute to the front matter of your blog post.
---
{% endhighlight %}
