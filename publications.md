---
layout: default
title: Publications
---
## Publications

<div class="publications-list">
    {% for pub in site.data.publications %}
        <!-- format author list -->
        {% assign authorlist = pub.author | split: " and " -%}
        {% assign numAuthors = authorlist | size %}
        {% assign minusOne = numAuthors | minus: 1 %}
        {% assign minusTwo = numAuthors | minus: 2 %}
        {% assign formattedAuthors = "" %}
        {% for i in (0..minusOne) %}
            {% assign name = authorlist[i] | split: ", " | reverse | join: " " %}
            {% assign formattedAuthors = formattedAuthors | append: name %}
            {% if i < minusOne %}
                {% if numAuthors > 2 %}
                    {% assign formattedAuthors = formattedAuthors | append: ", " %}
                {% else %}
                    {% assign formattedAuthors = formattedAuthors | append: " " %}
                {% endif %}
                {% if i == minusTwo %}
                    {% assign formattedAuthors = formattedAuthors | append: "and " %}
                {% endif %}
            {% endif %}
        {% endfor %}

        {% if pub.journal %}
            {% assign volume = ", " | append: pub.volume %}
            {% if volume == ", " %}
                {% assign volume = "" %}
            {% endif %}
            {% assign number = "(" | append: pub.number | append: ")" %}
            {% if number == "()" %}
                {% assign number = "" %}
            {% endif %}
            {% assign pages = ":" | append: pub.pages %}
            {% if pages == ":" %}
                {% assign pages = "" %}
            {% endif %}
            <p class="pub">({{pub.year}}) {{formattedAuthors}}. {% if pub.url %}<a href="{{pub.url}}">{{pub.title}}</a>{% else %}{{pub.title}}{% endif %}. <i>{{pub.journal}}</i>{{volume}}{{number}}{{pages}}.</p>
        {% elsif pub.institution %}
            <p class="pub">({{pub.year}}) {{formattedAuthors}}. {% if pub.url %}<a href="{{pub.url}}">{{pub.title}}</a>{% else %}{{pub.title}}{% endif %}. <i>{{pub.institution}}</i>.</p>
        {% endif %}
    {% endfor %}
</div>