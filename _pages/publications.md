---
layout: page
permalink: /publications/
title: publications
nav: true
nav_order: 1
---

{% capture unpublished %}{%  bibliography_count -f papers -q @Preprint* %}{% endcapture %}
{% assign unpublished = unpublished | plus: 0 %}

{% capture accepted %}{%  bibliography_count -f papers -q @Article[accepted]* %}{% endcapture %}
{% assign accepted = accepted | plus: 0 %}

{% capture published %}{%  bibliography_count -f papers -q @Article[doi]* %}{% endcapture %}
{% assign published = published | plus: 0 %}

{% if unpublished >0 %}

<h2>preprints</h2>
<div class="publications">
{% include preprints.html %}
</div>

<hr>
{% endif %}

{% if accepted >0 %}

<h2>accepted papers</h2>
<div class="publications">
{% include accepted_papers.html %}
</div>

<hr>
{% endif %}

{% if published >0 %}

<h2>published papers</h2>
<div class="publications">
{% include published_papers.html %}
</div>

<hr>
{% endif %}

<h2>theses</h2>
<div class="publications">
{% include thesis.html %}
</div>
