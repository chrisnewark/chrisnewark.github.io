---
layout: default
title: Events
navigation-position: 1
---

<table class="table table-striped table-hover ">
    <tbody>
        {% for event in site.events %}
            {% if event.relative_path contains site.current_season %}
                <tr>
                  <td>{{ event.date }}</td>
                  <td><a href="{{ event.url }}">{{ event.title }}</a></td>
                  <td>{{ event.location }}</td>
                </tr>
            {% endif %}
        {% endfor %}
    </tbody>
</table>
