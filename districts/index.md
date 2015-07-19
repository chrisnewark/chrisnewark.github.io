---
layout: default
title: Districts
display-in-navigation: true
navigation-position: 3
---

<table class="table table-striped table-hover">
    <thead>
        <tr>
            <th>District</th>
            <th>Name</th>
            <th>Contact</th>
        </tr>
    </thead>
    <tbody>
        {% for district in site.districts %}
            <tr>
                <td><a href="{{ district.url }}">{{ district.title }}</a></td>
                {% if site.current_season == "summer" %}
                    <td>{{ district.summer_manager }}</td>
                    <td>{{ district.summer_manager-email }}</td>
                {% else %}
                    <td>{{ district.winter_manager }}</td>
                    <td>{{ district.winter_manager-email }}</td>
                {% endif %}
            </tr>
        {% endfor %}
    </tbody>
</table>