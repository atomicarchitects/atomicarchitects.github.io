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

## Alumni

### <a href="https://mariogeiger.ch/">Mario Geiger</a> (<a href="https://atomicarchitects.github.io/assets/img/Mario_Geiger.jpg">photo</a> | <a href=" " title="Mario works on neural networks. When not at Berkeley Lab, he lives in Switzerland. His favorite ice cream flavor is pistachio. Mario is the BDFL of e3nn, a framework for neural networks with Euclidean symmetry.">hover for bio</a>)
Then: Postdoctoral Scholar
Now: NVIDIA

### <a href="https://www.linkedin.com/in/klsky/">Kostiantyn Lapchevskyi</a> (<a href="https://atomicarchitects.github.io/assets/img/koctya_with_duck_small.jpg">photo</a> | <a href=" " title="Applied physicist turned ML engineer pursuing a dream to build ‘The Blue Police Box’ one day.">hover for bio</a>)
Then: Masters Student at the Ukranian Catholic University

### <a href="http://mathben.com/">Ben Miller</a> (<a href="https://atomicarchitects.github.io/assets/img/ben_with_duck_small.jpg">photo</a> | <a href=" " title="Ben relied on physical intuition to get through his undergrad and enjoys learning how to make that physical intuition mathematically precise. He is studying the intersection of statistics, physics, and chemistry at the Freie Universität in Berlin. Specifically, he spends his time creating neural network models which learn using geometry. These days, Ben lies awake thinking about the broad landscape of neural network applications and how they manage to learn at all.">hover for bio</a>)
Then: Masters Student at FU Berlin
<br>
Now: PhD Student at the University of Amsterdam

### <a href="https://www.linkedin.com/in/hashim-piracha-65118116b/">Hashim Piracha</a> (<a href="https://atomicarchitects.github.io/assets/img/hashim_with_duck_small.jpg">photo</a> | <a href=" " title="Joining the team as an undergraduate from UC Berkeley, Hashim can often be spotted calculating tensor products of spherical harmonic signals, clustering atomic datasets, and jamming to Pakistani music. Whilst sipping cups of chai, he applies dimensionality reduction techniques such as t-SNE and PCA to visualize high dimensional data. Note: It is said that the more chai he drinks, the more efficient he becomes."> hover for bio</a> ) {#hashim} 
Then: Undergraduate Research Assistant 
<br>
Now: Undergraduate at UC Berkeley

### <a href="https://elliottperryman.vivaldi.net">Elliott Perryman</a> (<a href="https://atomicarchitects.github.io/assets/img/elliott_with_duck_small.jpg">photo</a> | <a href=" " title="Elliott is an undergraduate student studying computer science and physics and working at LBL through the SULI program. Elliott is from the Mule Capital of the world and enjoys running with friends, reading by the fireplace, and a maximally efficient line of Python."> hover for bio</a> ) {#elliott}
Then: Undergraduate Research Assistant
<br>
Now: Undergraduate at The University of Tennessee, Knoxville

## What's with the rubber ducks?
When someone joins the Atomic Architects, they get a <a href="https://en.wikipedia.org/wiki/Rubber_duck_debugging">debugger duck</a>.
