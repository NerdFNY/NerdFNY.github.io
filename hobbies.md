---
layout: page
permalink: /hobbies/index.html
title: Hobbies
---

<div class="hobbies-page">
  <header class="hobbies-hero">
    <h1 class="hobbies-eyebrow">PHOTOGRAPHY</h1>
  </header>

  <section class="memory-section memory-section-zju">
    <div class="memory-heading"><span>01</span><div><p class="memory-kicker">ZJU &amp; HANGZHOU</p><h2>1997 年过去了，我很怀念它</h2></div></div>
    {% assign zju_images = site.static_files | where_exp: "file", "file.path contains '/images/gallery/zju/'" | where_exp: "file", "file.path != '/images/gallery/zju/qingshan-04.jpg'" | where_exp: "file", "file.path != '/images/gallery/zju/manjuelong-06.jpg'" | where_exp: "file", "file.path != '/images/gallery/zju/wuyue-05.jpg'" | where_exp: "file", "file.path != '/images/gallery/zju/wuyue-06.jpg'" | where_exp: "file", "file.path != '/images/gallery/zju/qingshan-03.jpg'" | sort: "path" %}
    <div class="photo-gallery photo-gallery-zju" tabindex="0" aria-label="Zhejiang University and Hangzhou photo reel"><div class="photo-track">
      {% for pass in (1..2) %}{% for image in zju_images %}<figure><img src="{{ image.path }}" alt="Zhejiang University and Hangzhou" loading="lazy" decoding="async"><figcaption>ZJU &amp; Hangzhou</figcaption></figure>{% endfor %}{% endfor %}
    </div></div>
  </section>

  <section class="memory-section memory-section-ntu">
    <div class="memory-heading"><span>02</span><div><p class="memory-kicker">NTU &amp; SINGAPORE</p><h2>北纬一度，光在闪耀</h2></div></div>
    {% assign ntu_images = site.static_files | where_exp: "file", "file.path contains '/images/gallery/ntu/'" | sort: "path" %}
    <div class="photo-gallery photo-gallery-ntu" tabindex="0" aria-label="NTU and Singapore photo reel"><div class="photo-track">
      {% for pass in (1..2) %}{% for image in ntu_images %}<figure><img src="{{ image.path }}" alt="NTU and Singapore" loading="lazy" decoding="async"><figcaption>NTU &amp; Singapore</figcaption></figure>{% endfor %}{% endfor %}
    </div></div>
  </section>

  <section class="memory-section memory-section-tao">
    <div class="memory-heading"><span>03</span><div><p class="memory-kicker">TAO</p></div></div>
    {% assign qingdao_images = site.static_files | where_exp: "file", "file.path contains '/images/gallery/qingdao/'" | sort: "path" %}
    <div class="photo-gallery photo-gallery-tao" tabindex="0" aria-label="Qingdao photo reel"><div class="photo-track">
      {% for pass in (1..2) %}{% for image in qingdao_images %}<figure><img src="{{ image.path }}" alt="Qingdao" loading="lazy" decoding="async"><figcaption>Qingdao</figcaption></figure>{% endfor %}{% endfor %}
    </div></div>
  </section>
</div>
