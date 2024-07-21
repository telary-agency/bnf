---
layout: default
---
<h1 style="text-align: center; margin-bottom: 30px;">News Sites</h1>
<div class="container">
    {% for newspaper in site.data.newspapers %}
    <a href="{{ newspaper.url }}" target="_blank" rel="noopener noreferrer" class="tile-link">
        <div class="tile">
            <img src="{{ newspaper.logo }}" alt="{{ newspaper.name }}" class="logo" onerror="this.onerror=null; this.remove(); this.parentElement.innerHTML='<div class=\'newspaper-name\'>{{ newspaper.name }}</div>';">
        </div>
    </a>
    {% endfor %}
</div>