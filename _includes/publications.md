<section id="publications" aria-labelledby="publications-heading">
<h2 id="publications-heading">Publications</h2>

<ol class="pubs">
{% for pub in site.data.publications.main %}
  <li class="pub">
    {% if pub.image %}
    <a class="pub-media" href="{{ pub.pdf }}" tabindex="-1" aria-hidden="true">
      <img src="{{ pub.image }}" alt="" loading="lazy">
    </a>
    {% endif %}
    <div class="pub-body">
      {% if pub.conference_short %}<p class="pub-venue">{{ pub.conference_short }}</p>{% endif %}
      <h3 class="pub-title"><a href="{{ pub.pdf }}">{{ pub.title }}</a></h3>
      <p class="pub-authors">{{ pub.authors | replace: "Jushan Chen", "<strong>Jushan Chen</strong>" }}</p>
      {% if pub.conference %}<p class="pub-where">{{ pub.conference }}</p>{% endif %}
      <p class="pub-links">
        {% if pub.pdf %}<a href="{{ pub.pdf }}">Paper</a>{% endif %}
        {% if pub.code %}<a href="{{ pub.code }}">Code</a>{% endif %}
        {% if pub.page %}<a href="{{ pub.page }}">Project page</a>{% endif %}
        {% if pub.bibtex %}<a href="{{ pub.bibtex }}">BibTeX</a>{% endif %}
        {% if pub.notes %}<span class="pub-note">{{ pub.notes }}</span>{% endif %}
      </p>
    </div>
  </li>
{% endfor %}
</ol>
</section>
