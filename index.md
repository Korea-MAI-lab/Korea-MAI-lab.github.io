---
layout: home
permalink: /
---

<p class="intro"><strong>MAI Lab</strong> develops multimodal acoustic imaging technologies for biomedical measurement, visualization, and quantitative analysis. We integrate imaging physics, instrumentation, signal/image processing, and computational methods to make acoustic imaging more informative and more useful.</p>

<div class="section-head">
  <h2>Research Focus</h2>
  <a href="{{ '/research/' | relative_url }}">Research overview →</a>
</div>

<div class="focus-grid">
  <article class="focus-card">
    <div class="focus-number">01 · ACOUSTIC BIOIMAGING</div>
    <h3>Photoacoustic & Ultrasound Imaging</h3>
    <p>Multimodal systems for structural, functional, and molecular imaging across preclinical and translational applications.</p>
  </article>
  <article class="focus-card">
    <div class="focus-number">02 · RADIATION ACOUSTICS</div>
    <h3>Radiation-Induced Acoustic Imaging</h3>
    <p>Acoustic sensing and reconstruction of energy deposition for radiation imaging, dosimetry, and emerging hybrid modalities.</p>
  </article>
  <article class="focus-card">
    <div class="focus-number">03 · COMPUTATIONAL IMAGING</div>
    <h3>AI & Quantitative Reconstruction</h3>
    <p>Physics-aware reconstruction, signal enhancement, segmentation, and quantitative biomarker extraction from multimodal data.</p>
  </article>
</div>

<div class="section-head">
  <h2>Latest News</h2>
  <a href="{{ '/news/' | relative_url }}">View all →</a>
</div>
<div class="news-grid">
{% assign sorted_news = site.news | sort: 'date' | reverse %}
{% for post in sorted_news limit:3 %}
  <a class="news-card" href="{{ post.url | relative_url }}">
    <div class="news-date">{{ post.date | date: "%Y.%m" }}</div>
    <h3>{{ post.title }}</h3>
    <div class="muted">{{ post.excerpt | strip_html | truncatewords: 20 }}</div>
  </a>
{% endfor %}
</div>

<div class="section-head">
  <h2>Selected Publications</h2>
  <a href="{{ '/publications/' | relative_url }}">View all →</a>
</div>
<p class="muted">The publications page is generated from a BibTeX file, so new papers can be added without editing HTML.</p>
