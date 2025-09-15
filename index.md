---
layout: page
permalink: "/"
title: ""
---

<div style="display:flex; gap:24px; align-items:center; flex-wrap:wrap;">
  <img src="{{ site.author.avatar }}" alt="profile" style="width:140px; height:140px; border-radius:50%; object-fit:cover; box-shadow:0 2px 12px rgba(0,0,0,.12);">
  <div>
    <h1 style="margin:0 0 6px 0;">{{ site.author.name }}</h1>
    <p style="margin:0 0 10px 0; color:#666;">
      {{ site.author.role }} · {{ site.author.org }} · {{ site.author.location }}
    </p>
    <p style="margin:0 0 14px 0;">
      연구 관심사: Graph ML, Survival Analysis, EHR, Neuroimaging, RL, Generative Models
    </p>
    <div style="display:flex; gap:10px; flex-wrap:wrap;">
      <a class="btn" href="/papers/">📄 Papers</a>
      <a class="btn" href="https://github.com/{{ site.author.github }}" target="_blank">GitHub</a>
      {% if site.author.scholar and site.author.scholar != "" %}
        <a class="btn" href="https://scholar.google.com/citations?user={{ site.author.scholar }}" target="_blank">Google Scholar</a>
      {% endif %}
      {% if site.author.linkedin and site.author.linkedin != "" %}
        <a class="btn" href="{{ site.author.linkedin }}" target="_blank">LinkedIn</a>
      {% endif %}
      <a class="btn" href="mailto:{{ site.author.email }}">Email</a>
    </div>
  </div>
</div>

<hr>

### 소개
간단한 자기소개를 여기에 적으세요. 최근 관심 프로젝트, 논문, 강연 등.

- GCT for PCI reintervention prediction (EHR)
- Cognitive resilience in Alzheimer’s disease (SC/FC)
- Diffusion-based weak supervision for anomaly detection

> 블로그 포스트를 운영하실 거라면 `_posts/`에 마크다운 파일을 추가하고 `layout: post`로 작성하면 됩니다.
