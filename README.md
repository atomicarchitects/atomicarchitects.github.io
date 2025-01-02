# atomicarchitects.com

Basically everything is a database in _data.

Information per database:

* `alumni.yml`: name, website, position in lab then, current position, optional bio
* `meetings.yml`: year/month/day, time, presenter(s), location; this is displayed as a table showing the schedule for the next <= 8 group meetings
* `people.yml`: name, email, website, position within lab, optional bio, headshot (preferably square, named "First_Last.jpg" and placed inside `assets/img`)
* `.github/workflows/refresh.yml`: sets up the github action to refresh the website every week. Jekyll builds static websites, which means it can't automatically update the group meeting page every day.