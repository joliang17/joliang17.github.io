---
permalink: /
title: "Biography"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a fourth-year Ph.D. student in the Department of Computer Science at [University of Maryland, College Park](https://umd.edu/), advised by [Prof. Tianyi Zhou](https://tianyizhou.github.io/). 
My research interests are data-centric AI, computer vision (CV), and vision-language models (VLMs), especially exploring synthetic data generation and self-improving learning paradigms to improve model training and evaluation.

I am currently interested in **self-improving vision-language models** — training VLMs to create their own learning signal (on-policy self-distillation, self-evolving question generation) — and **agentic visual systems** that actively explore and gather evidence rather than answer in one shot.

I got my M.Eng. degree in Industrial Engineering and Operations Research at [University of California, Berkeley](https://ieor.berkeley.edu/). Before joining UCB, I obtained my B.Eng. degree in Industrial Engineering at [Tsinghua University](https://www.ie.tsinghua.edu.cn/eng/). 

News
======

<ul class="news-list">
  <li><time>2026.07</time><span><a href="https://arxiv.org/abs/2607.21556">Visual Contrastive Self-Distillation</a> is on arXiv — reward- and teacher-free on-policy self-distillation for VLMs. <a href="https://joliang17.github.io/VisualCSD/">Project page</a>.</span></li>
  <li><time>2026.07</time><span><a href="https://arxiv.org/abs/2512.11995">V-REX</a> is accepted to <strong>ECCV 2026</strong>; <a href="https://arxiv.org/abs/2603.06480">History-conditioned token pruning for VLN</a> is accepted to <strong>IROS 2026</strong>.</span></li>
  <li><time>2026.06</time><span><a href="https://arxiv.org/abs/2606.13929">Self-Evolving Visual Questioner</a> is on arXiv — VLMs that improve by asking themselves better questions.</span></li>
  <li><time>2025.09</time><span><a href="https://arxiv.org/abs/2504.10514">ColorBench</a> is accepted to <strong>NeurIPS 2025</strong>; received a NeurIPS 2025 Student Travel Award.</span></li>
</ul>

Publications
======

<div class="pub-toggle" role="group" aria-label="Publication view">
  <button class="chip is-active" type="button" data-pub-view="selected">Selected</button>
  <button class="chip" type="button" data-pub-view="all">All ({{ site.data.publications | size }})</button>
  <span class="section-note pub-toggle__note">* denotes equal contribution</span>
</div>

<ul class="pub-cards">
{% for pub in site.data.publications %}
  <li class="pub-card{% unless pub.selected %} pub-card--extra is-hidden{% endunless %}">
    {% if pub.teaser %}<a class="pub-card__thumb" href="{{ pub.url }}"><img src="/images/teasers/{{ pub.teaser }}" alt="" loading="lazy"></a>{% endif %}
    <div class="pub-card__body">
      <a class="pub-card__title" href="{{ pub.url }}">{{ pub.title }}</a>
      <p class="pub-card__authors">{{ pub.authors | markdownify | remove: "<p>" | remove: "</p>" | strip }}</p>
      <p class="pub-card__meta"><span class="venue">{{ pub.venue }}</span>
        <a href="{{ pub.url }}">paper</a>
        {% if pub.code %}<a href="{{ pub.code }}">code</a>{% endif %}
        {% if pub.page %}<a href="{{ pub.page }}">project page</a>{% endif %}
        {% if pub.data %}<a href="{{ pub.data }}">dataset</a>{% endif %}</p>
    </div>
  </li>
{% endfor %}
</ul>

<p class="more-link"><a href="/publications/">Browse by topic →</a></p>

<script>
(function () {
  var chips = document.querySelectorAll('[data-pub-view]');
  var extras = document.querySelectorAll('.pub-card--extra');
  chips.forEach(function (chip) {
    chip.addEventListener('click', function () {
      chips.forEach(function (c) { c.classList.remove('is-active'); });
      chip.classList.add('is-active');
      var showAll = chip.getAttribute('data-pub-view') === 'all';
      extras.forEach(function (li) { li.classList.toggle('is-hidden', !showAll); });
    });
  });
})();
</script>

Education
======

<ul class="edu-list">
  <li><div><strong>University of Maryland, College Park</strong><span>Ph.D. in Computer Science</span></div><time>2023 – present</time></li>
  <li><div><strong>University of California, Berkeley</strong><span>M.Eng. in Industrial Engineering &amp; Operations Research</span></div><time>2019 – 2020</time></li>
  <li><div><strong>Tsinghua University</strong><span>B.Eng. in Industrial Engineering</span></div><time>2015 – 2019</time></li>
</ul>

Awards & Service
======

<ul class="compact-list">
  <li><strong>Silver Reviewer Award</strong>, ICML 2026</li>
  <li><strong>Student Travel Award</strong>, NeurIPS 2025</li>
  <li><strong>Dean's Fellowship &amp; Chair's Fellowship</strong>, University of Maryland, 2023</li>
  <li><strong>Reviewer</strong>: ICLR 2027, ICML 2026 &nbsp;·&nbsp; <strong>Program Committee</strong>: AAAI 2026</li>
</ul>
