---
layout: template
---

<div class="nav-scroller bg-default-dark shadow-sm" style="width:100%;">
  <nav class="nav nav-underline" aria-label="Secondary navigation" id="navbarSideCollapse">
	{% for p in site.pages %}
		{% if p.blocker == page.blocker %}
			{% if p.permalink %}
				<li class="nav-item active">
					<a class="nav-link" href="{{ p.permalink }}">{{p.button}}</a>
				</li>
			{% else %}
				<li class="nav-item">
					<a class="nav-link" href="{{ p.filename }}">{{p.button}}</a>
				</li>
			{% endif %}
		{% endif %}
	{% endfor %}
  </nav>
</div>

<div class="content">
  	{{ content }}
</div>  