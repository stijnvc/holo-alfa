---
title: Code Snippets



---

Whenever you need to post a code snippet, use the liquid tags `hilight` and `endhilight` like this:

{% highlight css %}
nav a:hover {
  color: rgba(0,0,0,.72);
}
nav a.current {
  color: rgba(0, 0, 0, .72)
}
.subtitle {
  margin: 30px 0;
}


/* Structure overwrites */

@media all and (min-width: 370px) {
  .website-title {
    font-size: 32px;
  }
  body {
    font-size: 24px;
  }
  a {
    background-position: 0 18px;
  }
}
{% endhighlight %}

Note that this only provides color-coding. For that you might need to use a front end colorization engine like Highlight.JS or something similar.
