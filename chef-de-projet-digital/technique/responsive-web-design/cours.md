  
**RESPONSIVE WEB DESIGN**

Le guide du Chef de Projet Digital

*Comprendre, arbitrer, challenger les choix techniques*

Bachelor Chef de Projet Digital

Avril 2026

# **1\. Le Responsive Web Design : de quoi parle-t-on ?**

## **Définition**

Le Responsive Web Design (RWD) est une approche de conception web où le site s’adapte automatiquement à la taille de l’écran de l’appareil utilisé — smartphone, tablette, ordinateur portable ou écran large. Le contenu, la navigation et la mise en page se réorganisent de manière fluide pour offrir la meilleure expérience possible à chaque utilisateur.

Concrètement, un site responsive utilise une seule base de code HTML, stylisée avec du CSS qui s’adapte selon les conditions d’affichage. C’est l’opposé de créer un site mobile séparé (m.monsite.com), une pratique obsolète.

## **Pourquoi c’est un sujet CDP ?**

En tant que chef de projet digital, tu ne codes pas le responsive toi-même. Mais tu dois :

* Rédiger des spécifications techniques qui précisent le comportement du site sur chaque taille d’écran.

* Valider les maquettes en vérifiant que le designer a prévu les vues mobile, tablette et desktop.

* Challenger les choix du développeur : pourquoi tel breakpoint ? Pourquoi pas du mobile first ?

* Recetter le livrable en testant sur différents appareils et en identifiant les problèmes.

* Argumenter auprès du client quand il demande « pourquoi ça ne ressemble pas au desktop sur mon téléphone ».

| ℹ | Le RWD et le SEO Google utilise l’indexation mobile-first depuis 2019\. Cela signifie que c’est la version mobile de votre site qui est analysée en priorité pour le référencement. Un site non responsive est directement pénalisé dans les résultats de recherche. |
| :---- | :---- |

# **2\. Les types de layout**

Avant de parler de responsive, il faut comprendre les quatre grands types de mise en page (layout) qui existent en web design.

## **Layout fixe (Fixed)**

**Définition**

La page a une largeur fixe en pixels (par exemple 960px). Quel que soit l’écran, le contenu ne bouge pas. Sur un écran plus petit, une barre de défilement horizontale apparaît. Sur un écran plus grand, des marges vides s’affichent.

**À quoi ça sert**

Quasi plus utilisé aujourd’hui. On le retrouve parfois sur des applications internes (intranet) où tous les postes ont le même écran.

**Erreur à éviter**

Accepter une maquette en layout fixe pour un site public. C’est rédhibitoire pour le SEO et l’UX mobile.

## **Layout fluide (Fluid)**

**Définition**

Les éléments sont dimensionnés en pourcentages plutôt qu’en pixels. Le contenu s’étire ou se rétrécit proportionnellement à la taille de la fenêtre.

**À quoi ça sert**

C’est la base du responsive. Un conteneur à 80% de largeur s’adaptera naturellement. Mais attention : sans règles supplémentaires, le texte peut devenir illisible sur très petit ou très grand écran.

**Erreur à éviter**

Faire du 100% fluide sans contraintes (min-width / max-width). Une colonne de texte qui s’étire sur 1920px de large est illisible.

## **Layout adaptatif (Adaptive)**

**Définition**

Le site détecte la taille de l’écran et charge un layout spécifique parmi plusieurs versions prédéfinies (par exemple : une version 480px, une version 768px, une version 1024px). Entre deux seuils, le layout ne change pas.

**À quoi ça sert**

Utilisé quand on veut un contrôle très précis du rendu sur certains appareils clés, ou quand on ajoute du responsive à un vieux site sans tout recoder.

**Erreur à éviter**

Confondre adaptatif et responsive. L’adaptatif « saute » d’un layout à l’autre. Le responsive s’adapte de manière fluide et continue.

## **Layout responsif (Responsive)**

**Définition**

C’est la combinaison du layout fluide et de media queries. Le contenu s’adapte de manière continue ET se réorganise à certains seuils (breakpoints). C’est le standard actuel du web design.

**À quoi ça sert**

Tous les sites modernes. C’est ce que Google attend, ce que les utilisateurs attendent, et ce que le cahier des charges doit spécifier.

| Type | Comportement | Usage actuel |
| :---- | :---- | :---- |
| Fixe | Largeur figée en pixels | Obsolète (sauf intranet) |
| Fluide | Éléments en % — étirement proportionnel | Base du responsive |
| Adaptatif | Plusieurs layouts fixes selon des seuils | Refonte partielle de vieux sites |
| Responsif | Fluide \+ media queries \+ breakpoints | Standard actuel |

# **3\. Les approches de conception**

## **Mobile First**

**Définition**

On conçoit d’abord la version mobile du site, puis on enrichit progressivement le design pour les écrans plus grands. C’est le principe d’amélioration progressive (progressive enhancement).

**Pourquoi c’est important**

Plus de 60% du trafic web mondial vient du mobile. Commencer par le mobile force à prioriser le contenu essentiel et à optimiser les performances (images légères, navigation simplifiée). C’est aussi ce que Google préfère pour le SEO.

**Concrètement en CSS**

Le développeur écrit les styles de base pour le mobile, puis ajoute des media queries avec min-width pour enrichir le design sur les écrans plus larges.

**Erreur à éviter**

Demander au designer de livrer uniquement la maquette desktop en disant « on verra le mobile après ». Le mobile n’est pas une adaptation du desktop : c’est un design à part entière avec ses propres contraintes.

## **Desktop First**

**Définition**

On conçoit d’abord la version desktop, puis on simplifie pour les écrans plus petits (dégradation gracieuse). Le développeur utilise des media queries avec max-width.

**Quand l’utiliser**

Légitime uniquement quand l’audience est majoritairement sur ordinateur (ex : outils SaaS B2B, logiciels métier, back-offices). Vérifier les statistiques analytics avant de choisir.

**Erreur à éviter**

Choisir desktop first par habitude alors que les analytics montrent 70% de trafic mobile. Le choix de l’approche est une décision stratégique, pas un réflexe technique.

## **Content First**

**Définition**

Le design est conçu autour du contenu réel (textes, images, vidéos) et non l’inverse. On ne crée pas des « boîtes » qu’on remplit ensuite avec du Lorem Ipsum.

**Pourquoi c’est important**

Un design construit sur du faux contenu produit des mises en page qui cassent dès que le vrai contenu arrive : titres trop longs, images au mauvais ratio, blocs déséquilibrés. Content first évite les allées et venues en production.

**Erreur à éviter**

Valider une maquette entièrement remplie de Lorem Ipsum. En tant que CDP, exiger les contenus réels (ou au minimum réalistes) avant la validation du design.

| ✓ | Règle CDP Dans le cahier des charges ou le brief créatif, préciser systématiquement l’approche retenue (mobile first / desktop first) et exiger les maquettes sur au moins 3 formats : mobile (375px), tablette (768px), desktop (1440px). |
| :---- | :---- |

# **4\. Les points de rupture (breakpoints)**

## **Définition**

Les points de rupture (breakpoints) sont les seuils de largeur d’écran à partir desquels le design se réorganise. Par exemple, à 768px, on peut passer d’un menu horizontal à un menu burger, ou d’un affichage en 3 colonnes à 1 colonne.

## **Les seuils classiques**

| Largeur | Appareil type | Usage |
| :---- | :---- | :---- |
| \< 480px | Smartphone portrait | Contenu empilé, 1 colonne |
| 480px – 768px | Smartphone paysage / petite tablette | 2 colonnes possibles |
| 768px – 960px | Tablette / petit laptop | Layout intermédiaire |
| 960px – 1200px | Ordinateur portable | Layout desktop classique |
| \> 1200px | Écran large / moniteur | Layout étendu, max-width recommandé |

## **À quoi ça sert concrètement**

Les breakpoints dictent quand le layout change. En tant que CDP, tu retrouves ces valeurs dans les spécifications techniques et dans les fichiers CSS du développeur. Ils doivent correspondre aux formats de maquettes livrées par le designer.

## **Bonne pratique actuelle**

On ne choisit plus les breakpoints en fonction des appareils (iPhone 15, iPad Pro, etc.) mais en fonction du contenu. Le breakpoint se place là où le contenu commence à mal s’afficher. C’est ce qu’on appelle les content-aware breakpoints.

## **Erreurs à éviter**

* Fixer des breakpoints uniquement sur les tailles d’iPhone. Les appareils Android ont des tailles très variées.

* Oublier de tester entre les breakpoints (ex : à 650px, entre mobile et tablette).

* Multiplier les breakpoints inutilement. Trois à cinq suffisent dans la majorité des cas.

| ⚠ | Piège fréquent Le client teste sur son écran 27 pouces et dit « c’est parfait ». Mais 65% de ses visiteurs sont sur mobile. Toujours montrer les maquettes mobile en premier lors des présentations client. |
| :---- | :---- |

# **5\. Les unités CSS**

Les unités CSS sont au cœur du responsive. Comprendre la différence entre unités absolues et relatives est indispensable pour lire une maquette ou challenger un développeur.

## **Unités absolues**

Elles ne changent pas quelle que soit la taille de l’écran. La principale est le pixel (px).

**Quand les utiliser**

Pour les éléments graphiques qui ne doivent pas bouger : bordures (border: 1px), ombres (box-shadow), petits détails visuels. Jamais pour des largeurs de colonnes ou des tailles de police principales.

## **Unités relatives**

**Le pourcentage (%)**

**Définition :** Relatif au parent direct. Si un conteneur fait 1000px et qu’un élément enfant est à width: 50%, il fera 500px.

**Usage :** Largeurs de colonnes, layouts fluides. C’est la base de toute grille responsive.

**Le EM**

**Définition :** Relatif à la taille de police de l’élément parent. Si le parent a un font-size de 16px, 1em \= 16px, 2em \= 32px.

**Usage :** Marges et paddings de composants. L’avantage : si on change la taille de police du parent, tout le composant se redimensionne proportionnellement.

**Piège :** Les EM se cumulent. Un em dans un em dans un em donne des résultats imprévisibles. C’est pour ça que le REM existe.

**Le REM**

**Définition :** Relatif à la taille de police de la racine HTML (par défaut 16px dans tous les navigateurs). 1rem \= toujours 16px, quel que soit le niveau d’imbrication.

**Usage :** Les tailles de police (typographie). C’est l’unité de référence pour la typographie responsive. Permet aussi aux utilisateurs malvoyants de zoomer le texte via les paramètres de leur navigateur.

**VW et VH (Viewport Width / Height)**

**Définition :** Relatifs à la taille de la fenêtre du navigateur (viewport). 1vw \= 1% de la largeur de la fenêtre. 1vh \= 1% de sa hauteur.

**Usage :** Sections plein écran (hero sections en height: 100vh), typographie fluide qui grandit avec l’écran.

**Piège :** Sur mobile, la barre d’adresse du navigateur fait partie du viewport. Un élément en 100vh peut donc déborder sous la barre. Les développeurs utilisent dvh (dynamic viewport height) pour corriger ce problème.

## **Tableau récapitulatif**

| Unité | Référence | Usage principal |
| :---- | :---- | :---- |
| px | Absolue | Bordures, ombres, détails graphiques |
| % | Parent direct | Largeurs de colonnes, layouts fluides |
| em | Parent (police) | Marges/paddings de composants |
| rem | Racine HTML (16px) | Typographie, tailles de police |
| vw / vh | Fenêtre navigateur | Sections plein écran, typo fluide |
| fr | Espace disponible (Grid) | Colonnes de grilles CSS Grid |

# **6\. Les Media Queries**

## **Définition**

Les media queries sont des règles CSS qui permettent d’appliquer des styles sous certaines conditions. La condition la plus courante est la largeur de l’écran, mais on peut aussi cibler l’orientation (portrait/paysage), la résolution, ou le mode sombre.

## **Comment ça marche**

Le développeur écrit une règle du type : « si l’écran fait au moins 768px de large, alors applique ces styles ». Le navigateur vérifie la condition en temps réel et applique ou retire les styles en conséquence.

**Exemples**

@media (min-width: 768px) { ... } → Styles appliqués à partir de 768px (mobile first).

@media (max-width: 768px) { ... } → Styles appliqués en dessous de 768px (desktop first).

@media (orientation: landscape) { ... } → Styles appliqués quand l’écran est en mode paysage.

## **Ce que le CDP doit retenir**

* Les media queries sont le mécanisme technique qui rend le responsive possible. Sans elles, pas de changement de layout selon l’écran.

* Chaque breakpoint dans la maquette \= une media query dans le code.

* En mobile first, on utilise min-width (on ajoute des styles quand l’écran grandit). En desktop first, on utilise max-width (on retire des styles quand l’écran rétrécit).

## **Erreurs à éviter**

* Mélanger min-width et max-width dans un même projet sans logique. Choisir une approche et s’y tenir.

* Créer trop de media queries. Si le design en nécessite 15, c’est probablement un problème de conception, pas de code.

# **7\. Flexbox**

## **Définition**

Flexbox (Flexible Box Layout) est un modèle de mise en page CSS conçu pour organiser, aligner et distribuer des éléments dans un conteneur, sur un seul axe à la fois (horizontal OU vertical). C’est unidirectionnel.

## **Analogie pour comprendre**

Imagine une étagère. Flexbox te permet de disposer les objets sur cette étagère : les espacer régulièrement, les centrer, les coller à gauche ou à droite, ou les répartir de manière égale. Mais c’est une seule étagère (un seul axe). Si tu veux plusieurs rangées, il faut activer le retour à la ligne (flex-wrap).

## **Les propriétés clés à connaître**

| Propriété | Rôle | Exemple concret |
| :---- | :---- | :---- |
| display: flex | Active Flexbox sur le conteneur | Activer l’alignement des items d’un menu |
| flex-direction | Définit l’axe : row (ligne) ou column (colonne) | Menu horizontal (row) vs sidebar verticale (column) |
| justify-content | Alignement sur l’axe principal | Centrer un bouton, espacer des cards |
| align-items | Alignement sur l’axe secondaire | Centrer verticalement un logo à côté d’un texte |
| flex-wrap | Autorise le retour à la ligne | Grille de produits qui s’empile sur mobile |
| flex-grow | Capacité d’un élément à grandir | Un champ de recherche qui prend l’espace restant |
| flex-shrink | Capacité d’un élément à rétrécir | Empêcher une image de se comprimer |
| flex-basis | Taille de départ de l’élément | Définir la largeur initiale d’une card |

## **Quand utiliser Flexbox**

* Barres de navigation horizontales.

* Alignement d’éléments dans un header (logo \+ menu \+ CTA).

* Centrage vertical et horizontal de contenu.

* Distribution de cards sur une ligne avec retour à la ligne.

* Composants internes : boutons groupés, formulaires en ligne.

## **Erreurs à éviter**

* Utiliser Flexbox pour le layout global d’une page entière. C’est faisable mais CSS Grid est plus adapté.

* Imbriquer 5 niveaux de Flexbox les uns dans les autres. Le code devient inmaintenable.

# **8\. CSS Grid**

## **Définition**

CSS Grid Layout est un système de mise en page bidimensionnel : il gère à la fois les lignes et les colonnes simultanément. On définit une grille (comme un tableau invisible), puis on place les éléments dedans.

## **Analogie pour comprendre**

Si Flexbox est une étagère, CSS Grid est un plan d’architecte. Tu définis d’abord le quadrillage (combien de colonnes, combien de lignes, quelle taille), puis tu places chaque élément dans la case que tu veux. Un élément peut même occuper plusieurs cases.

## **Les propriétés clés à connaître**

| Propriété | Rôle | Exemple concret |
| :---- | :---- | :---- |
| display: grid | Active la grille sur le conteneur | Layout de page entière |
| grid-template-columns | Définit le nombre et la taille des colonnes | 3 colonnes égales : 1fr 1fr 1fr |
| grid-template-rows | Définit le nombre et la taille des lignes | Header fixe \+ contenu flexible |
| grid-column / grid-row | Place un élément sur des colonnes/lignes spécifiques | Une image qui s’étend sur 2 colonnes |
| gap | Espace entre les cellules de la grille | Espacement régulier entre les cards |
| repeat() | Répétition de colonnes | repeat(3, 1fr) \= 3 colonnes égales |
| fr (fraction) | Unité de fraction de l’espace disponible | 2fr 1fr \= 2/3 \+ 1/3 de l’espace |

## **Quand utiliser CSS Grid**

* Layout global d’une page (header, sidebar, contenu, footer).

* Grilles de produits, galeries photo.

* Dashboards avec widgets de tailles différentes.

* Mises en page éditoriales complexes (magazine, blog).

## **Erreurs à éviter**

* Utiliser Grid pour aligner 3 boutons en ligne. Flexbox suffit.

* Oublier que Grid et Flexbox sont complémentaires. Le meilleur usage : Grid pour la structure de page, Flexbox pour les composants internes.

| ℹ | Grid \+ Flexbox \= le combo gagnant La bonne pratique actuelle : utiliser CSS Grid pour le gabarit global de la page (header/sidebar/main/footer) et Flexbox pour l’agencement des éléments à l’intérieur de chaque zone (nav items, cards, boutons). |
| :---- | :---- |

# **9\. Les propriétés CSS indispensables**

Tu ne les écriras pas toi-même, mais tu dois savoir ce qu’elles font pour comprendre pourquoi un layout se comporte comme il le fait, ou pourquoi il dysfonctionne.

## **box-sizing: border-box**

**Définition**

Par défaut en CSS, quand tu définis la largeur d’un élément (width: 300px), le padding et la bordure s’ajoutent PAR-DESSUS. L’élément fait donc plus que 300px. Avec border-box, le padding et la bordure sont INCLUS dans les 300px. L’élément fait exactement la taille déclarée.

**Pourquoi c’est important**

Sans border-box, les calculs de largeur deviennent imprévisibles. Deux colonnes de 50% \+ du padding dépassent 100% et cassent le layout. C’est pour ça que tous les frameworks CSS et tous les développeurs compétents l’activent en reset global.

**Erreur à éviter**

Si un layout bug inexplicablement (dépassements, scrollbar horizontale), demander au dev si border-box est bien défini globalement. C’est une des causes les plus fréquentes.

## **object-fit: cover**

**Définition**

Quand une image est placée dans un conteneur aux dimensions fixes, object-fit: cover fait en sorte qu’elle remplisse tout le cadre sans se déformer, en se rognant si nécessaire. C’est l’équivalent du recadrage automatique.

**Exemple concret**

Une grille de fiches produits où chaque card a une image de 300x200px. Les photos originales ont toutes des formats différents. Sans object-fit: cover, certaines seront étirées ou écrasées. Avec, elles remplissent toutes proprement le cadre.

**Erreur à éviter**

Demander des images toutes au même format exact au client pour éviter le problème. C’est irréaliste — object-fit: cover est la solution technique standard.

## **position: absolute / relative**

**Définition**

Un élément en position: absolute sort du flux normal de la page et se positionne par rapport à son ancêtre le plus proche qui est en position: relative. Les autres éléments ne le « voient » plus.

**Exemple concret**

Un badge « Nouveau » ou « \-20% » affiché en superposition dans le coin d’une card produit. Un overlay de texte sur une image hero. Une icône de fermeture positionnée dans le coin d’une modale.

**Erreur à éviter**

Abuser de position: absolute pour tout placer « au pixel près ». Ça casse dès que le contenu ou l’écran change. Le positionnement absolu est pour les superpositions, pas pour la structure de page.

# **10\. Spécificité CSS, Variables et Mode Sombre**

## **La spécificité CSS**

**Définition**

La spécificité est le système de priorité du CSS. Quand plusieurs règles ciblent le même élément, le navigateur applique celle qui a le poids le plus fort. Un style appliqué via un ID (\#monElement) est plus fort qu’un style appliqué via une classe (.maClasse), qui est lui-même plus fort qu’un style appliqué via un élément HTML (p, div, h1).

**Pourquoi c’est important pour un CDP**

Quand un développeur te dit « je n’arrive pas à changer la couleur de ce bouton », c’est souvent un problème de spécificité : un autre style plus spécifique prend le dessus. Comprendre ce mécanisme te permet de poser les bonnes questions.

**\!important**

Le mot-clé \!important force une règle CSS à s’appliquer quoi qu’il arrive, en court-circuitant la spécificité. C’est un outil de dernier recours, pas une solution. Un code rempli de \!important est un signal d’alarme : l’architecture CSS est mal structurée.

## **Les variables CSS (Custom Properties)**

**Définition**

Les variables CSS permettent de définir une valeur une seule fois et de la réutiliser partout dans la feuille de style. Par exemple, on définit \--couleur-principale: \#2E5090 et on l’utilise partout avec color: var(--couleur-principale).

**Pourquoi c’est important**

Pour un client qui veut changer son bleu de marque en vert, le développeur modifie une seule variable au lieu de chercher-remplacer dans 200 lignes de CSS. C’est un indicateur de qualité du code : un bon développeur utilise des variables CSS.

**Usage CDP**

En recette, si tu remarques une incohérence de couleur (un bouton qui n’a pas la bonne teinte), le dev peut vérifier si la variable est bien utilisée partout. C’est aussi la base du thème sombre (dark mode).

## **Le mode sombre (Dark Mode)**

**Définition**

Le mode sombre est une fonctionnalité qui inverse le schéma de couleurs du site (fond sombre, texte clair) quand l’utilisateur a activé le mode sombre sur son appareil. En CSS, on le détecte avec la media query prefers-color-scheme: dark.

**Impact projet**

Intégrer un mode sombre double le travail de design et de recette. Cela doit être prévu dès le cahier des charges, pas ajouté en dernière minute. Si le client le souhaite, prévoir les variables CSS dès le départ.

# **11\. Les fonctions calc() et clamp()**

## **calc()**

**Définition**

calc() est une fonction CSS qui permet de faire des calculs mélangeant différentes unités. Par exemple : width: calc(100% \- 40px) crée un élément qui occupe toute la largeur moins 40px de marge.

**Exemple concret**

Une sidebar de 250px fixe à gauche, et un contenu principal qui prend le reste : width: calc(100% \- 250px). Cela permet de mélanger une valeur fixe (la sidebar) et une valeur fluide (le contenu).

**Usage CDP**

calc() est courant dans les spécifications techniques. Quand le designer prévoit « sidebar de 250px \+ contenu flexible », c’est calc() que le développeur utilisera (ou CSS Grid avec 250px 1fr).

## **clamp()**

**Définition**

clamp() est une fonction CSS qui définit une valeur fluide avec un minimum et un maximum. Elle prend trois paramètres : la valeur minimum, la valeur préférée (souvent en vw), et la valeur maximum.

**Syntaxe**

font-size: clamp(1rem, 2.5vw, 2rem) → la taille de police sera de 2.5% de la largeur de l’écran, mais jamais en dessous de 1rem (16px) ni au-dessus de 2rem (32px).

**Pourquoi c’est révolutionnaire**

Avant clamp(), il fallait écrire des media queries pour chaque taille d’écran afin d’ajuster la typographie. clamp() fait le même travail en une seule ligne, de manière fluide. La taille évolue progressivement sans « sauts » entre les breakpoints.

**Usage CDP**

Quand tu vois dans une maquette que le titre principal passe de 24px sur mobile à 48px sur desktop, avec un scaling fluide entre les deux, c’est clamp() que le développeur utilisera.

**Erreurs à éviter**

* Utiliser clamp() avec uniquement des pixels. La valeur préférée (au milieu) doit être en unité relative (vw) pour que le scaling fonctionne.

* En abuser pour tout. clamp() est idéal pour la typographie et les grands éléments visuels, mais pas nécessaire pour les bordures de 1px.

# **12\. Les images responsives**

Les images sont le principal facteur de poids d’une page web. Envoyer une image de 2000px de large à un smartphone qui l’affiche à 375px est un gaspillage de bande passante qui ralentit le chargement.

## **srcset et sizes**

**Définition**

L’attribut srcset permet de fournir plusieurs versions d’une même image à des tailles différentes. Le navigateur choisit automatiquement la version la plus adaptée à l’écran de l’utilisateur (taille \+ résolution). L’attribut sizes complète srcset en indiquant au navigateur la taille d’affichage prévue de l’image selon les conditions d’écran.

**Pourquoi c’est important**

Gain de performance massif. Un smartphone charge une image de 480px au lieu de 2000px. Le temps de chargement est divisé par 4, et la consommation de données mobiles est réduite drastiquement.

## **L’élément \<picture\>**

**Définition**

L’élément HTML \<picture\> permet de servir des images complètement différentes selon la taille de l’écran. C’est ce qu’on appelle l’art direction : sur mobile, on montre un cadrage serré ; sur desktop, on montre le plan large.

**Différence avec srcset**

srcset \= même image à différentes résolutions (le navigateur choisit la meilleure qualité). \<picture\> \= images différentes selon le contexte (le développeur décide quel cadrage montrer).

## **Ce que le CDP doit vérifier en recette**

* Les images ne chargent-elles pas en taille full sur mobile ? (Outils : onglet Réseau des DevTools du navigateur)

* Le design prévoit-il un cadrage différent pour mobile (art direction) ?

* Les images sont-elles en format moderne (WebP ou AVIF) avec fallback JPEG ?

| ⚠ | Impact performance Les images représentent en moyenne 50% du poids d’une page web. Un site qui sert des images non optimisées sur mobile peut avoir un temps de chargement 3à 5 fois plus lent. C’est un sujet de recette critique. |
| :---- | :---- |

# **13\. Vidéos, menus et tableaux responsifs**

## **Les vidéos responsives**

**Définition**

La balise HTML \<video\> permet d’intégrer des vidéos nativement. Pour qu’une vidéo soit responsive, il suffit de lui donner une largeur en pourcentage (width: 100%) et un height: auto.

**Attributs importants**

| Attribut | Rôle | Recommandation CDP |
| :---- | :---- | :---- |
| controls | Affiche les boutons lecture/pause/volume | Toujours actif sauf design spécifique |
| autoplay | Lance la vidéo automatiquement | Déconseillé sauf hero silencieuse |
| muted | Coupe le son par défaut | Obligatoire si autoplay (sinon bloqué par le navigateur) |
| loop | Boucle infinie | Hero vidéo, fonds animés |
| poster | Image affichée avant lecture | Toujours prévoir (UX \+ performance) |

**Erreur à éviter**

Autoplay avec le son : les navigateurs bloquent systématiquement les vidéos qui démarrent avec le son. Si autoplay est nécessaire (hero vidéo), il DOIT être combiné avec muted.

## **Le menu burger (menu responsive)**

**Définition**

Le menu burger est l’icône à trois traits horizontaux (≡) qui remplace le menu de navigation principal sur les écrans mobiles. Au clic, il ouvre un menu dépliant ou un panneau latéral.

**Quand l’utiliser**

Dès que le menu horizontal ne rentre plus sur l’écran sans être tronqué ou compressé. Généralement en dessous de 768px, mais le seuil dépend du nombre d’items de menu.

**Points de vigilance CDP**

* Le menu burger doit être accessible au clavier et aux lecteurs d’écran.

* L’animation d’ouverture/fermeture doit être fluide (pas de « saut »).

* Si le site a des sous-menus, prévoir leur comportement sur mobile (accordéon, sous-panneau).

## 

## 

## **Les tableaux responsifs**

**Le problème**

Les tableaux HTML (\<table\>) sont conçus pour une largeur fixe. Sur mobile, un tableau de 5 colonnes déborde de l’écran ou comprime le contenu au point de le rendre illisible.

**Solutions techniques**

* Défilement horizontal : entourer le tableau d’un conteneur avec overflow-x: auto. Le tableau reste intact, l’utilisateur swipe horizontalement.

* Empilage vertical : sur mobile, chaque ligne du tableau devient un « bloc » où les colonnes s’empilent verticalement avec les labels répétés.

* Colonnes masquées : on cache les colonnes les moins importantes sur mobile et on garde les essentielles.

**Erreur à éviter**

Présenter un tableau de données complexe sans stratégie mobile. En recette, toujours tester les tableaux sur un vrai smartphone, pas seulement dans le responsive du navigateur desktop.

# **14\. Bloc vs Inline et outils**

## **Éléments bloc vs inline**

**Définition**

En HTML/CSS, chaque élément a un mode d’affichage par défaut. Les éléments bloc (div, p, h1, section) prennent toute la largeur disponible et créent un retour à la ligne. Les éléments inline (span, a, strong, em) ne prennent que la largeur de leur contenu et restent sur la même ligne.

**Pourquoi c’est important**

Comprendre la différence explique pourquoi deux images se mettent côte à côte (inline) alors que deux paragraphes s’empilent (bloc). Les propriétés Flexbox et Grid changent ce comportement par défaut.

## **Emmet.io**

**Définition**

Emmet est un plugin intégré à la plupart des éditeurs de code (VS Code, Sublime Text) qui permet d’écrire du HTML et du CSS beaucoup plus vite grâce à des abréviations. Par exemple, taper div.container\>ul\>li\*5 et appuyer sur Tab génère automatiquement un div avec une liste de 5 items.

**Ce que le CDP doit savoir**

Emmet est un outil de productivité pour le développeur. Il n’affecte pas le code final. Mais connaître son existence te permet de comprendre pourquoi un développeur peut coder une page HTML aussi vite.

# **15\. Méthodologie et checklist CDP**

## **Méthodologie de construction**

Un bon développeur front-end ne code pas page par page. Il identifie d’abord les composants récurrents (header, footer, cards, boutons, formulaires) pour les coder une fois et les réutiliser partout. C’est le principe du design system.

**En tant que CDP**

* Vérifier que le designer a identifié les composants récurrents dans sa maquette.

* Demander au développeur comment il structure son CSS (méthodologie BEM, nommage cohérent).

* S’assurer que le code est maintenable : un changement de couleur ne doit pas nécessiter de modifier 50 fichiers.

## **Checklist de recette responsive**

Voici les points à vérifier systématiquement lors de la recette d’un site responsive :

| Point de contrôle | Comment tester | Red flag |
| :---- | :---- | :---- |
| Pas de scrollbar horizontale | Réduire la fenêtre du navigateur | Barre de défilement horizontale visible |
| Texte lisible sans zoom | Tester sur vrai smartphone | Texte \< 14px sur mobile |
| Images adaptées | DevTools \> onglet Réseau | Image de 2000px chargée sur mobile |
| Boutons/liens cliquables | Tester au doigt sur mobile | Boutons trop petits ou trop proches |
| Menu burger fonctionnel | Tester ouverture/fermeture | Menu qui ne se ferme pas, animation saccadée |
| Tableaux lisibles | Tester sur 375px de large | Colonnes tronquées, texte coupé |
| Formulaires utilisables | Remplir un formulaire sur mobile | Champs trop petits, clavier qui masque |
| Vidéos adaptatives | Lancer une vidéo sur mobile | Vidéo qui déborde du cadre |
| Performance mobile | Google PageSpeed Insights | Score \< 50 sur mobile |
| Breakpoints cohérents | Redimensionner lentement le navigateur | Contenu qui casse entre deux breakpoints |

## **Outils à connaître**

| Outil | Usage |
| :---- | :---- |
| Chrome DevTools (F12) | Simuler différentes tailles d’écran, inspecter le CSS |
| Google PageSpeed Insights | Mesurer la performance mobile |
| StatCounter (statcounter.com) | Statistiques de tailles d’écran par marché |
| mydevice.io | Connaître les specs de son propre appareil |
| BrowserStack / LambdaTest | Tester sur de vrais appareils à distance |
| Responsive Design Checker | Vérifier le rendu sur différentes résolutions |

| ✓ | Le mot de la fin En tant que CDP, ta valeur ajoutée sur le responsive n’est pas de coder. C’est de spécifier précisément ce qui est attendu, de poser les bonnes questions au développeur et au designer, et de recetter méthodiquement. Un bon brief responsive évite des semaines de corrections. |
| :---- | :---- |

