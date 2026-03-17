---
layout: page
title: projects
permalink: /projects/
nav: false
nav_order: 3
horizontal: false
---


{% if site.enable_project_categories and page.display_categories %} {% for category in page.display_categories %}
{{ category }}
{% assign categorized_projects = site.projects | where: "category", category %} {% assign sorted_projects = categorized_projects | sort: "importance" %} {% if page.horizontal %}
{% for project in sorted_projects %} {% include projects_horizontal.liquid %} {% endfor %}
{% else %}
{% for project in sorted_projects %} {% include projects.liquid %} {% endfor %}
{% endif %} {% endfor %}
{% else %}

{% assign sorted_projects = site.projects | sort: "importance" %}

{% if page.horizontal %}

{% for project in sorted_projects %} {% include projects_horizontal.liquid %} {% endfor %}
{% else %}
{% for project in sorted_projects %} {% include projects.liquid %} {% endfor %}
{% endif %} {% endif %}

<!-- pages/projects.md -->

Projets de recherche et collaborations scientifiques en cours

- SnT, Université de Luxembourg, article “HalluGuard: Evidence-Grounded Small Reasoning Models to Mitigate Hallucinations in Retrieval-Augmented Generation” (auteurs: Loris Bergeron, Ioana Buhnila, Jérôme François, Radu State)  en cours de relecture pour la conférence ACL 2026 (The 64th Annual Meeting of the Association for Computational Linguistics, San Diego, California, United States, 2–7 juillet, 2026).
- CHU de Montpellier, étude sur “Utilisation en pratique courante d’un LLM (OSS-120B) pour la génération des documents de sortie : évaluation multidimensionnelle dans le cadre d’un essai randomisé contrôlé aux Urgences Pédiatriques”, (auteurs : Louise Robert, Kevin Yauy, Zeno Loi, Guilain Bochu, Ioana Buhnila, David Morquin), accepté pour présentation orale à la Journée LLM à l'hôpital, organisée par l’ATALA, le 16 et le 17 mars 2026, à Paris.
- RACAI (Research Institute for Artificial Intelligence), Romanian Academy, article “Enhancing the PARSEME-Ro Corpus with Nominal, Modifier and Functional Multiword Expressions” (auteurs: Verginica Barbu Mititelu, Ioana-Maria Biolan, Ioana Buhnila, Mihaela Cristescu, Elena Irimia, Catalin Mihăilă, Isabella Sinca, Amalia Todirascu, Carmen Vasile), publié dans les Actes de la “20th International Conference on Linguistic Resources and Tools for Natural Language”, ConsILR-2025. 
- UniDive (Universality, diversity and idiosyncrasy in language technology), COST Action, CA21167, (2022 – 2026) ; chercheuse chargée de l’annotation des expressions polylexicales en roumain selon le guide PARSEME ; responsables scientifiques : Agata Savary (LISN) et Daniel Zeman (Charles University).
- STAR-FLE (Adaptations stratégiques de textes pour mieux lire et comprendre en FLE), projet ANR (2024 – 2027); chercheuse sur les LLMs pour l’apprentissage des expressions polylexicales en cours de FLE ; responsable scientifique : Amalia Todirascu (LiLPa).

Projets de recherche passés

- ClinReact (Lorraine Université d’Excellence, 2023 – 2025); chercheuse en postdoctorat sur le développement des méthodes de recherche d’informations augmentée (RAG) avec des LLMs pour le domaine médical en français et en anglais; utiliser des LLMs pour assister les chercheurs dans l’amélioration des traitements du cancer du cerveau ; responsables scientifiques : Mathieu Constant (ATILF), Marianne Clausel (IECL), Hélène Dumond (CRAN).
- ADAPTMED (Ressources pour l’adaptation et la simplification des textes médicaux, 2023 – 2024) ; chercheuse et ingénieure d’étude sur l’exploitation semi-automatique des données archivées du web de la BNF dans le contexte de l’épidémie du Covid-19 ; responsable scientifique : Amalia Todirascu (LiLPa).
- SimpleApprenant (Proposer des outils pour remédier aux difficultés d'apprentissage du français langue étrangère, 2017-2019) ; stagiaire en linguistique chargée de l’analyse et de l’annotation des textes écrits par des apprenants du français ; responsable scientifique: Amalia Todirascu (LiLPa).
