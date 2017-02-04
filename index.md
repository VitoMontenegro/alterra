---
layout: default
title: продадажа упаковочных материалов
---


<div class="content__inner">
	{% for post in site.categories.Recepts limit: 1 %}
		<div class="content__selection">
			<div class="content__primary">
				<div class="content__primary__top">
					<h2 class="content__primary__top_	_heading">
						{{ post.title }}
					</h2>
					<span class="content__primary__date content__primary__date_top">{{ post.date|date: "%B %d, %Y" }}</span> |
					<span class="	content__primary__top__comments">Комментарии</span>
					<span class="content__primary__top__numebr">116</span>
				</div>
				<div class="content__primary__buttom">
					<div class="content__primary__stikker">
						<img src="{{ "/assets/images/icons/stikker_bg.png" | prepend: site.baseurl }}" alt="">
					</div>
					<div class="content__primary__body">
						<iframe width="620" height="240" src="https://www.youtube.com/embed/{{ post.youtubeId }}" frameborder="0" allowfullscreen></iframe>
					</div>
					<div class="content__primary__footer">
						<div class="content__description__text content__description__text_top">
							{{ post.content }}
						</div>
						<div class="content__primary__button">
							<a href="{{post.url|prepend: site.baseurl}}" class="content__primary__link">
								Читать далее
							</a>									
						</div>	
					</div>							
				</div>
			</div>
		</div>
	{% endfor %}

	<div class="content__selection">
		<h1 class="content__selection__heading">
			Популярное
		</h1>
		<div class="selection__featured__prewiew__wrapper">	
			{% for post in site.categories.Products limit: 3 %}
			<div class="selection__featured__prewiew">
			
				<div class="featured__prewiew__stikker">
					<img src="{{ "/assets/images/icons/stikker.png" | prepend: site.baseurl }}" alt="">
				</div>
				<div class="featured__prewiew__show">
					<iframe width="270" height="100" src="https://www.youtube.com/embed/{{ post.youtubeId }}" frameborder="0" allowfullscreen></iframe>
				</div>
				<div class="featured__prewiew__description">
					<h2 class="content__description__heading">
						{{ post.title }}
					</h2>
					<span class="content__primary__date">{{ post.date|date: "%B %d, %Y" }}</span>
					<div class="content__description__text content__description__text_middle">
						{{ post.content }}
					</div>
					<div class="prewiew__description__button prewiew__description__button_feauter">
						<a href="{{post.url|prepend: site.baseurl}}" class="content__button__link">далее</a>
					</div>
				</div>
				
			</div>		
		{% endfor %}				
	</div>
	</div>
	<div class="content__selection">
		<h1 class="content__selection__heading">
			Ежедневные обновления
		</h1>
			<div class="daily__prewiew__description__wrapper">
					{% for post in site.categories.News limit: 3 %}
			<div class="daily__prewiew__description">
				<div class="daily__prewiew__description__inner">
					<h2 class="content__description__heading">
						{{ post.title }}
					</h2>
					<span class="content__primary__date">
						13 декабря, 2016
					</span>
					<div class="content__description__text content__description__text_bottom">
						{{ post.content }}
					</div>
					<div class="prewiew__description__button">
						<a href="{{ post.url | prepend: site.baseurl }}" class="content__button__link">
							далее
						</a>
					</div>
				</div>									
			</div>
					{% endfor %}		
			<div class="clearfix"></div>					
		</div>				
	</div>					
	<div class="content__footer">
		<div class="content__footer__button">
			<a href="#" class="content__footer__link">
				Комментарий
			</a>
		</div>
	</div>
</div>