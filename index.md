---
layout: splash
title: "Ali Demir"
permalink: /
author_profile: true
toc: false

header:
  overlay_color: "#0f172a"
  overlay_filter: "0.2"
  caption: "Academic homepage"
  actions:
    - label: "CV"
      url: "{{ '/files/ali_demir_cv.pdf' | relative_url }}"
    - label: "Google Scholar"
      url: "https://scholar.google.com/citations?user=PS_CX0AAAAAJ"
    - label: "GitHub"
      url: "https://github.com/alidemir1995ad-alt"

intro: |
  PhD Researcher in Empirical Economics. Focus: housing ↔ fertility, internal migration, family economics.

feature_row:
  - title: "Publications"
    excerpt: "Peer-reviewed and working papers with replication links."
    url: "{{ '/publications/' | relative_url }}"
  - title: "Teaching"
    excerpt: "Syllabi, slides, and assignments."
    url: "{{ '/teaching/' | relative_url }}"
  - title: "Talks"
    excerpt: "Conference presentations and seminars."
    url: "{{ '/talks/' | relative_url }}"
---

{% include feature_row %}

## Research focus
- Housing and fertility; internal migration; family economics.
- Methods: IV, event-study, DID, hazards.

## Selected papers
{% assign pubs = site.publications | where: "category", "manuscripts" | sort: "date" | reverse %}
{% if pubs and pubs.size > 0 %}
{% for pub in pubs limit:3 %}
- **[{{ pub.title }}]({{ pub.url | relative_url }})**{% if pub.authors %} — {{ pub.authors }}{% endif %}{% if pub.venue %}, _{{ pub.venue }}_{% endif %}{% if pub.year %} ({{ pub.year }}){% endif %}{% if pub.doi %}. DOI: {{ pub.doi }}{% endif %}
{% endfor %}
<p><a class="btn btn--primary btn--small" href="{{ '/publications/' | relative_url }}">All publications →</a></p>
{% else %}
_Coming soon. See_ <a href="https://scholar.google.com/citations?user=PS_CX0AAAAAJ">Google Scholar</a>.
{% endif %}

## News
{% if site.posts and site.posts.size > 0 %}
{% for post in site.posts limit:3 %}
- {{ post.date | date: "%b %e, %Y" }} — [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}
{% else %}
_No posts yet._
{% endif %}

## Contact
- Email: <a href="mailto:Ali.Demir-l1f@ruhr-uni-bochum.de">Ali.Demir-l1f@ruhr-uni-bochum.de</a>
- Affiliation: Ruhr University Bochum
