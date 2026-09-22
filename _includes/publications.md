<h2 id="publications">Publications</h2>
<div class="publications">
<ol class="bibliography">
{% for paper in site.data.publications.main %}
<li class="pub-row">
<a class="paper-figure" href="{{ paper.page | default: paper.pdf }}" aria-label="{{ paper.title | escape }} — figure and project">
<img src="{{ paper.image }}" class="teaser" alt="{{ paper.acronym }} overview figure" loading="lazy">
</a>
<div class="paper-content">
<div class="paper-role">{{ paper.acronym }} · {{ paper.role }} · {{ paper.venue }}</div>
<div class="title"><a href="{{ paper.pdf }}">{{ paper.title }}</a></div>
<div class="author">{{ paper.authors }}</div>
<p class="paper-summary">{{ paper.summary }}</p>
{% if paper.result %}<p class="paper-result">{{ paper.result }}</p>{% endif %}
{% if paper.contribution %}<p class="paper-contribution">Role: {{ paper.contribution }}</p>{% endif %}
<div class="links">
{% if paper.pdf %}<a href="{{ paper.pdf }}" class="btn">Paper</a>{% endif %}
{% if paper.code %}<a href="{{ paper.code }}" class="btn">Code</a>{% endif %}
{% if paper.page %}<a href="{{ paper.page }}" class="btn">Project &amp; demos</a>{% endif %}
</div>
</div>
</li>
{% endfor %}
</ol>
</div>
