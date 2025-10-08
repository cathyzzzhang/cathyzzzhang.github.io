{% assign wip = site.data.publications.work_in_progress %}
{% if wip and wip.size > 0 %}
<h2 id="work-in-progress" style="margin: 2px 0px 10px;">Work in Progress</h2>

<ul class="wip-list" style="list-style: none; padding-left: 0; margin: 0;">
{% for link in wip %}
  <li style="margin-bottom: 18px;">
    <div class="title" style="font-weight: 600;">
      {% if link.pdf %}
      <a href="{{ link.pdf }}">{{ link.title }}</a>
      {% else %}
      {{ link.title }}
      {% endif %}
    </div>
    {% if link.authors %}
    <div class="author" style="margin-top: 4px;">{{ link.authors }}</div>
    {% endif %}
    {% if link.collaborators %}
    <div class="collaborators" style="margin-top: 4px;"><em>with {{ link.collaborators }}</em></div>
    {% endif %}
    {% if link.notes %}
    <div class="notes" style="margin-top: 4px;"><strong><i style="color:#e74d3c">{{ link.notes }}</i></strong></div>
    {% endif %}
  </li>
{% endfor %}
</ul>
{% endif %}
