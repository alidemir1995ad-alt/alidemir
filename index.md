---
layout: splash
title: "Ali Demir"
permalink: /
author_profile: true
toc: false

# Lightweight hero (no heavy image for speed)
header:
  overlay_color: "#0f172a"        # slate-900
  overlay_filter: "0.2"
  caption: "Academic homepage"
  actions:
    - label: "CV"
      url: "{{ '/files/ali_demir_cv.pdf' | relative_url }}"
    - label: "Google Scholar"
      url: "https://scholar.google.com/citations?user=PS_CX0AAAAAJ}"
    - label: "GitHub"
      url: "https://github.com/alidemir1995ad-alt"

intro: |
  PhD Researcher in Empirical Economics. Focus: housing ↔ fertility, internal migration, family economics. Rigorous causal inference, reproducible code, clean visuals.

feature_row:
  - title: "Publications"
    excerpt: "Peer-reviewed and working papers with replication links."
    url: "{{ '/publications/' | relative_url }}"
  - title: "Teaching"
    excerpt: "Syllabi, slides, and assignments."
    url: "{{ '/teaching/' | relative_url }}"
  - title: "Talks"
    excerpt: "Conference presentations and invited seminars."
    url: "{{ '/talks/' | relative_url }}"
---

{% include feature_row %}

## Research focus
- Housing and fertility: tenure, size, timing of births.  
- Internal migration: sex-ratio shocks, marriage markets, labor outcomes.  
- Methods: IV, event-study, DID, hazards, transparent preanalysis plans.

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

## Data & code
- Repositories: <a href="https://github.com/alidemir1995ad-alt">GitHub</a>.  
- Replication packages: linked from each paper page.  
- Stack: Stata, R, Python. Clean README, versioned data, seeds set.

## News
{% if site.posts and site.posts.size > 0 %}
{% for post in site.posts limit:3 %}
- {{ post.date | date: "%b %e, %Y" }} — [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}
<p><a class="btn btn--light-outline btn--small" href="{{ '/posts/' | relative_url }}">More updates →</a></p>
{% else %}
_No posts yet._
{% endif %}

## Contact
- Email: <a href="mailto:Ali.Demir-l1f@ruhr-uni-bochum.de">Ali.Demir-l1f@ruhr-uni-bochum.de</a>  
- Affiliation: Ruhr University Bochum  
- ORCID: <a href="https://orcid.org">orcid.org</a>

<!-- Performance notes:
- No large hero image. Uses color overlay only.
- All internal links use | relative_url to respect baseurl.
- Collections preview pulls top 3 manuscripts; define front matter fields (title, authors, venue, year, doi) in /_publications items.
-->
