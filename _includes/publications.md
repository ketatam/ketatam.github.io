<h2 id="publications">Publications</h2>
<p><small>* Equal contribution.</small></p>

<div class="publications" style="margin-top: 0;">
  <ol class="bibliography">
    {% for paper in site.data.publications.main %}
    <li style="min-height: 0; margin-bottom: 1.8rem;">
      <div class="title">
        <a href="{{ paper.pdf | escape }}">{{ paper.title | escape }}</a>
      </div>

      <div class="author">{{ paper.authors }}</div>
      <div class="periodical">{{ paper.conference }}</div>

      {% if paper.notes %}
      <div style="margin-top: 0.25rem;">
        <strong>{{ paper.notes | escape }}</strong>
      </div>
      {% endif %}

      {% if paper.summary %}
      <p style="margin: 0.4rem 0 0.6rem;">
        {{ paper.summary | escape }}
      </p>
      {% endif %}

      <div class="links">
        <a class="btn" href="{{ paper.pdf | escape }}">Paper</a>
        {% if paper.code %}
        <a class="btn" href="{{ paper.code | escape }}">Code</a>
        {% endif %}
        {% if paper.talk %}
        <a class="btn" href="{{ paper.talk | escape }}">Talk</a>
        {% endif %}
      </div>
    </li>
    {% endfor %}
  </ol>
</div>