---
layout: default
title: Bookmark
---

# 网站收藏夹

这里收藏了我最喜欢的一些网站，希望你也喜欢。

<div class="row" data-masonry='{"percentPosition": true }'>

  {% for member in site.data.bookmarks %}
  <div class="col-sm-6 col-lg-4 mb-4">
    <div class="card">
      {% if member.Image != null %}
      <!-- <svg class="bd-placeholder-img card-img-top" width="100%" height="200" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Placeholder: Image cap" preserveAspectRatio="xMidYMid slice" focusable="false">
        <title>{{ member.Name }}</title>
        <rect width="100%" height="100%" fill="#868e96" /><text x="50%" y="50%" fill="#dee2e6" dy=".3em">Image cap</text>
      </svg> -->
      <div class="bd-placeholder-img card-img-top" width="100%" height="200"  xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Placeholder: Image cap" preserveAspectRatio="xMidYMid slice" focusable="false">
        <img src="images/{{ member.Image }}"/>
      </div>

      <!-- <img class="bd-placeholder-img card-img-top" width="100%" height="200" role="img" aria-label="Placeholder: Image cap" preserveAspectRatio="xMidYMid slice" focusable="false" src="/images/bookmarks/{{ member.Image }}"/> -->
      {% endif %}

      <div class="card-body">
        <h5 class="card-title" style="    display: inline-flex; align-items: center;">
          {{ member.Name }}
          {% if member.Icon != null %}
          <img height="20" focusable="false" src="images/{{ member.Icon }}" style="margin-left: 5px;"/>
          {% endif %}
        </h5>
        <p class="card-text">{{ member.Description }}</p>
        <p class="card-text"><a target = "_blank" href="https://{{ member.Address }}"><small class="text-muted">{{ member.Address }}</small></a></p>
        <!-- <p class="card-text"><small class="text-muted">{{ member.Address }}</small></p> -->
      </div>
    </div>
  </div>
  {% endfor %}

</div>



<script src="https://cdn.jsdelivr.net/npm/masonry-layout@4.2.2/dist/masonry.pkgd.min.js" integrity="sha384-GNFwBvfVxBkLMJpYMOABq3c+d3KnQxudP/mGPkzpZSTYykLBNsZEnG2D9G/X/+7D" crossorigin="anonymous" async></script>