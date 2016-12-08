---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: default
---

<nav id='sidebar'>
  {% include nav.html %}
</nav>

<section id='content'>
  {% for post in site.posts %}
  <article class='{{ post.type }}'>
    <a name='{{ post.url }}' href='#{{ post.url }}'><h2>{% if post.type %}<code><b>{{ post.type }}</b> {{ post.path }}</code> {% endif %}{{ post.title }}</h2></a>
    <section class='body'>
      {{ post.content }}
    </section>
  </article>
  {% endfor %}
</section>
