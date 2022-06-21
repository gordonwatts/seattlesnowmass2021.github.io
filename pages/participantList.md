---
permalink: /participantList/
title: Workshop Participant List
hero_image: /assets/images/uw-fountain.jpg
hide_hero: false
---
<script src="/assets/js/table-sort.js"></script>

This page contains a list of all the participants and also some break downs of demographics.

Updated: {{ site.data.participant_list.generated_at }}

## Participants

Number of in-person participants: {{ site.data.participant_list.number_inperson_participants }}

Number of virtual participants: {{ site.data.participant_list.number_virtual_participants }}

Local Organizing Committee/Volunteer/Press: {{ site.data.participant_list.number_LOC_Vol_Press }}

Total number of participants: {{ site.data.participant_list.number_participants }}

### Events

Number of conference dinner attendees: {{ site.data.participant_list.number_dinner_attendees }}

Number of LIGO/Hanford trip attendees: {{ site.data.participant_list.number_LIGO }}

Number of Mariners baseball game attendees: {{ site.data.participant_list.number_baseball }}


### Participant List

{% assign sorted_names = site.data.participant_list.participants | sort: "lastname" %}

Click on table header to change table ordering.

{: .table-sort}
| First Name | Last Name | Institute | Attendance |
| :--- | :--- | :--- | :--- |
{%- for person in sorted_names %}
| {{ person.firstname }} | {{ person.lastname }} | {{ person.affiliation }} |  {{ person.attendance_type }} |
{%- endfor %}

## Participant Breakdowns

By job position type:

<img src="/assets/images/attendance_analysis/piechart_position.png" width="40%" />

By self-reported gender:

<img src="/assets/images/attendance_analysis/piechart_gender.png" width="40%" />
