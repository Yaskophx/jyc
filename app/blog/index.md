---
permalink: /blog/
layout:    default
title:     blog
---
<div id="blog">
	<h1>Blog Posts</h1>
	<ul class="posts">
		{% for post in site.posts %}
			<h2 class="post-title"><a href="{{ post.url }}">{{ post.title }}</a></h2>
			<p class="post-meta">{{ post.date | date_to_string }}</p>
			<p class="post-excerpt">{{ post.excerpt | strip_html }}&hellip; (<a href="{{ post.url }}">Read More</a>)</p>
		{% endfor %}
		
	</ul>
	
</div>