---
layout: default
home: true
---



{% for post in paginator.posts %}

{% assign minutes = post.content | number_of_words | divided_by: 180 %}
{% if minutes == 0 %}
  {% assign read-time = site.var_less_than_a_minute_read %}
{% else %}
  {% assign read-time = minutes | append: "&nbsp;" | append: site.var_min_read %}
{% endif %}

  <article>
    <span class="meta">
      {% if site.display-author-front-page %}
        {% if post.author.name %}
          {{ post.author.name }} •
        {% else %}
          {% if site.author.name %}
            {{ site.author.name }} •
          {% endif %}
        {% endif %}
      {% endif %}
      {{ post.date | date: site.date_format }} • {{ read-time }}</span>
  	<a href="{{ post.url | prepend: site.baseurl }}"><h1>{{ post.title }}</h1></a>
      <p>
      {% if post.summary %}
        {{ post.summary }}&nbsp;<a class="read-more" href="{{ post.url | prepend: site.baseurl }}">{{ site.var_read }}  →</a>
      {% else %}
        {{ post.excerpt | remove: '<p>' | remove: '</p>' }}&nbsp;<a class="read-more" href="{{ post.url | prepend: site.baseurl }}">{{ site.var_read }}  →</a>
      {% endif %}
      </p>

  </article>
{% endfor %}

{% if paginator.previous_page or paginator.next_page %}
  {% include pagination.html %}
{% endif %}
