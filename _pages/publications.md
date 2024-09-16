---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

Published
=======

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}

Working Papers
======

Online algorithms for Participatory Budgeting
------
With Jan Maly

Deciding whether to fund a proposed project from a limited budget or not is one of the most
common and crucial problems in basically any organisation. The rise of participatory budgeting
(PB) over the last 30 years [Dias et al.(2019)] has demonstrated that such funding decision
can be made in a democratic and participatory way. So far, PB has mostly been used on
the level of municipalities, but recently it has also been applied in smaller organisations, for
example in Lithuanian schools1 . Currently, PB is usually organized as a yearly one shot event
in which the whole budget for the year is decided upon in one election. However, in many
cases, funding decisions have to be made continuously throughout the year whenever a new
project is proposed.

[See paper, (preliminary version)](https://matthieuhervouin.github.io/files/Online_Participatory_Budgeting.pdf)

