---
layout: page
title: Archive
permalink: /archive/
---
<div class="container">
    <div class="row">
        <div class="col col-12">
            <div class="archive-tags">
                {% for tag in site.tags %}
                <a href="{{ site.baseurl }}/tag/{{ tag[0] }}" class="archive-tag">{{ tag[0] | upcase }}</a>
                {% endfor %}
            </div>
        </div>
    </div>
	<div class="row">
		<div class="col col-12">
            {% for post in site.posts %}
                {%- assign _currentdate = post.date | date: '%Y' -%}
                {%- if _currentdate != _date -%}
                    {%- unless forloop.first -%}</ul></section>{%- endunless -%}
                    <section class="archive-year"><h2>{{ _currentdate }}</h2><ul>
                    {%- assign _date = _currentdate -%}
                {%- endif -%}
                <h3>
                    <a href="{{ post.url | prepend: site.baseurl }}">{{post.title}}</a>
                </h3>
            {% endfor %}
        <!-- </div>
	</div>
</div> -->
