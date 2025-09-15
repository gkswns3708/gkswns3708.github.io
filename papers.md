---
layout: page
title: Papers
permalink: /papers/
---

<input id="paperSearch" type="search" placeholder="제목, 저자, venue, 태그 검색…" style="width:100%; padding:10px; margin:8px 0 18px 0; border:1px solid #ddd; border-radius:8px;">

<ul id="paperList" style="list-style:none; padding-left:0;">
{% for p in site.data.papers %}
  <li class="paper-item" data-search="{{ p.title | downcase }} {{ p.authors | downcase }} {{ p.venue | downcase }} {{ p.year }} {% if p.tags %}{{ p.tags | join: ' ' | downcase }}{% endif %}"
      style="margin:0 0 16px 0; padding:14px; border:1px solid #eee; border-radius:12px;">
    <div style="display:flex; justify-content:space-between; gap:12px; align-items:baseline; flex-wrap:wrap;">
      <div>
        <strong>{{ p.title }}</strong>
        <span style="color:#888;"> ({{ p.year }})</span><br>
        <em style="color:#666;">{{ p.authors }}</em> — {{ p.venue }}
        {% if p.tags %}
          <div style="margin-top:6px;">
            {% for t in p.tags %}<span style="font-size:12px; padding:2px 8px; border:1px solid #ddd; border-radius:999px; margin-right:6px;">{{ t }}</span>{% endfor %}
          </div>
        {% endif %}
      </div>
      <div style="display:flex; gap:10px; white-space:nowrap;">
        <a class="btn" href="{{ p.link | default: '/web/index.html' | relative_url }}">Open index</a>
        {% if p.pdf %}<a class="btn" href="{{ p.pdf }}" target="_blank">PDF</a>{% endif %}
        {% if p.code %}<a class="btn" href="{{ p.code }}" target="_blank">Code</a>{% endif %}
      </div>
    </div>
  </li>
{% endfor %}
</ul>

<script>
(function(){
  const input = document.getElementById('paperSearch');
  const items = Array.from(document.querySelectorAll('.paper-item'));
  function norm(s){ return (s||'').toLowerCase().normalize('NFKD'); }
  input.addEventListener('input', function(){
    const q = norm(this.value.trim());
    items.forEach(li => {
      const hay = norm(li.getAttribute('data-search'));
      li.style.display = hay.includes(q) ? '' : 'none';
    });
  });
})();
</script>
