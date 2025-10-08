{% assign wip = site.data.publications.work_in_progress %}
{% if wip and wip.size > 0 %}
<h2 id="work-in-progress" class="section-heading">Work in Progress</h2>

<div class="wip-list">
{% for link in wip %}
  <div class="wip-card">
    <div class="wip-title">
      {% if link.pdf %}
      <a href="{{ link.pdf }}">{{ link.title }}</a>
      {% else %}
      {{ link.title }}
      {% endif %}
    </div>
    {% if link.summary %}
    <div class="wip-summary">{{ link.summary }}</div>
    {% endif %}
    {% if link.collaborators %}
    <div class="wip-collaborators">with {{ link.collaborators }}</div>
    {% endif %}
    {% if link.notes %}
    <div class="wip-notes">{{ link.notes }}</div>
    {% endif %}
  </div>
{% endfor %}
</div>
{% endif %}
