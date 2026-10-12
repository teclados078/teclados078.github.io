<h2 id="publications" style="margin: 2px 0px -15px;">Publications</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.publications.main %}

<li>
<div class="pub-row{% if link.image %} has-thumbnail{% endif %}">
  {% if link.image %}
  <a class="pub-thumbnail" href="{{ link.image | relative_url }}" target="_blank" rel="noopener" aria-label="View full-size figure for {{ link.title | escape }}">
    <img src="{{ link.image | relative_url }}" alt="Representative figure for {{ link.title | escape }}" width="{{ link.image_width }}" height="{{ link.image_height }}" loading="lazy" decoding="async">
  </a>
  {% endif %}
  <div class="pub-details">
      <div class="title">{{ link.title }}</div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em>
      </div>
    <div class="links">
      {% if link.paper %}
      <a href="{{ link.paper }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Paper</a>
      {% endif %}
      {% if link.arxiv %}
      <a href="{{ link.arxiv }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">arXiv</a>
      {% endif %}
      {% if link.code %} 
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if link.page %} 
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
      {% endif %}
      {% if link.notes %} 
      <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
      {% endif %}
    </div>
  </div>
</div>
</li>

{% endfor %}

</ol>
</div>
