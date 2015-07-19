---
layout: default
title: Events
display-in-navigation: true
navigation-position: 1
---

<table class="table table-striped table-hover ">
    <tbody>
        {% for event in site.events %}
            {% if event.relative_path contains site.current_school_year %}
                <tr>
                    <td>{{ event.date }}</td>
                    <td>
                        {% assign content = event.content | strip_newlines %}
                        {% if content == "" %}
                            {{ event.title }}
                        {% else %}
                            <a href="{{ event.url }}">{{ event.title }}</a>
                        {% endif %}                
                    </td>
                    <td>{{ event.location }}</td>
                </tr>
            {% endif %}
        {% endfor %}
    </tbody>
</table>
