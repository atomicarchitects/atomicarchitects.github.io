---
layout: default
title: Group Meetings
---

Our group meetings are Wednesdays at 4-5 PM ET. All meetings are in 36-462 (Allen Room), unless otherwise specified.

<table>
    <tr>
        <th>Date</th>
        <th>Time</th>
        <th>Presenter</th>
        <th>Location</th>
    </tr>
    {% assign meeting_count = 0 %}
    {% assign today = "now" | date: "%Y%m%d" %}
    {% assign max_meetings = 8 %}
    {% for meeting in site.data.meetings %}
        {% assign meeting_month = meeting.month | prepend: '00' | slice: -2, 2 %}
        {% assign meeting_day = meeting.day | prepend: '00' | slice: -2, 2 %}
        {% assign meeting_date = meeting.year | append: meeting_month | append: meeting_day %}
        {% if meeting_date >= today and meeting_count < max_meetings %}
            <tr>
                <td>{{meeting.month}}/{{meeting.day}}/{{meeting.year}}</td>
                <td>{{meeting.time}}</td>
                <td>{{meeting.presenter}}</td>
                <td>{{meeting.location}}</td>
            </tr>
            {% assign meeting_count = meeting_count | plus: 1 %}
        {% endif %}
    {% endfor %}
