---
title: Events
---

# Events

[<img alt="" src="{{ "/static/images/icon.calendar.svg" | relative_url }}" class="calendar icon" />](webcal://h2vx.com/ics/get-cal.php?uri={{ page.url | absolute_url | cgi_escape }} "Subscribe to our calendar.")
[Subscribe to our calendar](https://h2vx.com/ics/get-cal.php?uri={{ page.url | absolute_url | cgi_escape }}).

<ol class="h-events">
{% for event in site.events %}
<li>
{% include h-event.html excerpt=true %}
</li>
{% endfor %}
</ol><!-- .h-events -->
