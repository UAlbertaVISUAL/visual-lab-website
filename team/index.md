---
title: Team
nav:
  order: 3
  tooltip: About our team
---

# {% include icon.html icon="fa-solid fa-users" %}Team

Meet the researchers behind the VISUAL Lab.

{% include section.html %}

{% include list.html data="members" component="portrait" filter="role == 'pi'" %}
{% include list.html data="members" component="portrait" filter="role != 'pi'" %}


{% capture content %}

{% include figure.html image="images/2025_group_photo.jpg" %}
{% include figure.html image="images/Group2018.jpg" %}
{% include figure.html image="images/Group2017.jpg" %}

{% endcapture %}

{% include grid.html style="square" content=content %}
