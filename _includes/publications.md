<h2 id="publications">Publications</h2>
<p><small>* Equal contribution.</small></p>

<div class="publications" style="margin-top: 0;">
  <ol class="bibliography">
    {% for paper in site.data.publications.main %}
    <li>
      <div class="pub-row">
        <div class="abbr">
          <abbr class="badge" title="{{ paper.conference | escape }}">{{ paper.conference_short | escape }}</abbr>
          {% if paper.image and paper.image != "" %}
          <a class="teaser-link" href="{{ paper.image | relative_url | escape }}" target="_blank" rel="noopener" aria-label="Open full-size figure for {{ paper.title | escape }}">
            <img src="{{ paper.image | relative_url | escape }}" class="teaser" alt="{{ paper.image_alt | default: paper.title | escape }}" loading="lazy" />
          </a>
          {% else %}
          <div class="teaser teaser-placeholder" aria-hidden="true">
            <span>Image coming soon</span>
          </div>
          {% endif %}
        </div>

        <div class="publication-details">
          <div class="title">
            <a href="{{ paper.page | escape }}">{{ paper.title | escape }}</a>
          </div>

          <div class="author">{{ paper.authors }}</div>
          <div class="periodical"><em>{{ paper.conference | escape }}</em></div>

          {% if paper.notes %}
          <div class="notes">
            <strong>{{ paper.notes | escape }}</strong>
          </div>
          {% endif %}

          <div class="links">
            <a class="btn" href="{{ paper.pdf | escape }}">PDF</a>
            {% if paper.code %}
            <a class="btn" href="{{ paper.code | escape }}">Code</a>
            {% endif %}
            {% if paper.talk %}
            <a class="btn" href="{{ paper.talk | escape }}">Talk</a>
            {% endif %}
          </div>
        </div>
      </div>
    </li>
    {% endfor %}
  </ol>
</div>
