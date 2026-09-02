

**BACHELOR CHEF DE PROJET DIGITAL**

**GESTION DE PROJET DIGITAL**

*Cours restructuré & enrichi — Version 2*

# **MODULE 1 — FONDAMENTAUX**

Un projet \= effort temporaire pour créer un produit, service ou résultat unique. Début, fin, objectifs, ressources sous contraintes.

## **1.1 Le triangle des contraintes (QCD)**

| Le triangle Qualité – Coût – Délai |  |
| ----- | :---- |
| **Concept** | Tout projet est gouverné par 3 variables interdépendantes. Toucher à l'une affecte obligatoirement les deux autres. Il faut choisir sa contrainte principale dès le départ. |
| **Objectif** | Piloter avec un cap clair plutôt que de vouloir tout optimiser en même temps. |
| **Résultat Attendu** | Un projet livré dans le respect de la contrainte principale, avec arbitrages documentés. |
| **Points Clés** | Identifier dès le cadrage quelle contrainte est non-négociable (souvent le délai ou le budget). Promettre 'rapide, pas cher ET de qualité' est physiquement impossible — le dire franchement. Documenter l'arbitrage QCD pour se protéger en cas de conflit client. |
| **Erreurs À éviter** | Croire qu'on peut tout optimiser en même temps. Ne pas nommer la contrainte prioritaire → chacun interprète à sa façon. Changer l'axe prioritaire en cours de route sans renégocier. |
| **Exemple Concret** | Site e-commerce avant Noël : contrainte principale \= délai. On réduit le périmètre (moins de pages produits), mais on ne décale pas la date de lancement. |

## **1.2 Les méthodes de gestion de projet**

Pas de méthode universelle. Le choix dépend du contexte, du niveau d'incertitude et de la taille du projet.

| Waterfall (Cascade) — Méthode prédictive |  |
| ----- | :---- |
| **Concept** | Approche séquentielle : chaque phase est complétée avant de passer à la suivante. Le plan est défini une fois pour toutes au départ. Phases : Analyse → Conception → Développement → Tests → Déploiement. |
| **Objectif** | Cadrer totalement un projet dont les exigences sont connues, stables et contractuelles. |
| **Résultat Attendu** | Livrable conforme aux spécifications initiales, visibilité totale sur coûts et délais. |
| **Points Clés** | Obligatoire quand le budget doit être précisément chiffré en amont (marchés publics). Idéal dans les secteurs réglementés : santé, banque, nucléaire. Tout changement de périmètre doit passer par un processus formel (Change Request). |
| **Erreurs À éviter** | L'utiliser sur un projet innovant où les besoins vont forcément évoluer. Bloquer les changements sans aucune soupape d'arbitrage. Négliger les tests en fin de cycle — la dette s'accumule. |
| **Exemple Concret** | Refonte du système de facturation d'une mutuelle : budget voté par le CA, audit réglementaire prévu. Waterfall imposé par le contexte. |

| RAD (Rapid Application Development) — Itératif centré utilisateur |  |
| ----- | :---- |
| **Concept** | 4 phases cycliques : Définir les exigences → Prototype → Construction → Déploiement. Les utilisateurs valident à chaque itération. On livre vite pour apprendre vite. |
| **Objectif** | Réduire le risque d'inadéquation avec les vrais besoins en testant des prototypes réels tôt. |
| **Résultat Attendu** | Produit validé par les utilisateurs, moins d'effet tunnel, corrections peu coûteuses. |
| **Points Clés** | Implique fortement les utilisateurs finaux — sans eux, ça ne fonctionne pas. Les bugs trouvés tôt coûtent 10× moins cher à corriger qu'en fin de projet. Adapté aux projets digitaux avec périmètre flou au départ. |
| **Erreurs À éviter** | Sauter la phase 'définir les exigences' pour aller vite sur le prototype. Ne pas documenter les décisions prises pendant les itérations. Confondre RAD et absence de planning. |
| **Exemple Concret** | Application interne de gestion des congés : prototype livré en 2 semaines, RH testent, 3 itérations, version finale validée en 6 semaines. |

| Scrum — Méthode agile par sprints |  |
| ----- | :---- |
| **Concept** | Cadre agile organisé en sprints de 2 semaines. Chaque sprint produit un incrément fonctionnel livrable. L'équipe s'auto-organise autour d'un backlog priorisé. |
| **Objectif** | Livrer de la valeur en continu sur des projets où le périmètre évolue fréquemment. |
| **Résultat Attendu** | Incréments fonctionnels livrés toutes les 2 semaines, feedback intégré au fil de l'eau. |
| **Points Clés** | 3 rôles : Product Owner (priorités), Scrum Master (facilitation), équipe de développement. 4 cérémonies clés : Sprint Planning, Daily Standup (15 min), Sprint Review, Rétrospective. Le backlog est vivant — il évolue avec le projet. |
| **Erreurs À éviter** | Faire du 'Scrum washing' : garder les réunions, supprimer la discipline. Product Owner indisponible → l'équipe bloquée sur les priorités. Sprints trop longs (\> 4 semaines) → on perd l'agilité. |
| **Exempleconcret** | Plateforme SaaS B2B : Sprint 1 \= authentification \+ dashboard. Sprint 2 \= module facturation. Le client valide chaque sprint. Priorités réajustées à chaque Sprint Planning. |

| Kanban — Flux continu visuel |  |
| ----- | :---- |
| **Concept** | Méthode de gestion de flux : les tâches avancent de colonne en colonne (À faire → En cours → Terminé) sur un tableau visuel. Pas de sprints — le travail est continu. |
| **Objectif** | Visualiser le flux de travail, limiter le travail en cours (WIP) et identifier les goulots d'étranglement. |
| **Résultat Attendu** | Flux fluide, moins de multitâche, livraisons continues. |
| **Points Clés** | WIP Limit \= nombre maximum de tâches simultanées par colonne. C'est la règle clé. Idéal pour la maintenance, le support, ou les équipes en amélioration continue. Outils : Trello, Jira, Linear, simple tableau physique. |
| **Erreurs À éviter** | Pas de WIP limit → le tableau se remplit sans que rien ne sorte. Utiliser Kanban sur un projet avec une date de livraison ferme et des dépendances — préférer Scrum ou Waterfall. Colonnes trop génériques (À faire / En cours / Fait) → pas assez de visibilité. |
| **Exemple Concret** | Équipe support d'une agence web : tickets entrants traités en flux continu. WIP limit \= 3 tickets par développeur en simultané. Chaque ticket visible sur le board Trello. |

| Méthode | Quand l'utiliser ? | Exemples secteurs |
| :---- | :---- | :---- |
| **Waterfall** | Besoin connu \+ budget fixe \+ secteur réglementé | Marchés publics, BTP, banque, santé |
| **RAD** | Besoin flou \+ utilisateurs disponibles \+ délai court | Apps internes, MVP startup |
| **Scrum** | Produit digital \+ périmètre évolutif \+ équipe dédiée | SaaS, e-commerce, applis mobiles |
| **Kanban** | Flux continu \+ pas de date butoir fixe | Support, maintenance, content ops |

# **MODULE 2 — CADRAGE & DOCUMENTS CLÉS**

## **2.1 Les 4 documents de cadrage**

| Document | Contenu | Qui valide ? |
| :---- | :---- | :---- |
| **Lettre de mission** | Mandat officiel confié au CDP : mission, périmètre haut niveau, durée | Direction générale |
| **Charte de projet** | Projet officiellement lancé : objectifs, budget, sponsors, risques macro | Sponsor / Direction |
| **Note de cadrage** | Périmètre détaillé, grandes lignes opérationnelles, acteurs identifiés | Maître d'ouvrage |
| **Cahier des charges** | Ce qu'on fait, comment et dans quelles conditions. Document de référence contractuel. | MOA \+ MOE |

## **2.2 Rédiger un cahier des charges — Les 8 étapes**

Le CDC est le document de référence du projet. Il engage les deux parties. Sa rédaction suit une logique précise, de l'état des lieux jusqu'au budget.

| N° | Section | Contenu attendu |
| :---- | :---- | :---- |
| **1** | **État actuel** | Décrire la situation existante : outils en place, processus actuels, problèmes identifiés. C'est la baseline. Sans elle, on ne peut pas mesurer le progrès. |
| **2** | **Objectifs du projet** | Pourquoi ce projet existe. Objectifs SMART : Spécifiques, Mesurables, Atteignables, Réalistes, Temporels. |
| **3** | **Périmètre** | Ce qui est INCLUS et ce qui est EXCLU. Définir les limites évite le scope creep dès le départ. |
| **4** | **Spécifications fonctionnelles** | Ce que le système doit faire du point de vue utilisateur. Fonctionnalités, parcours, cas d'usage. |
| **5** | **Spécifications techniques** | Comment c'est construit : technologies, hébergement, intégrations, performances attendues. |
| **6** | **Ressources** | Humaines (équipe interne \+ prestataires), matérielles, logicielles, informationnelles. |
| **7** | **Délais** | Planning macro : jalons clés, dates de rendu, date de livraison finale. |
| **8** | **Budget** | Enveloppe globale, répartition par poste, conditions de facturation. |

| 💡 Conseil de rédaction CDC Toujours commencer par l'état actuel — on ne comprend pas un besoin sans comprendre le contexte. Les spécifications fonctionnelles avant les techniques : 'quoi' avant 'comment'. Chaque objectif doit être mesurable — sinon c'est un vœu, pas un objectif. La section 'hors périmètre' est aussi importante que 'périmètre' : elle évite les malentendus. |
| :---- |

## **2.3 MOA / MOE**

| Maîtrise d'Ouvrage (MOA) vs Maîtrise d'Œuvre (MOE) |  |
| ----- | :---- |
| **Concept** | MOA \= le client (définit le besoin, valide, paye). MOE \= le réalisateur (conçoit, construit, livre). Comme en BTP : MOA \= propriétaire, MOE \= architecte \+ entreprise. |
| **Objectif** | Clarifier qui décide et qui fait — la confusion entre ces rôles est l'une des premières causes d'échec. |
| **Résultat Attendu** | Responsabilités claires, pas de doublon dans la prise de décision. |
| **Points Clés** | La MOA valide le cahier des charges et la recette finale. La MOE propose les solutions techniques et s'engage sur délais/coûts. Un CDP peut être côté MOA ou côté MOE selon son employeur. |
| **Erreurs À éviter** | Laisser la MOE décider des priorités fonctionnelles — c'est le rôle de la MOA. MOA absente pendant la réalisation → désaccord garanti en recette. Ne pas formaliser le bon de commande entre les deux parties. |
| **Exemple Concret** | Agence web (MOE) réalise le site d'une coutellerie artisanale (MOA). L'artisan valide maquettes et contenus. L'agence propose les solutions CMS et hébergement. |

## **2.4 Le Scope Creep**

| Scope Creep — La dérive des exigences |  |
| ----- | :---- |
| **Concept** | Extension non contrôlée du périmètre par ajouts successifs de petites demandes hors contrat. Chaque ajout semble anodin, mais l'accumulation dérègle planning et budget. |
| **Objectif** | Protéger le périmètre défini dans le CDC et maintenir la rentabilité du projet. |
| **Résultat Attendu** | Projet livré dans les délais et le budget initiaux, sans perte de marge. |
| **Points Clés** | Tout changement de périmètre \= Change Request formel avec impact chiffré (temps \+ coût). Documenter précisément le périmètre initial dans le CDC — ce qui n'est pas dedans n'existe pas. Dire non n'est pas un échec — c'est du pilotage responsable. |
| **Erreurs À éviter** | Accepter verbalement des demandes 'juste une petite chose' sans les chiffrer. Pas de processus de validation des modifications en place. Vouloir satisfaire tout le monde sans renégocier les ressources. |
| **Exempleconcret** | Site vitrine 5 pages. En cours de projet : le client demande un blog, une boutique et un espace membre. Sans gestion du scope : \+30% de charge non facturée. |

## **2.5 L'étude d'opportunité**

| Étude d'opportunité — GO ou NO-GO |  |
| ----- | :---- |
| **Concept** | Avant même de lancer le projet, on vérifie qu'il mérite d'exister : pourquoi ce projet ? Quels bénéfices ? Pour quel coût ? Quels risques ? |
| **Objectif** | Éviter de lancer un projet inutile, sous-financé ou voué à l'échec dès le départ. |
| **Résultat Attendu** | Décision formelle GO / NO-GO avec justification documentée. |
| **Points Clés** | Présenter les objectifs business (pas techniques). Quantifier les bénéfices attendus autant que possible. Analyser honnêtement les coûts et les risques — pas de biais optimiste. |
| **Erreurs À éviter** | Sauter cette étape pour 'gagner du temps' → on perd le double plus tard. Projections de bénéfices trop optimistes pour faire valider un projet déjà décidé. Ignorer les risques pour ne pas bloquer le lancement. |
| **Exemple Concret** | E-commerce B2B (budget 80k€) : étude révèle que 3 clients représentent 90% du CA et achètent déjà par téléphone. ROI insuffisant. Projet abandonné. 80k€ économisés. |

# **MODULE 3 — ACTEURS & ORGANISATION**

## **3.1 Cartographie des acteurs**

| Acteur | Rôle principal | Erreur fréquente |
| :---- | :---- | :---- |
| **Direction** | Valide, finance, arbitre les conflits de priorités | Absente jusqu'à la recette finale |
| **Chef de projet** | Pilote, coordonne, gère objectifs et risques | Faire à la place de l'équipe plutôt que piloter |
| **Équipe projet** | Développe, design, teste, intègre | Travailler en silo sans remonter les blocages |
| **Parties prenantes** | Influencent le projet sans en faire partie (clients, prestataires, utilisateurs…) | Ne pas les impliquer → mauvaises surprises en recette |

## **3.2 Culture projet vs Culture produit**

| Briser les silos — Passer à la culture projet |  |
| ----- | :---- |
| **Concept** | Culture produit \= chacun dans sa spécialité, sans vision d'ensemble (silos). Culture projet \= toute l'équipe partage les mêmes objectifs et s'implique sur le résultat global. |
| **Objectif** | Créer une équipe orientée résultat plutôt qu'orientée tâche individuelle. |
| **Résultat Attendu** | Meilleure communication, décisions plus rapides, moins de travail refait. |
| **Points Clés** | En culture projet, le dev comprend le besoin client, le designer comprend les contraintes tech. Les rituels de synchronisation (daily, weekly) cassent les silos. Le CDP est le garant de cette culture transversale. |
| **Erreurs À éviter** | Équipes techniques qui ne savent jamais à quoi sert ce qu'elles produisent. Réunions sans ordre du jour → retour à la culture silo. Évaluer les gens uniquement sur leur performance individuelle. |
| **Exemple Concret** | L'intégrateur découvre en livraison que les maquettes ne respectent pas les contraintes du CMS. Résultat : 3 jours de retard. Avec culture projet, ce point est adressé semaine 1\. |

# **MODULE 4 — CYCLE DE VIE D'UN PROJET**

## **4.1 Les grandes phases**

Tout projet passe par les mêmes grandes phases, quelle que soit la méthode. La méthode détermine comment on traverse ces phases, pas leur existence.

| Phase | Nom | Activités principales | Livrable clé |
| :---- | :---- | :---- | :---- |
| **1** | **Initialisation** | Étude d'opportunité, lettre de mission, charte projet | GO / NO-GO documenté |
| **2** | **Cadrage** | Note de cadrage, CDC, identification des acteurs | CDC validé par MOA \+ MOE |
| **3** | **Planification** | WBS, PERT, Gantt, plan de com, gestion des risques | Planning opérationnel validé |
| **4** | **Lancement (Kick-off)** | Présentation à l'équipe, validation collective du plan | Équipe alignée et opérationnelle |
| **5** | **Réalisation** | Production, développement, design, tests | Livrables intermédiaires validés |
| **6** | **Pilotage** | Comitologie, suivi KPIs, gestion des risques en continu | Écarts identifiés et traités |
| **7** | **Recette** | Validation par la MOA des livrables finaux | PV de recette signé |
| **8** | **Déploiement** | Mise en production, formation, passage de main | Produit opérationnel en production |
| **9** | **Clôture** | Bilan projet, retour d'expérience, archivage | Documentation finale \+ retex |

## **4.2 Le Kick-off — Bien lancer un projet**

| Le Kick-off — La réunion de lancement |  |
| ----- | :---- |
| **Concept** | Réunion officielle qui marque le démarrage opérationnel du projet. Tout le monde est là, tout le monde repart avec la même compréhension du projet, de son rôle et du planning. |
| **Objectif** | Aligner toutes les parties prenantes dès le départ et créer un engagement collectif. |
| **Résultat Attendu** | Équipe mobilisée, rôles clairs, planning partagé, risques connus de tous. |
| **Points Clés** | Présenter le projet : pourquoi il existe, quels objectifs, pour qui. Partager le périmètre : ce qu'on fait, ce qu'on ne fait pas. Clarifier les rôles et responsabilités de chaque participant. Présenter le planning macro et les jalons clés. Ouvrir la parole sur les risques identifiés et les questions. |
| **Erreurs À éviter** | Kick-off sans agenda préparé → réunion floue, pas d'engagement. Inviter trop de monde : dilution des responsabilités. Ne pas produire de compte-rendu : la réunion n'a jamais eu lieu officiellement. Faire le kick-off avant que le CDC soit validé — on lance sans base solide. |
| **Exemple Concret** | Refonte site coutellerie : kick-off en présentiel avec l'artisan (MOA), le CDP, le lead dev et le designer (MOE). 1h30. Livrable : CR envoyé sous 48h, planning partagé sur Notion. |

# **MODULE 5 — PLANIFICATION & ORDONNANCEMENT**

## **5.1 Les types de planning**

| Type | Description | Granularité | Audience |
| :---- | :---- | :---- | :---- |
| **Planning directeur** | Vision macro, jalons clés uniquement | Mois | Direction, COPIL |
| **Macroplanning** | Étapes principales \+ dates début/fin. Tient sur 1 A4. | Semaines | Parties prenantes |
| **Rétro-planning** | On part de la date butoir et on remonte. Challenge la faisabilité. | Jours | CDP \+ équipe |
| **Planning détaillé** | Toutes les tâches, dépendances, ressources. Suivi quotidien. | Jours / h | Équipe projet |
| **Diagramme de Gantt** | Représentation visuelle des tâches dans le temps avec dépendances. | Jours / h | Équipe \+ MOA |

## **5.2 WBS, PERT et Gantt**

| WBS — Décomposer avant de planifier |  |
| ----- | :---- |
| **Concept** | Le WBS décompose le projet en couches : Produit final → Sous-livrables → Tâches → Sous-tâches. On répond à QUOI faire avant de répondre QUAND. C'est la fondation du planning. |
| **Objectif** | S'assurer qu'on n'oublie rien et que chaque tâche a un responsable avant de planifier. |
| **Résultat Attendu** | Liste exhaustive de tout ce qui doit être produit, avec attribution claire. |
| **Points Clés** | Construire le WBS AVANT le Gantt — sinon on planifie des oublis. Chaque élément terminal doit être assigné à une personne précise. Inclure les livrables de gestion : réunions, reporting, comités, recette. |
| **Erreurs À éviter** | Commencer à planifier sans avoir listé tous les livrables. WBS trop haut niveau : les tâches oubliées apparaissent en cours de projet. Ne pas inclure les tâches 'invisibles' (tests, formation, documentation). |
| **Exemple Concret** | Projet site coutellerie : Design (maquettes \+ charte) \+ Dev (intégration \+ CMS \+ formulaires) \+ Contenu (textes SEO \+ photos) \+ Lancement (mise en prod \+ tests \+ formation client). |

| PERT — Identifier le chemin critique |  |
| ----- | :---- |
| **Concept** | Le PERT visualise les dépendances entre tâches et calcule le chemin critique : la séquence de tâches la plus longue qui détermine la durée totale. Toute tâche sur le chemin critique retardée \= projet retardé. |
| **Objectif** | Identifier les tâches bloquantes et les marges de manœuvre disponibles. |
| **Résultat Attendu** | Chemin critique connu, ressources concentrées sur les tâches critiques. |
| **Points Clés** | Étape 1 : identifier les dépendances. Étape 2 : ordonnancer. Étape 3 : calculer le chemin critique. Les tâches hors chemin critique ont de la 'marge' — on peut les décaler sans impact. Recalculer le chemin critique dès qu'une tâche prend du retard. |
| **Erreurs À éviter** | Oublier des dépendances → chemin critique faussé. Ne pas recalculer en cours de projet. Ignorer les tâches à marge zéro — une seule suffit à tout bloquer. |
| **Exemple Concret** | Site web : back-end (10j) et contenu (7j) en parallèle, intégration (5j) dépend des deux. Chemin critique \= 10j \+ 5j \= 15j. Le contenu a 3j de marge. |

| Gantt — Piloter l'avancement quotidien |  |
| ----- | :---- |
| **Concept** | Représentation visuelle de toutes les tâches dans le temps, avec durées, dépendances et ressources. Outil de pilotage quotidien du CDP. C'est la carte du projet à jour. |
| **Objectif** | Détecter les dérives tôt et communiquer l'avancement à toutes les parties prenantes. |
| **Résultat Attendu** | Tableau de bord visuel partageable, écarts détectés en temps quasi-réel. |
| **Points Clés** | Mise à jour hebdomadaire minimum — un Gantt périmé est pire que pas de Gantt. Inclure : tâche, date début, durée, responsable, dépendances, % avancement. Outils : Gantt Project (gratuit), ClickUp, Monday, Notion. |
| **Erreurs À éviter** | Gantt trop détaillé dès le départ → obsolète en 48h. Ne pas partager le Gantt avec l'équipe. Le considérer comme figé — il doit vivre avec le projet. |
| **Exemple Concret** | Refonte 3 mois : S1-2 cadrage, S3-5 design, S6-10 dev, S11 tests, S12 formation \+ déploiement. Chaque barre colorée par responsable. Partagé sur ClickUp. |

# **MODULE 6 — GESTION DES PRIORITÉS**

## **6.1 MoSCoW**

| MoSCoW — Prioriser les fonctionnalités |  |
| ----- | :---- |
| **Concept** | Classe chaque fonctionnalité en 4 catégories : Must have (indispensable), Should have (important), Could have (confort), Won't have (hors périmètre maintenant). |
| **Objectif** | Décider collectivement quoi livrer en priorité quand le temps ou le budget est limité. |
| **Résultat Attendu** | Liste de fonctionnalités triée, défendable devant le client, actionnables par l'équipe. |
| **Points Clés** | Les 'Must have' seuls doivent permettre au produit d'exister et d'être utile. Impliquer le client dans la classification — le CDP ne décide pas seul. Les 'Won't have' ne sont pas des refus définitifs : 'pas maintenant'. |
| **Erreurs À éviter** | 80% en 'Must have' → ça ne priorise rien. Ne pas revisiter les priorités entre chaque phase. Confondre 'Could have' et 'Should have' — dans le doute, déclasser. |
| **Exemple Concret** | Site artisan : Must \= catalogue \+ contact \+ responsive. Should \= galerie photos. Could \= blog. Won't \= e-commerce (phase 2). |

## **6.2 Matrice Eisenhower**

| Matrice Eisenhower — Urgent vs Important |  |
| ----- | :---- |
| **Concept** | Classe les tâches sur 2 axes : Urgent/Non urgent × Important/Non important. 4 quadrants, 4 actions différentes. |
| **Objectif** | Éviter de passer sa journée sur des urgences peu importantes au détriment du travail stratégique. |
| **Résultat Attendu** | Semaine mieux structurée, tâches stratégiques réellement avancées. |
| **Points Clés** | Q1 (Urgent \+ Important) : Faire maintenant. Q2 (Non urgent \+ Important) : Planifier — c'est là que se joue la performance réelle. Q3 (Urgent \+ Non important) : Déléguer. Q4 (Non urgent \+ Non important) : Éliminer. |
| **Erreurs À éviter** | Passer ses journées en Q1 et Q3 → jamais de temps pour le Q2 stratégique. Confondre urgence et importance. Utiliser la matrice comme outil de reporting plutôt que de décision. |
| **Exempleconcret** | Bug client signalé (Q1 → now). Préparation audit mensuel (Q2 → planifier mardi). Répondre aux CC (Q3 → déléguer). Refaire la déco du bureau (Q4 → supprimer). |

# **MODULE 7 — COMITOLOGIE & PILOTAGE**

## **7.1 Les instances de gouvernance**

| Comitologie — Structurer les réunions de gouvernance |  |
| ----- | :---- |
| **Concept** | 3 niveaux de réunions projet : stratégique (COPIL), opérationnel (COPROJ), terrain (COSUIVI). Chaque niveau a sa fréquence, ses participants et ses types de décisions. |
| **Objectif** | Les bonnes personnes, au bon niveau, avec les bonnes infos, pour prendre les bonnes décisions. |
| **Résultat Attendu** | Décisions fluides, pas de réunion inutile, visibilité à tous les niveaux. |
| **Points Clés** | COPIL : décisions stratégiques, arbitrages budget. Sponsors \+ direction. Fréquence : mensuelle. COPROJ : avancement opérationnel, points bloquants. CDP \+ chefs d'équipe. Fréquence : hebdo. COSUIVI : pilotage terrain, quotidien ou bi-hebdo. CDP \+ équipe. Chaque réunion doit avoir : un ordre du jour, un animateur, un Compte Rendu sous 48h. |
| **Erreurs À éviter** | Inviter tout le monde à tout → dilution des décisions. COPIL sans livrable à valider → réunion narrative sans impact. Confondre les niveaux : les décisions stratégiques ne se prennent pas en COSUIVI. |
| **Exemple Concret** | E-commerce : COPIL mensuel avec le DG pour jalons et budget. COPROJ hebdo CDP \+ lead dev \+ lead design. Daily 15 min avec l'équipe pour les blocages. |

# **MODULE 8 — GESTION DES RISQUES**

## **8.1 Le processus complet**

Un risque \= événement incertain qui peut impacter négativement le projet. La gestion des risques est un processus CONTINU, pas une case à cocher au démarrage.

| Les 5 étapes de gestion des risques |  |
| ----- | :---- |
| **Concept** | Identifier → Analyser (probabilité × impact) → Prioriser → Traiter → Surveiller. On ne peut pas éliminer tous les risques. On les réduit, transfère ou assume. |
| **Objectif** | Anticiper les problèmes plutôt que les subir, et avoir un plan B prêt pour les risques critiques. |
| **Résultat Attendu** | Registre des risques vivant, plans de contingence documentés, alertes au bon niveau. |
| **Points Clés** | Score \= Probabilité (1-5) × Impact (1-5). Seuls les scores élevés méritent un plan d'action détaillé. 4 stratégies de traitement : Éviter, Réduire, Transférer, Accepter. Le registre des risques doit être mis à jour à chaque COPROJ. Impliquer l'équipe dans l'identification — les risques techniques remontent rarement seuls. |
| **Erreurs À éviter** | Identifier les risques une seule fois au démarrage et ne plus y revenir. Registre des risques \= document décoratif. Confondre risque et problème : le risque est potentiel, le problème est réel. |
| **Exemple Concret** | Risque : client livre les contenus avec 3 semaines de retard (probabilité 4/5, impact 4/5 \= score 16 \= critique). Traitement : clause contractuelle sur délais \+ placeholder content pour ne pas bloquer le dev. |

## **8.2 La matrice probabilité × impact**

Lecture : Probabilité en ligne × Impact en colonne \= Score de criticité

| Proba \\ Impact | Faible (1) | Moyen (2) | Fort (4) | Critique (8) |
| :---: | :---: | :---: | :---: | :---: |
| **Rare (1)** | 1 ✅ | 2 ✅ | 4 🟡 | 8 🟠 |
| **Possible (2)** | 2 ✅ | 4 🟡 | 8 🟠 | 16 🔴 |
| **Probable (4)** | 4 🟡 | 8 🟠 | 16 🔴 | **32 🔴** |
| **Quasi-certain (8)** | 8 🟠 | 16 🔴 | **32 🔴** | **64 ⛔** |

| Lecture de la matrice Score 1-4 (vert ✅) : Risque faible. Surveiller, pas d'action urgente. Score 8 (orange 🟠) : Risque modéré. Plan de réduction à prévoir. Score 16+ (rouge 🔴) : Risque critique. Plan d'action immédiat requis. Score 32+ (⛔) : Risque majeur. Remonter au COPIL, envisager modification de conception. |
| :---- |

## **8.3 Les 4 stratégies de traitement**

| Stratégie | Principe | Exemple concret |
| :---- | :---- | :---- |
| **Éviter** | Modifier la conception pour que le risque n'existe plus | Risque : technologie non maîtrisée.  Action : choisir une techno connue de l'équipe. |
| **Réduire** | Prendre des mesures préventives pour diminuer probabilité ou impact | Risque : retard contenu client.  Action : clause contractuelle \+ planning de livraison co-signé. |
| **Transférer** | Déléguer le risque à un tiers (prestataire, assurance) | Risque : panne serveur.  Action : hébergement infogéré avec SLA et garantie de disponibilité. |
| **Accepter** | Assumer le risque résiduel, sans action préventive | Risque : légère pluie le jour d'un événement en extérieur. Impact faible, rien à faire. |

# **MODULE 9 — RGPD & CONFORMITÉ**

## **9.1 Les fondamentaux**

| RGPD — 3 principes, 6 obligations |  |
| ----- | :---- |
| **Concept** | Règlement en vigueur depuis mai 2018 qui encadre la collecte et l'utilisation des données personnelles des citoyens EU. 3 principes directeurs : responsabilité, confiance, transparence. |
| **Objectif** | Protéger les droits des individus sur leurs données et imposer une gestion loyale et sécurisée. |
| **Résultat Attendu** | Conformité légale, confiance utilisateurs, évitement des sanctions CNIL (jusqu'à 4% du CA mondial). |
| **Points Clés** | Donnée personnelle \= toute info permettant d'identifier directement ou indirectement (nom, email, IP, cookie…). 6 principes : licéité \+ loyauté \+ transparence / limitation des finalités / minimisation / exactitude / limitation conservation / sécurité. Tout traitement doit avoir une base légale : consentement, contrat, obligation légale ou intérêt légitime. Droits des personnes : accès, rectification, effacement, portabilité, opposition. |
| **Erreurs À éviter** | Penser que le RGPD ne concerne que les grandes entreprises. Collecter des données 'au cas où' sans finalité définie à l'avance. Politique de confidentialité copiée-collée sans adaptation. |
| **Exemple Concret** | Formulaire contact artisan : collecte nom \+ email. Base légale \= intérêt légitime. À mentionner : durée de conservation 3 ans, droit de suppression, pas de revente. |

| Document légal | Contenu attendu |
| :---- | :---- |
| **Politique de confidentialité** | Données collectées, finalité, durée de conservation, droits des utilisateurs |
| **Mentions légales** | Identité de l'éditeur, hébergeur, directeur de publication |
| **Politique de cookies** | Types de cookies, durée, opt-in/opt-out obligatoire |
| **CGV / CGU** | Conditions générales de vente ou d'utilisation |
| **Informations sur les prix** | Obligatoires pour tout e-commerce |
| **Droit de rétractation** | 14 jours pour les achats en ligne (B2C) |

# **MODULE 10 — LE CYCLE COMPLET D'UN PROJET DIGITAL**

*Pour chaque étape : qui intervient, quels outils, quel objectif, quel livrable, et l'erreur la plus fréquente.*

| 1\. Étude d'opportunité   *→  Décider si le projet mérite d'exister — GO ou NO-GO* |  |  |
| :---- | :---- | ----- |
| **Acteurs** | Direction, sponsor, éventuellement le CDP |  |
| **Outils** | Business case, analyse coûts/bénéfices, SWOT |  |
| **Livrable** | Document de décision GO / NO-GO signé par la direction |  |
| **⚠️ Erreur** | Présenter uniquement les bénéfices et ignorer les risques pour forcer le GO |  |

| 2\. Initialisation & Cadrage   *→  Poser les bases du projet et formaliser les engagements* |  |  |
| :---- | :---- | ----- |
| **Acteurs** | CDP, MOA, MOE, direction |  |
| **Outils** | Lettre de mission, charte projet, note de cadrage, étude d'opportunité |  |
| **Livrable** | Cahier des charges validé et signé par MOA \+ MOE |  |
| **⚠️ Erreur** | Commencer à planifier avant que le CDC soit validé — on construit sur du sable |  |

| 3\. Planification   *→  Définir précisément quoi faire, quand, qui et avec quoi* |  |  |
| :---- | :---- | ----- |
| **Acteurs** | CDP, chefs d'équipe, équipe projet |  |
| **Outils** | WBS, PERT, Gantt, registre des risques, plan de communication, MoSCoW |  |
| **Livrable** | Planning opérationnel validé \+ registre des risques initial \+ plan com |  |
| **⚠️ Erreur** | Sauter le WBS et aller directement au Gantt — on planifie des oublis |  |

| 4\. Kick-off   *→  Aligner toute l'équipe et créer l'engagement collectif* |  |  |
| :---- | :---- | ----- |
| **Acteurs** | CDP, MOA, toute l'équipe projet, parties prenantes clés |  |
| **Outils** | Présentation projet, planning macro, rôles & responsabilités, RACI |  |
| **Livrable** | Compte-rendu de kick-off \+ planning partagé \+ contacts de l'équipe |  |
| **⚠️ Erreur** | Faire le kick-off sans CR → la réunion n'existe pas officiellement |  |

| 5\. Réalisation   *→  Produire les livrables dans le respect du CDC et du planning* |  |  |
| :---- | :---- | ----- |
| **Acteurs** | Équipe projet (dev, design, contenu), CDP en coordination |  |
| **Outils** | Trello / Jira / ClickUp, Gantt, outils métier (Figma, VS Code…) |  |
| **Livrable** | Livrables intermédiaires validés à chaque jalons, PV de validation |  |
| **⚠️ Erreur** | CDP qui fait à la place de l'équipe au lieu de débloquer les situations |  |

| 6\. Pilotage continu   *→  Détecter les dérives tôt et prendre les décisions d'arbitrage* |  |  |
| :---- | :---- | ----- |
| **Acteurs** | CDP (coordinateur), COPIL (décisions stratégiques), COPROJ (décisions opéra.) |  |
| **Outils** | Tableau de bord KPIs, Gantt mis à jour, registre des risques, CR de réunions |  |
| **Livrable** | Reporting hebdomadaire, comptes-rendus COPIL/COPROJ, alertes arbitrées |  |
| **⚠️ Erreur** | Attendre que le problème soit visible de tous pour le signaler — trop tard |  |

| 7\. Recette   *→  Vérifier que le livrable final correspond au CDC et le faire valider par la MOA* |  |  |
| :---- | :---- | ----- |
| **Acteurs** | MOA (valide), CDP (coordonne), équipe projet (corrections) |  |
| **Outils** | Grille de recette, cahier de tests, protocole de recette |  |
| **Livrable** | PV de recette signé par la MOA — c'est la validation officielle |  |
| **⚠️ Erreur** | Recette bâclée sous pression délai → bugs découverts en production |  |

| 8\. Déploiement & Formation   *→  Mettre le livrable en production et s'assurer que les utilisateurs savent s'en servir* |  |  |
| :---- | :---- | ----- |
| **Acteurs** | CDP, équipe technique (déploiement), utilisateurs finaux (formation) |  |
| **Outils** | Plan de déploiement, support de formation, guide utilisateur, plan de rollback |  |
| **Livrable** | Produit opérationnel en production \+ utilisateurs formés \+ documentation |  |
| **⚠️ Erreur** | Déployer un vendredi soir sans plan de rollback — personne disponible pour corriger |  |

| 9\. Clôture & Amélioration continue   *→  Capitaliser sur l'expérience du projet pour s'améliorer* |  |  |
| :---- | :---- | ----- |
| **Acteurs** | CDP, équipe projet, MOA |  |
| **Outils** | Rétrospective (PDCA, 5 pourquoi), bilan projet, archivage documentation |  |
| **Livrable** | Bilan projet documenté \+ retex partagé \+ améliorations process identifiées |  |
| **⚠️ Erreur** | Passer directement au projet suivant sans bilan → on répète les mêmes erreurs |  |

# **CHEATSHEET — À EMPORTER PARTOUT**

| ⚡ Les 10 erreurs les plus fréquentes 1\.  Lancer sans étude d'opportunité sérieuse 2\.  Périmètre flou dans le CDC → scope creep garanti 3\.  MOA absente pendant la réalisation 4\.  WBS inexistant → tâches oubliées découvertes trop tard 5\.  Gantt créé et jamais mis à jour 6\.  Comitologie inexistante → décisions informelles non tracées 7\.  Registre des risques figé après la phase de cadrage 8\.  MoSCoW avec 80% en Must Have → pas de priorisation réelle 9\.  RGPD traité comme une case juridique à cocher 10\. Fin de projet sans bilan → on répète les mêmes erreurs |
| :---- |

| 🛠️ Outils recommandés par usage Planning / Gantt     →  ClickUp, Monday, GanttProject (gratuit) WBS                  →  Miro, FigJam, XMind Kanban / Suivi       →  Trello, Jira, Linear, Notion Documents cadrage    →  Notion, Confluence, Google Docs Gestion des risques  →  Tableau dédié Excel ou outil PM intégré Reporting KPIs       →  Looker Studio, Klipfolio, Excel Prototypage          →  Figma, Adobe XD Communication équipe →  Slack, Teams, Notion |
| :---- |

| 📏 Les questions à se poser à chaque étape Initialisation  : Pourquoi ce projet existe ? Qui le finance ? Qui décide ? Cadrage         : Qu'est-ce qui est DANS le périmètre ? Qu'est-ce qui est HORS périmètre ? Planification   : Ai-je listé TOUS les livrables avant de planifier ? Kick-off        : Est-ce que TOUT LE MONDE repart avec la même compréhension ? Réalisation     : Suis-je en train de piloter ou de faire à la place de mon équipe ? Pilotage        : Y a-t-il des signaux faibles que je sous-estime ? Recette         : Le client a-t-il validé formellement, ou juste dit 'c'est bien' ? Déploiement     : Ai-je un plan de rollback si ça tourne mal ? Clôture         : Qu'est-ce que j'aurais fait différemment ? |
| :---- |

