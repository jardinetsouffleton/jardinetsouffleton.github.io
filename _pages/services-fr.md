---
permalink: /fr/services/
title: "Conseil, formation et conférences en IA"
seo_title: "Conseil, formation et conférences en évaluation de l’IA | Léo Boisvert"
description: "Conférences ancrées dans la recherche, formations pratiques et conseil pour les équipes qui évaluent et déploient des modèles de langage et des agents d’IA."
layout: default
author_profile: false
lang: fr
alternate_url: /services/
last_modified_at: 2026-07-23
schema: services
---

{% assign services_content = site.data.services[page.lang] %}

<main class="services" id="main-content">
  <header class="services__hero">
    <p class="eyebrow">Conseil et conférences</p>
    <h1>Une réflexion claire pour les équipes qui bâtissent avec l’IA.</h1>
    <p>J’aide les responsables techniques, les chercheurs et les organisations à comprendre ce que les modèles de langage peuvent accomplir, où les évaluations peuvent échouer et comment construire des systèmes d’IA plus fiables.</p>
    <a class="button button--primary" href="mailto:leo.boisvert@hotmail.ca?subject=Demande%20de%20consultation">Démarrer une conversation</a>
  </header>

  <section class="services__list" aria-label="Services offerts">
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

  <section class="services__formats" aria-labelledby="formats-title-fr">
    <div>
      <p class="eyebrow">Formats</p>
      <h2 id="formats-title-fr">Conçu pour votre contexte</h2>
    </div>
    <div class="format-grid">
      {% for format in services_content.formats %}
        <div><strong>{{ format.name }}</strong><span>{{ format.duration }}</span></div>
      {% endfor %}
    </div>
  </section>

  <section class="services__faq" id="faq" aria-labelledby="faq-title-fr">
    <div class="section-heading">
      <p class="eyebrow">Questions fréquentes</p>
      <h2 id="faq-title-fr">À quoi vous attendre</h2>
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

  <section class="services__contact" aria-labelledby="services-contact-title-fr">
    <div>
      <p class="eyebrow">Travaillons ensemble</p>
      <h2 id="services-contact-title-fr">Parlez-moi de ce que votre équipe cherche à comprendre ou à construire.</h2>
    </div>
    <div>
      <p>Je vous proposerai un format adapté à votre public, à vos objectifs et au niveau de profondeur technique recherché.</p>
      <a class="button button--light" href="mailto:leo.boisvert@hotmail.ca?subject=Demande%20de%20consultation">Me joindre <span aria-hidden="true">↗</span></a>
    </div>
  </section>
</main>
