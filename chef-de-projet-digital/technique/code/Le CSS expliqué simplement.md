# **Le CSS expliqué simplement**

## **Qu'est-ce que le CSS, vraiment ?**

Rappelle-toi l'analogie de la maison :

* Le **HTML**, c'est la structure : les murs, les fenêtres, les portes  
* Le **CSS**, c'est la décoration : les couleurs, les tailles, les positions, l'ambiance

CSS signifie "Cascading Style Sheets" (feuilles de style en cascade). C'est le langage qui permet de dire au navigateur : "Ce titre doit être en bleu, en gras, et centré. Ce paragraphe doit avoir une marge de 20 pixels."

**Sans CSS**, le web serait noir et blanc, tout en Times New Roman, sans aucune mise en page. Juste du texte brut de gauche à droite.

## **Le principe fondamental : les règles CSS**

En CSS, tout fonctionne avec des **règles**. Une règle, c'est une instruction qui dit : "Pour cet élément HTML, applique ce style".

Voici la structure de base :

sélecteur {  
    propriété: valeur;  
    propriété: valeur;  
}

**Exemple concret** :

p {  
    color: blue;  
    font-size: 18px;  
}

Décortiquons :

* **`p`** : Le sélecteur (cible tous les `<p>`)  
* **`{}`** : Contient les déclarations de style  
* **`color: blue;`** : Une déclaration (propriété \+ valeur)  
* **`;`** : Le point-virgule sépare les déclarations

## **Comment connecter le CSS au HTML ?**

Il existe 3 méthodes. La meilleure est la dernière.

### **1\. Le style inline (à éviter)**

Directement dans la balise HTML :

\<p style="color: red; font-size: 20px;"\>Texte rouge\</p\>

**Problème** : Si tu as 100 paragraphes, tu dois répéter le style 100 fois. C'est ingérable.

### **2\. Le style dans le `<head>` (pour tester)**

\<\!DOCTYPE html\>  
\<html\>  
\<head\>  
    \<style\>  
        p {  
            color: blue;  
        }  
    \</style\>  
\</head\>  
\<body\>  
    \<p\>Ce paragraphe sera bleu\</p\>  
\</body\>  
\</html\>

**Avantage** : Tout dans un seul fichier, pratique pour tester. **Inconvénient** : Si tu as plusieurs pages HTML, tu dois dupliquer le CSS partout.

### **3\. Un fichier CSS externe (la bonne méthode)**

**Fichier `styles.css`** :

p {  
    color: blue;  
}

**Fichier `index.html`** :

\<\!DOCTYPE html\>  
\<html\>  
\<head\>  
    \<link rel="stylesheet" href="styles.css"\>  
\</head\>  
\<body\>  
    \<p\>Ce paragraphe sera bleu\</p\>  
\</body\>  
\</html\>

**Avantage** : Un seul fichier CSS pour tout ton site. Tu modifies une fois, ça change partout.

## **Les sélecteurs : cibler les éléments**

Les sélecteurs sont le cœur du CSS. Ils définissent **quels éléments** tu vas styliser.

### **Le sélecteur de balise**

Cible tous les éléments d'un type :

h1 {  
    color: green;  
}

p {  
    font-size: 16px;  
}

Tous les `<h1>` seront verts, tous les `<p>` auront une taille de 16px.

### **Le sélecteur de classe**

La classe est l'outil le plus utilisé. Tu donnes un nom à un élément et tu le styles.

**HTML** :

\<p class="important"\>Ce paragraphe est important\</p\>  
\<p\>Ce paragraphe est normal\</p\>  
\<p class="important"\>Celui-ci aussi est important\</p\>

**CSS** :

.important {  
    color: red;  
    font-weight: bold;  
}

**Syntaxe** : Un point `.` suivi du nom de la classe.

**Règle d'or** : Les classes sont réutilisables. Tu peux en mettre sur plusieurs éléments.

### **Le sélecteur d'ID**

L'ID est **unique**. Il ne doit y en avoir qu'un seul par page.

**HTML** :

\<div id="header"\>En-tête principal\</div\>

**CSS** :

\#header {  
    background-color: navy;  
    color: white;  
}

**Syntaxe** : Un dièse `#` suivi du nom de l'ID.

**Règle d'or** : Un ID \= un seul élément dans toute la page.

### **Plusieurs classes sur un élément**

Tu peux combiner plusieurs classes :

**HTML** :

\<p class="texte-rouge texte-grand"\>Texte rouge et grand\</p\>

**CSS** :

.texte-rouge {  
    color: red;  
}

.texte-grand {  
    font-size: 24px;  
}

### **Les sélecteurs combinés**

Tu peux être très précis :

/\* Tous les \<p\> qui ont la classe "intro" \*/  
p.intro {  
    font-style: italic;  
}

/\* Tous les \<p\> qui sont à l'intérieur d'un \<div\> \*/  
div p {  
    color: blue;  
}

/\* Tous les \<p\> qui sont des enfants DIRECTS d'un \<div\> \*/  
div \> p {  
    margin-left: 20px;  
}

/\* Le premier \<p\> après un \<h2\> \*/  
h2 \+ p {  
    font-weight: bold;  
}

## **Les propriétés CSS essentielles**

### **Les couleurs**

Il existe plusieurs façons de définir une couleur :

/\* Nom de couleur \*/  
color: red;

/\* Code hexadécimal \*/  
color: \#FF0000;

/\* RGB \*/  
color: rgb(255, 0, 0);

/\* RGBA (avec transparence) \*/  
color: rgba(255, 0, 0, 0.5); /\* 0.5 \= 50% de transparence \*/

**Propriétés de couleur** :

* `color` : Couleur du texte  
* `background-color` : Couleur de fond

### **Les textes**

p {  
    /\* Taille du texte \*/  
    font-size: 16px;  
      
    /\* Police \*/  
    font-family: Arial, sans-serif;  
      
    /\* Épaisseur \*/  
    font-weight: bold; /\* ou normal, ou un nombre de 100 à 900 \*/  
      
    /\* Style \*/  
    font-style: italic;  
      
    /\* Alignement \*/  
    text-align: center; /\* left, right, center, justify \*/  
      
    /\* Décoration \*/  
    text-decoration: underline; /\* underline, line-through, none \*/  
      
    /\* Espacement entre les lettres \*/  
    letter-spacing: 2px;  
      
    /\* Espacement entre les lignes \*/  
    line-height: 1.5;  
}

### **Les dimensions**

div {  
    /\* Largeur \*/  
    width: 500px;  
      
    /\* Hauteur \*/  
    height: 300px;  
      
    /\* Largeur maximale \*/  
    max-width: 1200px;  
      
    /\* Hauteur minimale \*/  
    min-height: 100px;  
}

**Unités disponibles** :

* `px` : Pixels (fixe)  
* `%` : Pourcentage (relatif au parent)  
* `em` : Relatif à la taille de police de l'élément  
* `rem` : Relatif à la taille de police du document  
* `vh` : Pourcentage de la hauteur de la fenêtre (viewport height)  
* `vw` : Pourcentage de la largeur de la fenêtre (viewport width)

### **Les marges et espacements**

C'est le modèle de boîte (box model) :

┌─────────────────────────────────┐  
│        Margin (marge)           │  
│  ┌───────────────────────────┐  │  
│  │     Border (bordure)      │  │  
│  │  ┌─────────────────────┐  │  │  
│  │  │  Padding (rembour.)│  │  │  
│  │  │  ┌──────────────┐  │  │  │  
│  │  │  │   Content    │  │  │  │  
│  │  │  └──────────────┘  │  │  │  
│  │  └─────────────────────┘  │  │  
│  └───────────────────────────┘  │  
└─────────────────────────────────┘

**Margin** : Espace **extérieur** autour de l'élément **Padding** : Espace **intérieur** entre le contenu et la bordure

div {  
    /\* Marges (extérieur) \*/  
    margin: 20px; /\* Tous les côtés \*/  
    margin: 10px 20px; /\* Haut/bas | Gauche/droite \*/  
    margin: 10px 20px 30px 40px; /\* Haut | Droite | Bas | Gauche (sens horaire) \*/  
      
    /\* Ou individuellement \*/  
    margin-top: 10px;  
    margin-right: 20px;  
    margin-bottom: 30px;  
    margin-left: 40px;  
      
    /\* Padding (intérieur) \*/  
    padding: 15px; /\* Tous les côtés \*/  
    padding: 10px 20px; /\* Haut/bas | Gauche/droite \*/  
      
    /\* Ou individuellement \*/  
    padding-top: 10px;  
    padding-right: 20px;  
    padding-bottom: 30px;  
    padding-left: 40px;  
}

**Astuce** : `margin: 0 auto;` centre un élément horizontalement (si tu as défini une largeur).

### **Les bordures**

div {  
    /\* Bordure complète \*/  
    border: 2px solid black;  
      
    /\* Ou séparément \*/  
    border-width: 2px;  
    border-style: solid; /\* solid, dashed, dotted, double \*/  
    border-color: black;  
      
    /\* Bordures individuelles \*/  
    border-top: 1px solid red;  
    border-right: 2px dashed blue;  
      
    /\* Coins arrondis \*/  
    border-radius: 10px;  
    border-radius: 50%; /\* Cercle parfait si élément carré \*/  
}

## **Le positionnement : gérer l'espace**

### **Display : le comportement de base**

Chaque élément HTML a un comportement par défaut :

/\* Block : prend toute la largeur, commence sur une nouvelle ligne \*/  
div {  
    display: block;  
}

/\* Inline : prend uniquement la largeur du contenu, reste sur la même ligne \*/  
span {  
    display: inline;  
}

/\* Inline-block : mélange des deux (reste sur la même ligne mais accepte width/height) \*/  
img {  
    display: inline-block;  
}

/\* None : cache complètement l'élément \*/  
.cache {  
    display: none;  
}

### **Position : placer les éléments**

/\* Static : comportement par défaut, suit le flux normal \*/  
div {  
    position: static;  
}

/\* Relative : position par rapport à sa position normale \*/  
.decale {  
    position: relative;  
    top: 20px; /\* Décale de 20px vers le bas \*/  
    left: 10px; /\* Décale de 10px vers la droite \*/  
}

/\* Absolute : position par rapport au parent le plus proche qui a position: relative \*/  
.parent {  
    position: relative;  
}

.enfant {  
    position: absolute;  
    top: 0;  
    right: 0; /\* Coin supérieur droit du parent \*/  
}

/\* Fixed : position fixe par rapport à la fenêtre (reste visible au scroll) \*/  
.menu-fixe {  
    position: fixed;  
    top: 0;  
    left: 0;  
    width: 100%;  
}

/\* Sticky : mélange entre relative et fixed (devient fixe au scroll) \*/  
.navbar {  
    position: sticky;  
    top: 0;  
}

### **Flexbox : pour les mises en page modernes**

Flexbox est un système puissant pour aligner et distribuer l'espace entre les éléments.

**Le principe** : Tu as un conteneur parent (flex container) et des enfants (flex items).

\<div class="conteneur"\>  
    \<div class="item"\>Item 1\</div\>  
    \<div class="item"\>Item 2\</div\>  
    \<div class="item"\>Item 3\</div\>  
\</div\>

/\* Le conteneur \*/  
.conteneur {  
    display: flex;  
      
    /\* Direction \*/  
    flex-direction: row; /\* row (horizontal), column (vertical), row-reverse, column-reverse \*/  
      
    /\* Alignement horizontal (axe principal) \*/  
    justify-content: center; /\* flex-start, flex-end, center, space-between, space-around \*/  
      
    /\* Alignement vertical (axe secondaire) \*/  
    align-items: center; /\* flex-start, flex-end, center, stretch \*/  
      
    /\* Retour à la ligne \*/  
    flex-wrap: wrap; /\* nowrap, wrap \*/  
      
    /\* Espacement entre les items \*/  
    gap: 20px;  
}

/\* Les items \*/  
.item {  
    /\* Permet à l'item de grandir pour remplir l'espace disponible \*/  
    flex-grow: 1;  
      
    /\* Permet à l'item de rétrécir si nécessaire \*/  
    flex-shrink: 1;  
      
    /\* Taille de base de l'item \*/  
    flex-basis: 200px;  
      
    /\* Raccourci : flex-grow | flex-shrink | flex-basis \*/  
    flex: 1 1 200px;  
}

**Exemple pratique : centrer quelque chose**

.parent {  
    display: flex;  
    justify-content: center; /\* Centre horizontalement \*/  
    align-items: center; /\* Centre verticalement \*/  
    height: 100vh; /\* Prend toute la hauteur de l'écran \*/  
}

### **Grid : pour les mises en page en grille**

Grid est idéal pour créer des layouts complexes en deux dimensions.

\<div class="grille"\>  
    \<div class="item"\>1\</div\>  
    \<div class="item"\>2\</div\>  
    \<div class="item"\>3\</div\>  
    \<div class="item"\>4\</div\>  
\</div\>

.grille {  
    display: grid;  
      
    /\* Définit 3 colonnes de largeurs égales \*/  
    grid-template-columns: 1fr 1fr 1fr;  
    /\* Ou : repeat(3, 1fr) \*/  
      
    /\* Définit 2 lignes de 200px chacune \*/  
    grid-template-rows: 200px 200px;  
      
    /\* Espacement entre les cellules \*/  
    gap: 20px;  
}

/\* Exemple avancé : colonnes de tailles différentes \*/  
.grille-complexe {  
    display: grid;  
    grid-template-columns: 200px 1fr 2fr;  
    /\* Colonne 1 : 200px fixe  
       Colonne 2 : 1 part de l'espace restant  
       Colonne 3 : 2 parts de l'espace restant \*/  
}

## **Les pseudo-classes : cibler des états**

Les pseudo-classes permettent de cibler des éléments dans des états particuliers :

/\* Au survol de la souris \*/  
a:hover {  
    color: red;  
}

/\* Au clic \*/  
button:active {  
    background-color: darkblue;  
}

/\* Quand l'élément a le focus (formulaires) \*/  
input:focus {  
    border-color: blue;  
}

/\* Le premier enfant \*/  
li:first-child {  
    font-weight: bold;  
}

/\* Le dernier enfant \*/  
li:last-child {  
    color: red;  
}

/\* Le nième enfant \*/  
li:nth-child(2) {  
    color: blue;  
}

/\* Un enfant sur deux (pour les rayures de tableau) \*/  
tr:nth-child(even) {  
    background-color: \#f2f2f2;  
}

## **Les pseudo-éléments : créer du contenu**

Les pseudo-éléments permettent de styliser une partie spécifique d'un élément ou d'ajouter du contenu :

/\* La première lettre \*/  
p::first-letter {  
    font-size: 2em;  
    font-weight: bold;  
}

/\* La première ligne \*/  
p::first-line {  
    color: blue;  
}

/\* Ajouter du contenu avant \*/  
h2::before {  
    content: "→ ";  
    color: red;  
}

/\* Ajouter du contenu après \*/  
a::after {  
    content: " ↗";  
}

## **Responsive design : s'adapter aux écrans**

Les **media queries** permettent d'appliquer des styles selon la taille de l'écran :

/\* Style de base (mobile first) \*/  
.conteneur {  
    width: 100%;  
    padding: 10px;  
}

/\* Écrans moyens (tablettes, min 768px) \*/  
@media (min-width: 768px) {  
    .conteneur {  
        width: 750px;  
        margin: 0 auto;  
    }  
}

/\* Grands écrans (desktop, min 1024px) \*/  
@media (min-width: 1024px) {  
    .conteneur {  
        width: 1000px;  
    }  
}

/\* Très grands écrans (min 1440px) \*/  
@media (min-width: 1440px) {  
    .conteneur {  
        width: 1200px;  
    }  
}

**Points de rupture courants** :

* Mobile : jusqu'à 767px  
* Tablette : 768px à 1023px  
* Desktop : 1024px et plus

## **La cascade et la spécificité**

Le "C" de CSS signifie "Cascade". Quand plusieurs règles s'appliquent au même élément, laquelle gagne ?

### **La spécificité (du plus faible au plus fort)**

1. **Sélecteur de balise** : `p { }`  
2. **Classe** : `.texte { }`  
3. **ID** : `#titre { }`  
4. **Style inline** : `<p style="...">`  
5. **\!important** (à éviter) : `color: red !important;`

**Exemple** :

p {  
    color: blue; /\* Spécificité faible \*/  
}

.important {  
    color: red; /\* Spécificité moyenne, gagne sur la règle précédente \*/  
}

\#titre {  
    color: green; /\* Spécificité forte, gagne sur tout \*/  
}

\<p class="important" id="titre"\>  
    Ce texte sera vert (l'ID gagne)  
\</p\>

### **L'ordre compte**

À spécificité égale, la dernière règle gagne :

p {  
    color: blue;  
}

p {  
    color: red; /\* Gagne car déclarée après \*/  
}

## **Les erreurs à éviter absolument**

### **1\. Oublier le point-virgule**

/\* MAUVAIS \*/  
p {  
    color: red  
    font-size: 18px;  
}

/\* BON \*/  
p {  
    color: red;  
    font-size: 18px;  
}

### **2\. Oublier le point devant une classe**

/\* MAUVAIS \*/  
important {  
    color: red;  
}

/\* BON \*/  
.important {  
    color: red;  
}

### **3\. Utiliser des noms de classe avec espaces**

\<\!-- MAUVAIS \--\>  
\<div class="ma classe"\>

\<\!-- BON \--\>  
\<div class="ma-classe"\>  
\<\!-- ou \--\>  
\<div class="maClasse"\>

### **4\. Abuser de \!important**

/\* À ÉVITER \*/  
p {  
    color: red \!important;  
}

`!important` casse la cascade et rend le code difficile à maintenir. Utilise-le seulement en dernier recours.

### **5\. Ne pas utiliser de reset CSS**

Les navigateurs ont des styles par défaut différents. Un reset permet de partir sur une base propre :

/\* Reset CSS simple \*/  
\* {  
    margin: 0;  
    padding: 0;  
    box-sizing: border-box; /\* Inclut padding et border dans width/height \*/  
}

### **6\. Définir des largeurs fixes sans penser au responsive**

/\* MAUVAIS \*/  
.conteneur {  
    width: 1200px; /\* Déborde sur mobile \*/  
}

/\* BON \*/  
.conteneur {  
    max-width: 1200px;  
    width: 100%;  
    padding: 0 20px;  
}

## **Exemple complet : une carte de service**

**HTML** :

\<div class="carte"\>  
    \<img src="service.jpg" alt="Service" class="carte-image"\>  
    \<div class="carte-contenu"\>  
        \<h3 class="carte-titre"\>Email Marketing\</h3\>  
        \<p class="carte-description"\>  
            Stratégies de rétention pour professionnels de santé.  
        \</p\>  
        \<a href="\#" class="carte-bouton"\>En savoir plus\</a\>  
    \</div\>  
\</div\>

**CSS** :

/\* Reset de base \*/  
\* {  
    margin: 0;  
    padding: 0;  
    box-sizing: border-box;  
}

body {  
    font-family: Arial, sans-serif;  
    background-color: \#f5f5f5;  
    padding: 40px;  
}

/\* La carte \*/  
.carte {  
    max-width: 400px;  
    background-color: white;  
    border-radius: 10px;  
    overflow: hidden;  
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);  
    transition: transform 0.3s ease;  
}

.carte:hover {  
    transform: translateY(-5px);  
    box-shadow: 0 8px 12px rgba(0, 0, 0, 0.15);  
}

/\* L'image \*/  
.carte-image {  
    width: 100%;  
    height: 200px;  
    object-fit: cover;  
}

/\* Le contenu \*/  
.carte-contenu {  
    padding: 20px;  
}

.carte-titre {  
    font-size: 24px;  
    color: \#333;  
    margin-bottom: 10px;  
}

.carte-description {  
    color: \#666;  
    line-height: 1.6;  
    margin-bottom: 20px;  
}

/\* Le bouton \*/  
.carte-bouton {  
    display: inline-block;  
    padding: 10px 20px;  
    background-color: \#007bff;  
    color: white;  
    text-decoration: none;  
    border-radius: 5px;  
    transition: background-color 0.3s ease;  
}

.carte-bouton:hover {  
    background-color: \#0056b3;  
}

## **Les transitions et animations**

### **Transitions : pour des changements fluides**

.bouton {  
    background-color: blue;  
    transition: background-color 0.3s ease;  
}

.bouton:hover {  
    background-color: red;  
}

**Syntaxe** : `transition: propriété durée fonction-timing;`

**Fonctions de timing** :

* `ease` : Lent au début et à la fin  
* `linear` : Vitesse constante  
* `ease-in` : Lent au début  
* `ease-out` : Lent à la fin  
* `ease-in-out` : Lent au début et à la fin

### **Animations : pour des mouvements complexes**

/\* Définir l'animation \*/  
@keyframes glissement {  
    0% {  
        transform: translateX(0);  
    }  
    50% {  
        transform: translateX(100px);  
    }  
    100% {  
        transform: translateX(0);  
    }  
}

/\* Appliquer l'animation \*/  
.element {  
    animation: glissement 2s ease infinite;  
}

**Syntaxe** : `animation: nom durée fonction-timing nombre-répétitions;`

* `infinite` : Répète indéfiniment  
* `alternate` : Alterne aller-retour  
* `forwards` : Garde l'état final

## **Les variables CSS (custom properties)**

Les variables permettent de réutiliser des valeurs :

:root {  
    \--couleur-principale: \#007bff;  
    \--couleur-secondaire: \#6c757d;  
    \--espacement: 20px;  
}

.bouton {  
    background-color: var(--couleur-principale);  
    padding: var(--espacement);  
}

.bouton:hover {  
    background-color: var(--couleur-secondaire);  
}

**Avantage** : Change une seule valeur, ça change partout.

## **Conseils pour progresser**

1. **Commence par des projets simples** : Une carte, un bouton, un menu  
2. **Pratique Flexbox et Grid** : Ce sont les outils modernes de mise en page  
3. **Utilise les DevTools du navigateur** : F12 dans Chrome/Firefox pour inspecter et tester  
4. **Pense mobile-first** : Commence par le design mobile, puis élargis  
5. **Évite les frameworks au début** : Maîtrise d'abord le CSS pur

## **Ressources utiles**

* **MDN Web Docs** : Documentation de référence  
* **CSS-Tricks** : Astuces et guides  
* **Can I Use** : Vérifier la compatibilité navigateur  
* **Flexbox Froggy** : Jeu pour apprendre Flexbox  
* **Grid Garden** : Jeu pour apprendre Grid

## **La suite logique**

Maintenant que tu maîtrises HTML et CSS, tu pourras passer à :

* **JavaScript** : Pour rendre tes pages interactives  
* **Frameworks CSS** : Tailwind, Bootstrap (une fois le CSS pur maîtrisé)  
* **Préprocesseurs** : SASS/SCSS (CSS avec des super-pouvoirs)

Mais d'abord, prends ton temps pour bien maîtriser les bases du CSS. C'est la fondation de tout le web design moderne.

Tu as des questions sur un point particulier ?

