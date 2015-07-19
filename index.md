---
layout: default
title: Events
navigation-position: 1
---

<table class="table table-striped table-hover ">
    <tbody>
        {% for event in site.events %}
        <tr>
          <td>{{ event.date }}</td>
          <td>{{ event.title }}</td>
          <td>{{ event.location }}</td>
        </tr>
        {% endfor %}
    </tbody>
</table>
