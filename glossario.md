---
layout: default
title: Glossário
permalink: /glossario/
---

# 📖 Glossário Técnico

Termos do mundo da engenharia de software explicados de forma objetiva. Útil para devs em formação, revisão rápida ou quando você precisa explicar algo para alguém fora da área.

---

{% if site.glossary.size > 0 %}
{% assign sorted_terms = site.glossary | sort: "title" %}
{% assign current_letter = "" %}

{% for term in sorted_terms %}
{% assign first_letter = term.title | slice: 0 | upcase %}
{% if first_letter != current_letter %}
{% assign current_letter = first_letter %}
<h2 style="color: #8afa8a; margin-top: 2rem; border-bottom: 1px solid #3c3c3c; padding-bottom: 0.3rem;">{{ current_letter }}</h2>
{% endif %}

    <div style="margin-bottom: 1rem; padding: 0.8rem; border-left: 3px solid #3c3c3c;">
      <a href="{{ term.url }}" style="font-weight: bold;">{{ term.title }}</a>
      {% if term.description %}
        <p style="margin: 0.3rem 0 0; color: #9e9e9e; font-size: 0.9rem;">{{ term.description }}</p>
      {% endif %}
    </div>

{% endfor %}
{% else %}

<p style="color: #9e9e9e; font-style: italic;">Glossário em construção... 🚧</p>
{% endif %}
