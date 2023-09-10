---
layout: page
title: svalbard
description: 
img: assets/img/travel/svalbard/20190622-DSC05098-2.jpg
importance: 3
category: fun
---

A selection of my favourite pictures from my time on Svalbard. :snowflake:

<div class="row">
  {% for image in site.static_files %}
    {% capture file_extension %}{{ image.path | split: '.' | last | downcase }}{% endcapture %}
    {% if image.path contains 'assets/img/travel/svalbard' and (file_extension == 'jpg' or file_extension == 'jpeg' or file_extension == 'JPG') %}
      <div class="col-sm-12 col-md-6 col-lg-4 mt-3">
        <div class="gallery-item">
          <a href="{{ image.path }}" data-lightbox="svalbard-gallery" data-title="{{ image.name }}">
            <img src="{{ image.path }}" alt="{{ image.name }}" class="img-fluid rounded z-depth-1">
          </a>
        </div>
      </div>
    {% endif %}
  {% endfor %}
</div>
