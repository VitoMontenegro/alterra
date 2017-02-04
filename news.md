---
layout: default
title: Новости
---


{% for post in site.categories.News %}
<div>
	<a href="{{ post.url | prepend: site.baseurl }}"><h2>{{ post.title }}</h2></a><hr />
	<span>{{ post.date | date:"%d %m %Y" }}</span>
	<div class="content__description__text content__description__text_top">
		{{ post.description }}
	</div>
</div>
{% endfor %}