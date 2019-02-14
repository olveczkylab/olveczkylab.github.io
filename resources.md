---
title: Reference
permalink: /resources/
---




{% assign reference_types = "scientists|students|discussion" | split: "|" %}

{% for type in reference_types %}

{% if type == 'science' %}
### **Resources and data from our published papers**
 {% elsif type == 'students' %}
### **Resources for lab members**
 {% elsif type == 'discussion' %}
### **Other resources**
{% endif %}

<div class="content list">
  {% for post in site.posts %}
    {% if post.categories contains type %}
    <div class="list-item">
      <p class="list-post-title">
        <a href="{{ site.baseurl }}{{ post.url }}">- {{ post.title }}</a>
      </p>
    </div>
    {% endif %}
  {% endfor %}
</div>

<hr>
{% endfor %}
