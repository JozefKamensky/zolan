---
layout: page
title: Archive
permalink: /archive/
---
<div class="container">
	<div class="row">
		<div class="col col-12">
            {% for post in site.posts %}
                {%- assign _currentdate = post.date | date: '%Y' -%}
                {%- if _currentdate != _date -%}
                    {%- unless forloop.first -%}</ul></section>{%- endunless -%}
                    <section><h2>{{ _currentdate }}</h2><ul>
                    {%- assign _date = _currentdate -%}
                {%- endif -%}
                <h3 >
                    <a href="{{ post.url | prepend: site.baseurl }}">{{post.title}}</a>
                </h3>
            {% endfor %}
        <!-- </div>
	</div>
</div> -->
