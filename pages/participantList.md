---
permalink: /participantList/
title: Workshop Participant List
hero_image: /assets/images/uw-fountain.jpg
hide_hero: false
---
<script src="/assets/js/table-sort.js"></script>

Updated: {{ site.data.participant_list.generated_at }}

Number of participants: {{ site.data.participant_list.participants | size }}

{% assign sorted_names = site.data.participant_list.participants | sort: "lastname" %}

Click on table header to change table ordering.

{: .table-sort}
| First Name | Last Name | Institute |
| :--- | :--- | :--- |
{%- for person in sorted_names %}
| {{ person.firstname }} | {{ person.lastname }} | {{ person.affiliation }} |
{%- endfor -%}
