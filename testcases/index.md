---
layout: page
title: Testcases
permalink: /testcases/
---

{% assign groups = site.data.testcase | group_by: 'group' %}
{% for group in groups %}
<div class="collapsable">
    <input id="{{ group.name }}" class="toggle" type="checkbox">
    <label for="{{ group.name }}" class="lbl-toggle">{{ group.name }}</label>
    <div class="collapsable-content">    
        <ul class="col2">
            {% for item in group.items %}
            <li>
            <a href="{{ item.id }}">{{item.id}}</a> {{item.name}}
            <a href="{{ item.id }}/medical">(Medical)</a>
            </li>   
            {% endfor %}
        </ul>
    </div>
</div>
{% endfor %}
