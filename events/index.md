---
title: Events
---

# Upcoming events

[<img alt="" src="{{ "/static/images/icon.calendar.svg" | relative_url }}" class="calendar icon" />](webcal://h2vx.com/ics/get-cal.php?uri={{ page.url | absolute_url | cgi_escape }} "Subscribe to our calendar.")
[Subscribe to our calendar](https://h2vx.com/ics/get-cal.php?uri={{ page.url | absolute_url | cgi_escape }}).

{% assign events = site.events | where_exp: "event", "event.endDate > site.time" | sort: "startDate" %}
<ol class="h-events">
{% for event in events %}
    <li>
        {% include h-event.html excerpt=true %}
    </li>
{% endfor %}
</ol><!-- .h-events -->

# Past events

{% assign events = site.events | where_exp: "event", "event.endDate < site.time" | sort: "startDate" %}
<ol class="h-events">
{% for event in events reversed %}
    <li>
        {% include h-event.html excerpt=true %}
    </li>
{% endfor %}
</ol><!-- .h-events -->
