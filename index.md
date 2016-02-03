---
layout: default
title: Events
display-in-navigation: true
navigation-position: 1
---
<p>
{% for event in site.events %}
.
{% endfor %}
    </p>
<table class="table table-striped table-hover ">
    <tbody>
        {% for event in site.events %}
        {% if event.relative_path contains site.current_school_year %}
        <tr>
            <td>{{ event.date | date_to_long_string }}</td>
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

<div style="width: 100%; text-align:center;">
    <a href="http://www.phoenix-data-management.co.uk/">
        <img style="display: inline-block; margin-left: auto; margin-right: 20px;" alt="Phoenix data management limited" src="/images/sponsors/phoenix.jpg" width="231" height="96">
    </a>
    <a href="http://www.kentsport.org/">
        <img style="display: inline-block; margin-left: auto; margin-right: auto" class="alignnone" alt="Kent Sport" src="/images/sponsors/kent-sport.jpg">
    </a>
</div>