---
layout: default
---
<div class="announcement-banner">
  <div class="banner-content">
    <a href="https://inscriptionbilletterie.bnf.fr/" class="banner-button">Prendre votre pass BNF</a>
    <a href="https://x.com/constant_des" target="_blank" rel="noopener noreferrer" class="banner-button">Suivez nous sur Twitter</a>
  </div>
</div>

<div class="news-container">
  <div class="news-section active" id="websites">
    <h2 class="section-title">Websites</h2>
    <div class="container">
      {% for newspaper in site.data.newspapers %}
        {% if newspaper.part == 'website' %}
          <a href="{{ newspaper.url }}" target="_blank" rel="noopener noreferrer" class="tile-link">
            <div class="tile">
              {% if newspaper.logo and newspaper.logo != "" %}
                <img src="{{ newspaper.logo }}" alt="{{ newspaper.name }}" class="logo">
              {% else %}
                <div class="newspaper-name">{{ newspaper.name }}</div>
              {% endif %}
            </div>
          </a>
        {% endif %}
      {% endfor %}
    </div>
  </div>

  <div class="news-section" id="digital-editions">
    <h2 class="section-title">Digital Editions</h2>
    <div class="container">
      {% for newspaper in site.data.newspapers %}
        {% if newspaper.part == 'digital-edition' %}
          <a href="{{ newspaper.url }}" target="_blank" rel="noopener noreferrer" class="tile-link">
            <div class="tile">
              {% if newspaper.logo and newspaper.logo != "" %}
                <img src="{{ newspaper.logo }}" alt="{{ newspaper.name }}" class="logo">
              {% else %}
                <div class="newspaper-name">{{ newspaper.name }}</div>
              {% endif %}
            </div>
          </a>
        {% endif %}
      {% endfor %}
    </div>
  </div>
</div>

<div class="tabs">
  <button class="tab-btn active" data-target="websites">Websites</button>
  <button class="tab-btn" data-target="digital-editions">Digital Editions</button>
</div>

