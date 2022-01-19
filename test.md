---
var1: test value
var2: "test value with quotes"
---

# Topics / Collection

{% for topic in site.topics %}
  <a href="{{topic.url}}">{{topic.title}}</a>
  <h2>Meta 1 {{ topic.meta1 }}</h2>
  <h2>Meta 2 {{ topic.meta2 }}</h2>
  <h2>Meta 3 {{ topic.meta3 }}</h2>
  <p>{{ topic.content | markdownify }}</p>
{% endfor %}

# Posts

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

# Tags and related posts

{% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}

# Front matter

<h2>{{page.var1}}</h2>
<h2>{{page.var2}}</h2>