---
title: Events
---

<ol class="h-events">
{% for event in site.events %}
<li>
{% include h-event.html event=event %}
</li>
{% endfor %}
</ol><!-- .h-events -->
