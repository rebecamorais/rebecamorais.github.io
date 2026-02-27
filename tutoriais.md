---
layout: default
title: Tutoriais
permalink: /tutoriais/
---

# 📚 Tutoriais

Guias práticos sobre ferramentas, fluxos de desenvolvimento e boas práticas que uso no dia a dia — escritos para quem já tem alguma base técnica mas quer ir direto ao ponto.

---

{% if site.tutorials.size > 0 %}

<ul style="list-style: none; padding: 0;">
  {% assign sorted_tutorials = site.tutorials | sort: "date" | reverse %}
  {% for tutorial in sorted_tutorials %}
  <li style="margin-bottom: 1.5rem; padding: 1rem; border: 1px solid #3c3c3c; border-radius: 6px;">
    <a href="{{ tutorial.url }}" style="font-size: 1.1rem; font-weight: bold;">{{ tutorial.title }}</a>
    {% if tutorial.description %}
      <p style="margin: 0.4rem 0 0; color: #9e9e9e; font-size: 0.9rem;">{{ tutorial.description }}</p>
    {% endif %}
    {% if tutorial.tags %}
      <p style="margin: 0.4rem 0 0; font-size: 0.8rem; color: #5a5a5a;">
        🏷️ {{ tutorial.tags | join: " · " }}
      </p>
    {% endif %}
  </li>
  {% endfor %}
</ul>
{% else %}
<p style="color: #9e9e9e; font-style: italic;">Em breve, os primeiros tutoriais... 🚧</p>
{% endif %}
