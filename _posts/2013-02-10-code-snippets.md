---
title: Code Snippets
---

Whenever you need to post a code snippet, use the liquid tags `hilight` and `endhilight`.

like this:

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
{% endhighlight %}

You can also add line numbers by setting `linenos`. Like in this example:

{% highlight bash linenos %}
#!/bin/bash

###### CONFIG
ACCEPTED_HOSTS="/root/.hag_accepted.conf"
BE_VERBOSE=false

if [ "$UID" -ne 0 ]
then
 echo "Superuser rights required"
 exit 2
fi

genApacheConf(){
 echo -e "# Host ${HOME_DIR}$1/$2 :"
}
{% endhighlight %}

Note that when you try to copy this code block the line numbers will be copied too.
