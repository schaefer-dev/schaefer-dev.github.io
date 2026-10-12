---
layout: default
title: "Daniel Schäfer | Certifications & Skills"
description: "Certifications, technical skills, programming languages and strengths of Daniel Schäfer, Head of Software Architecture & Engineering."
---

<h1>Certifications &amp; Skills</h1>

<section>
<h2 id="certifications">Certifications</h2>
<div class="cert-list">
{% for c in site.data.skills.certifications %}
<div class="entry">
  <h3>{{ c.title }}</h3>
  <span class="meta">{{ c.meta }}</span>
  <p class="project-links">{% for l in c.links %}<a href="{% if l.url contains '://' %}{{ l.url }}{% else %}{{ l.url | relative_url }}{% endif %}">{{ l.text }}</a>{% endfor %}</p>
</div>
{% endfor %}
</div>
</section>

<section>
<h2 id="skills">Skills</h2>
<div class="skill-grid">
{% for g in site.data.skills.groups %}
<div class="skill-group">
  <h3>{{ g.name }}</h3>
  <ul class="tags">{% for i in g.items %}<li>{{ i }}</li>{% endfor %}</ul>
</div>
{% endfor %}
</div>
</section>

<section>
<h2 id="strengths">Strengths</h2>
<dl class="doc-list">
{% for s in site.data.skills.strengths %}
  <dt>{{ s.name }}</dt>
  <dd>{{ s.evidence | markdownify | remove: '<p>' | remove: '</p>' | strip }}</dd>
{% endfor %}
</dl>
</section>
