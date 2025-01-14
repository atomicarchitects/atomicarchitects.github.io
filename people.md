---
layout: default
title: People
---

<div class="people-list">
{% for person in site.data.people %}
    {% assign splitname = person.name | split: " " -%}
      <div style="width: 170px; height: 270px; display: grid; grid-template-rows: 170px 3em auto 1em; padding: 10px 15px;">
        <img src="assets/img/{{splitname | join: '_'}}.jpg" height="170px" style="width: auto;"/>
        <h3 style="margin-bottom: 0;">
          <a href="{{person.website}}" title="{{person.bio}}">{{person.name}}</a>
        </h3>
        <h3 style="margin-bottom: 0;">{{person.position}}</h3>
        <h4 style="margin-bottom: 0;"><a href="mailto:{{person.email}}">Email</a></h4>
      </div>
{% endfor %}
</div>

<h2 style="padding-top:1em;">Alumni</h2>

<div class="alumni-list"> 
{% for person in site.data.alumni %}
    {% assign splitname = person.name | split: " " -%}
        <h3><a href="{{person.website}}">{{person.name}}</a> (<a href="https://atomicarchitects.github.io/assets/img/{{splitname | join: '_'}}.jpg">photo</a> | <a href=" " title="{{person.bio}}">hover for bio</a>)</h3>

        <p>Then: {{person.then}}
        
        {% if person.now != 'blank' %}
            <br> Now: {{person.now}}
        {% endif %}
        </p>
{% endfor %}
</div>

## What's with the rubber ducks?
When someone joins the Atomic Architects, they get a <a href="https://en.wikipedia.org/wiki/Rubber_duck_debugging">debugger duck</a>.
