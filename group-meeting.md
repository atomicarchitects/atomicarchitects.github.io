---
layout: default
title: Group Meeting
---

Our group meetings are Tuesdays at 4-5 pm. All meetings are in 36-428 (Haus Room) unless otherwise specified.

<table>
    <tr>
        <th>Date</th>
        <th>Presenter</th>
        <th>Location</th>
    </tr>
    {% for meeting in site.data.meetings %}
    <tr>
        <td>{{meeting.month}}/{{meeting.day}}/{{meeting.year}}</td>
        <td>{{meeting.presenter}}</td>
        <td>{{meeting.location}}</td>
    {% endfor %}
    </tr>