---
layout: default
title: Nellie Kolon
---

<div class="flex-title">
  <div>
  <div class="carousel">
  <button class="carousel-arrow left" onclick="moveSlide(-1)">&#8592;</button>
  <img id="carousel-img" src="/assets/media/krug2.png" alt="krug" style="max-width: 200px; border-radius: 8px;">
  <button class="carousel-arrow right" onclick="moveSlide(1)">&#8594;</button>
</div>

{% raw %}
<script>
  const images = [
    "/assets/media/krug1.png",
    "/assets/media/krug2.png",
    "/assets/media/krug3.png"
  ];
  let current = 0;
  function moveSlide(direction) {
    current = (current + direction + images.length) % images.length;
    document.getElementById('carousel-img').src = images[current];
  }
</script>
{% endraw %}
  </div>
  <div style="margin-left: 2rem;">
  At Charles Krug Winery in Napa Valley, I worked as a Harvest Lab Intern, supporting the wine fermentation process from vineyard to bottle. I carried out inoculations of fresh grape juice, monitored fermentation, and used analytical techniques to quantify key chemical properties throughout production. I also gained hands-on experience with wine profiles, grape varietals, and the technical processes that shape the wine industry.
  </div>
</div>

<div style="margin-bottom:8px;"></div>

<div style="display: flex; justify-content: center;">
  <img src="/assets/media/krug4.png" alt="krug4" style="max-width: 650px; border-radius: 8px;">
</div>