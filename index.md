---
layout: page
permalink: "/"
title: ""
---

<div style="display:flex; gap:24px; align-items:center; flex-wrap:wrap;">
  <style>
  .avatar-wrap{position:relative; width:140px; height:140px; border-radius:50%; padding:3px;
    background: conic-gradient(from 180deg, #a78bfa, #60a5fa, #34d399, #f472b6, #a78bfa);}
  .avatar-wrap img{width:100%; height:100%; border-radius:50%; object-fit:cover; display:block; background:#f6f6f6;}
  .avatar-wrap:hover{transform:translateY(-2px); box-shadow:0 8px 24px rgba(0,0,0,.12); transition:.25s;}
</style>

<div class="avatar-wrap" title="{{ site.author.name }}">
  <img src="{{ site.author.avatar | relative_url }}" alt="profile of {{ site.author.name }}">
</div>
  <div>
    <h1 style="margin:0 0 6px 0;">{{ site.author.name }}</h1>
    <p style="margin:0 0 10px 0; color:#666;">
      {{ site.author.role }} · {{ site.author.org }} · {{ site.author.location }}
    </p>
    <p style="margin:0 0 14px 0;">
      Research Interest: Segmentation, LLM
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
Hi! I’m **Hanjun Choi**, an M.S.- Ph.D. student in the Ai-med Lab at GIST, aiming to become an AI researcher who builds models that work in real-world, diverse settings. I led **WANCDR** as the **sole first author**, with **Prof. Mansu Kim** as the corresponding author—a Wasserstein-adversarial framework that aligns preclinical (GDSC) and clinical (TCGA) gene-expression domains to improve drug-response prediction and generalization to unseen drugs. &#x20;

I’m currently exploring **medical image segmentation**, **LLMs** (for clinical reasoning and multi-modal workflows), and **chemical property modeling** (molecular representations, structure–activity prediction). I enjoy rigorous problem-solving and build end-to-end systems in **C++**, **Python**, and **PyTorch**.

**Contact**
Email: [gkswns3708@naver.com](mailto:gkswns3708@naver.com)

GitHub: [https://github.com/gkswns3708](https://github.com/gkswns3708)


