---
layout: page
title: Ask Me Anything
permalink: /ama
---
<p></p>
<div class="display-center">
Each week we host an AMA on our Discord with someone with community experience. These AMAs provide you the opportunity to interact with and learn from those with years of experience building, moderating, and growing various types of communities. Below you'll find a list of our upcoming AMAs as well as transcripts from our past events.
</div>
<br>
<h6>Upcoming AMAs</h6>
<p>Stay tuned for upcoming AMA info!</p>
<!--
<div class="upcoming-ama">
  <p><strong>AMA Host Name</strong> - Founder of Community</p>
  <p><i>November 15th at 7pm EST</i></p>
</div>
<div class="upcoming-ama">
  <p><strong>AMA Host Name</strong> - Bot developer of Dyno</p>
  <p><i>November 15th at 7pm EST</i></p>
</div>-->
<p></p>
<h6>Past AMAs</h6>
<div class="post-list" itemscope="" itemtype="http://schema.org/Blog">
  {% for post in site.posts %}
  <div class="ama-post">
    <a href="{{ post.url }}">
      <p><strong>{{ post.guest }}</strong> - {{ post.subtitle }}</p>
    </a>
  </div>
{% endfor %}
</div>