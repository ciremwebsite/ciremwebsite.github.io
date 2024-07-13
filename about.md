---
title: A propos
call_to_action: Contact
background_image_path:
large_header: false
show_in_navigation: false #true
#navigation_order: 1
---

Le Collectif Interfacultaire Représentant les Externes en Médecine (CIREM) est une association dédiée à la représentation des étudiants en médecine de la 4ème à la 6ème année. Basé sur un modèle de démocratie directe, le CIREM utilise de nombreux sondages pour recueillir les avis de ses membres et s'appuie sur l'expertise de professionnels, notamment juridiques, pour les aider dans leurs démarches.

Notre mission est de garantir que les voix des externes en médecine soient entendues et que leurs intérêts soient défendus de manière efficace et équitable.

# Notre équipe 

<p class="editor-link"><a href="cloudcannon:collections/_staff_members" class="btn"><strong>&#9998;</strong> Update Staff Members</a></p>

<ul class="staff-list">
	{% for member in site.staff_members %}
		<li class="staff">
			<div class="staff-details">
				<div class="staff-image">
					<img src="{{ member.image }}" alt="Staff photo for {{ member.name }}" width="120" height="120">
				</div>
				<ul class="staff-info">
					<li>{{ member.name }}</li>
					<li><small>{{ member.credentials }}</small></li>
					<li><a href="tel:{{ site.data.company.phone }}">{{ site.data.company.phone }}</a>  ext {{ member.phone_extension }}</li>
				</ul>
			</div>

			<div class="staff-bio">
				<p>{{ member.content | markdownify }}</p>
			</div>
		</li>
	{% endfor %}
</ul>
