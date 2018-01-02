---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: home
---
# Articles
  {% for post in site.posts %}
<div class="card" style="width: 18rem;">
  <div class="card-body">
    <h5 class="card-title">{{ post.title }}</h5>
    <h6 class="card-subtitle mb-2 text-muted">{{ post.date | date: "%Y-%m-%d" }}</h6>
    <p class="card-text">{{ post.excerpt }}</p>
    <a href="{{ post.url }}" class="btn btn-primary">Read more</a>
  </div>
</div>  
  {% endfor %}
