---
title: Team
nav:
  order: 3
  tooltip: About our team
---

# {% include icon.html icon="fa-solid fa-users" %}Team

Meet the researchers behind the VISUAL Lab.

{% include section.html %}

{% include list.html data="members" component="portrait" filter="role == 'principal-investigator'" %}
{% include list.html data="members" component="portrait" filter="role != 'principal-investigator'" %}


{% capture content %}

{% include figure.html image="images/2025_group_photo.jpg" caption="2025 Team" link="team" width="100%"%}

{% endcapture %}

{% include grid.html style="square" content=content %}
