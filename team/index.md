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
{% include list.html data="members" component="portrait" filter="role == 'postdoc'" %}
{% include list.html data="members" component="portrait" filter="role == 'phd'" %}
{% include list.html data="members" component="portrait" filter="role == 'ms'" %}
{% include list.html data="members" component="portrait" filter="role == 'undergrad'" %}




{% capture content %}
<div class="center" style="width:100%;">
  {% include figure.html image="images/2025_group_photo.jpg" caption="2025 Team" link="team" width="100%" %}
</div>
{% endcapture %}
{% include grid.html style="square" content=content %}
