---
layout: default
title: "Daniel Schäfer | Projects"
description: "Personal side projects, work projects at semvox and university projects by Daniel Schäfer, from Swift, Kotlin and Python tools to genAI architecture for the Volkswagen Group."
---

<h1>Projects</h1>

<nav class="jumpbar" aria-label="Sections on this page">
<ul>
  <li><a href="#personal">Side projects</a></li>
  <li><a href="#work">Work</a></li>
  <li><a href="#university">University</a></li>
  <li><a href="#courses">Courses</a></li>
  <li><a href="#other">Other</a></li>
</ul>
</nav>

<section class="projects-section">
<h2 id="personal">Side projects</h2>
<p class="section-intro">Projects I build in my free time to improve my development workflows and solve problems from my own hobbies (birding, cycling, photography, note-taking). Most of them are open source on GitHub.</p>
<div class="project-grid">
{% for p in site.data.personal_projects %}
{% include project-card.html project=p %}
{% endfor %}
</div>
</section>

<section class="projects-section">
<h2 id="work">Work at semvox</h2>
<p class="section-intro">Standout projects from my time at semvox, newest first.</p>
{% for item in site.data.work_projects %}
{% include entry.html item=item %}
{% endfor %}
</section>

<section class="projects-section">
<h2 id="university">University projects</h2>
<p class="section-intro">Projects from my B.Sc. and M.Sc. in Computer Science at Saarland University, newest first.</p>
{% for item in site.data.university_projects %}
{% include entry.html item=item %}
{% endfor %}
</section>

<section class="projects-section courses">
<h2 id="courses">University courses</h2>
<p class="section-intro">Lectures I attended at Saarland University, B.Sc. and M.Sc.</p>
<details class="more">
<summary>Show all {{ site.data.courses | size }} courses</summary>
<table>
  <thead><tr><th>Year</th><th>Term</th><th>Course</th></tr></thead>
  <tbody>
  {% for c in site.data.courses %}{% if c.group == "cs" %}<tr><td>{{ c.year }}</td><td>{{ c.term }}</td><td>{{ c.name }}</td></tr>
  {% endif %}{% endfor %}
  <tr><th colspan="3">Electives outside computer science</th></tr>
  {% for c in site.data.courses %}{% if c.group == "other" %}<tr><td>{{ c.year }}</td><td>{{ c.term }}</td><td>{{ c.name }}</td></tr>
  {% endif %}{% endfor %}
  </tbody>
</table>
</details>
</section>

<section class="projects-section">
<h2 id="other">Other projects</h2>
<ul>
  <li>Teaching myself Python</li>
  <li>Teaching myself Rust</li>
  <li>Teaching myself Swift</li>
  <li>Custom ATMega32U4 Controller installed in Keyboard to support <a href="https://github.com/schaefer-dev/qmk_firmware">QMK Firmware</a> setup to implement fancy features like mouse-control, tap-modifiers and more :)</li>
  <li>Home Network Setup implementing QoS with Traffic Analysis and DPI</li>
  <li>Home-server running DNS server and VPN-tunnel (to get safe and ad-free browsing everywhere in the world)</li>
  <li>Home-server running backup and file servers to manage family documents and keep family photo library up to date</li>
  <li>Running my own Hackintosh for 4+ years</li>
  <li>Managing my <a href="https://github.com/schaefer-dev/dotfiles">dotfiles</a> and improving workflows</li>
  <li>Geeksforgeeks.org and leetcode challenges</li>
  <li>Project Euler</li>
  <li>This website :)</li>
</ul>
</section>
