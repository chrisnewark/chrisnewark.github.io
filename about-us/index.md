---
layout: default
title: About Us
display-in-navigation: true
navigation-position: 2
---

<table class="table table-striped table-hover">
    <thead>
        <tr>
            <th>Post</th>
            <th>Name of holder</th>
        </tr>
    </thead>
    <tbody>
        {% for s in site.data.staff %}
            <tr>
                <td>{{ s.post }}</td>
                <td>{{ s.name }}</td>
            </tr>
        {% endfor %}
    </tbody>
</table>

<div class="well">
    <a href="/files/KSAA-Constitution-Rules-Revised-November-2014.pdf">KSAA Constitution & Rules - Revised November 2014</a>
</div>