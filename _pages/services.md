---
permalink: /services/
title: "AI consulting, training and speaking"
seo_title: "AI Evaluation Consulting, Training & Speaking | Léo Boisvert"
description: "Research-grounded talks, practical training, and advisory support for teams evaluating and deploying language models and autonomous AI agents."
layout: default
author_profile: false
lang: en
alternate_url: /fr/services/
last_modified_at: 2026-07-23
schema: services
---

{% assign services_content = site.data.services[page.lang] %}

<main class="services" id="main-content">
  <header class="services__hero">
    <p class="eyebrow">Consulting & speaking</p>
    <h1>Clear thinking for teams building with AI.</h1>
    <p>I help technical leaders, researchers, and organizations understand what language models can do, where evaluations can fail, and how to build more reliable AI systems.</p>
    <a class="button button--primary" href="mailto:leo.boisvert@hotmail.ca?subject=Consulting%20inquiry">Start a conversation</a>
  </header>

  <section class="services__list" aria-label="Services offered">
    {% for category in services_content.categories %}
      <article class="service-row" id="{{ category.id }}">
        <p class="service-row__index">{{ category.index }}</p>
        <div>
          <h2>{{ category.name }}</h2>
          <p>{{ category.summary }}</p>
        </div>
        <ul>
          {% for topic in category.topics %}
            <li class="service-topic">
              <strong>{{ topic.name }}</strong>
              <span>{{ topic.description }}</span>
            </li>
          {% endfor %}
        </ul>
      </article>
    {% endfor %}
  </section>

  <section class="services__formats" aria-labelledby="formats-title">
    <div>
      <p class="eyebrow">Formats</p>
      <h2 id="formats-title">Designed around your context</h2>
    </div>
    <div class="format-grid">
      {% for format in services_content.formats %}
        <div><strong>{{ format.name }}</strong><span>{{ format.duration }}</span></div>
      {% endfor %}
    </div>
  </section>

  <section class="services__faq" id="faq" aria-labelledby="faq-title">
    <div class="section-heading">
      <p class="eyebrow">Frequently asked questions</p>
      <h2 id="faq-title">What to expect</h2>
    </div>
    <div class="faq-list">
      {% for item in services_content.faq %}
        <article class="faq-item">
          <h3>{{ item.question }}</h3>
          <p>{{ item.answer }}</p>
        </article>
      {% endfor %}
    </div>
  </section>

  <section class="services__contact" aria-labelledby="services-contact-title">
    <div>
      <p class="eyebrow">Let’s work together</p>
      <h2 id="services-contact-title">Tell me what your team is trying to understand or build.</h2>
    </div>
    <div>
      <p>I’ll suggest a format that fits your audience, goals, and level of technical depth.</p>
      <a class="button button--light" href="mailto:leo.boisvert@hotmail.ca?subject=Consulting%20inquiry">Get in touch <span aria-hidden="true">↗</span></a>
    </div>
  </section>
</main>
