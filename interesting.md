---
layout: default
title: Интересно
---




<div class="content__selection">
	<div class="content__primary">
	{% for post in site.categories.Interesno %}
		<div class="content__primary__top">
			<a href="{{ post.url | prepend: site.baseurl }}">
				<h2 class="content__primary__top__heading">
					{{ post.title | escape }} 
				</h2>
			</a> 
			<span class="content__primary__date content__primary__date_top">
				{{ post.date | date: "%b %-d, %Y" }}
			</span> |
			<span class="	content__primary__top__comments">Комментарии</span>
			<span class="content__primary__top__numebr">116</span>
		</div>				
		<div class="content__primary__footer">
			<div class="content__description__text ">
			{{ post.content }}
			</div>						
		</div>
	{% endfor %}
	</div>
</div>

