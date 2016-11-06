# Front-end Job Interview Questions

<a id='toc'></a>

## Table des matières

  1. [Questions générales](#general-questions)
  1. [Questions sur HTML](#html-questions)
  1. [Questions sur CSS](#css-questions)
  1. [Questions sur JS](#js-questions)
  1. [Questions sur réseau](#network-questions)
  1. [Questions sur l'orienté Object](#code-object)
  1. [Questions sur les bases de données](#code-bdd)
  1. [Questions sur la programmation](#code-questions)
  1. [Questions pour le fun](#fun-questions)
  1. [Références](#ref)

---

<a id='general-questions'></a>

## Questions générales

* Qu'avez-vous appris cette semaine ?
* Qu'est ce qui vous motive ou vous intéresse dans le développement ?
* Quel a été le dernier défi technique que vous avez expérimenté et comment l'avez-vous résolu ?
* Quelles considérations en terme d'UI, Sécurité, Performance, SEO, Maintenabilité ou Technologie faites-vous lorsque vous concevez une application web ou site ?

>**UI :** responsive design, clarté, ergonomie, palette de couleurs, social engineering (qu'est-ce que l'utilisateur va voir le plus ? etc...), webfonts (fontface, association des polices serif/sans-serif).
>
>**Sécurité :** https si possible ?, stockage local (cookies) ou distant (BDD) (encryption, hashing, salting).
>
>**Performance :** chargement des scripts et styles au bon moment (pas de `<style>` avant le `</body>`...), fonctions dépréciées, animations lourdes/bidouillées, webfonts légères.<br/>
>Pour JS: création et modification des éléments AVANT leur insertion dans le DOM.<br/>
>Si plusieurs fonctions/manières de coder possibles, bien étudier ce qui est le plus performant, dans ce cas précis, avant de l'utiliser.
>
>**Search Engine Optimisation :**<br/>
>Inutile si :
>- Trop compétitif (ex: assurance hypothécaire)
>- Trop général et pas assez spécifique (ex: plombier)
>- Avec trop peu de recherches (ex: produits nettoyants pour garderie)
>- Non ciblé à une localisation ( ex: dentiste plutôt que dentiste à Ste-Foy)
>
>Il faut des mots-clés qui :
>- Correspondent à des recherches que les gens font
>- Utilisent des termes de localisation comme des villes ou quartiers combinés à votre mot clé
>- Ont un un bon ratio de recherches vs concurrence
>- Correspondent à des requêtes reliées à vos produits ou services
>- Peuvent convertir des visiteurs en clients
>
>Outils :
>- Google Keyword Planner
>- keywordtool.io
>- Suggestions de Google dans la barre de recherche
>
>Points importants :
>- Titre de la page
>- Sous-titre et balises H tags
>- Utiliser des synonymes
>
>**Maintenabilité:** commentaires, architecture évolutive, design patterns, séparation du code au maximum (en fonctions, fichiers...), lisibilité du code (nom des variables/fonctions, espacement)
>
>**Technologie:** faire de la veille, étudier ce qui est le mieux avant de se lancer (Quels languages, frameworks, version des frameworks ?..)

* Parlez-moi de votre environnement de travail préféré.
* Avec quels logiciels de gestion de versions êtes-vous familier?
* Pouvez-vous décrire comment vous travaillez (votre workflow) lorsque vous créez une page web ?<br/>

>**Spécifications :** Définir les spécifications client/projet (graphiques, ergonomie, performance...), réponse à quels besoins (ordi, smartphone/tablette, utilisateurs...)<br/>
>**Recherche :** Chercher s'il existe déjà des projets similaires (inspiration, idées, reprise de projetsn internes...)<br/>
>**Planning :** sur la base des étapes précédentes, évaluer le temps de production<br/>
>**Ebauche du site :** *sitemap* (one-page, ou bien +ieurs pages avec onglets, comment ranger tout ça, dans quelles catégories), *wireframing* (définir l'aspect général sans rentrer dans les considérations graphiques/couleurs -> en concordance avec le futur contenu, mais rempli avec du Lorem Ipsum)<br/>
>**Contenu**<br/>
>**Développement :** CSS, animations, détails suffisants pour présenter le projet au client mais sujets à amélioration après feedback<br/>
>**Feedback**<br/>
>**Améliorations, optimisations, tests, correction de bugs :** UI, performances, et tout ce que le client souhaite voir modifié<br/>
>**SEO**<br/>
>**Déploiement**<br/>
>**Suivi :** support éventuel, suivi du traffic et autres infos (profils visiteurs, Google analytics)

* Donnez-vous une note sur 10 sur les principaux langage que vous maitrisez.
* Si vous aviez 5 feuilles de style différentes, de quelle façon les intégreriez-vous le mieux dans un site ?

>On peut utiliser plusieurs balises `<link>` :

```html
<link rel="stylesheet" href="/styles/xxx.css" type="text/css" />
<link rel="stylesheet" href="/styles/yyy.css" type="text/css" />
```

>On peut également utiliser une balise `<style>` et des `@import`, mais le chargement de la page est plus long :

```html
<style type="text/css">
  @import url(/styles/xxx.css);
  @import url(/styles/yyy.css);
</style>
```

* Pouvez-vous décrire la différence entre amélioration progressive et dégradation gracieuse ?

>**But :** rendre le contenu accessible au plus grand nombre. Ce qui les oppose est leur approche du problème.
>
>**Dégradation gracieuse :** l'approche est *top-down*, on développe d'abord pour une configuration précise, puis on s'efforce d'étendre le nombre de configurations capables de rendre le contenu correctement.
>
>**Amélioration progressive :** l'approche est *bottom-up* (par couches). Les couches sont développées de la plus basique/universelle à la plus spécifique :
>  1. Couche sémantique (HTML, XML) : contenu accessible pour tous (tout est balisé), fonctionnalité accessible pour tous (tout est « cliquable »)
>  1. Couche visuelle (CSS)
>  1. Couche événementielle (JavaScript, AJAX)
>  1. Respect des préférences utilisateur (cookies ?)

* Comment optimisez-vous les performances de vos pages web (assets/ressources) ?

>Minimiser requêtes HTTP, feuilles de style au début, scripts à la fin, réduire nombre d'éléments du DOM, 
>
>**Optimiser les images du site :**
>- Réduire la taille des images
>- Spécifiez la taille des images
>- Créez un sous-domaine pour les images si possible
>
>**Optimiser les feuilles de styles CSS**
>- Assembler tous les styles CSS dans un seul fichier externe
>- Utiliser l’attribut Link plutôt que @import
>- Eviter au maximum les sauts de ligne dans la feuille de style
>- Utiliser les couleurs simplifiées standard à 3 caractères
>- Supprimer toutes les classes et tous les ID non utilisés
>- compresser les fichiers css via des outils de copression tels que http://www.cssdrive.com/index.php/main/csscompressor
>
>**Optimiser la gestion de cache**
>- Installer un système de gestion de cache côté serveur et côté client.
> 
>**Optimiser le JS**
>- Regrouper les scripts JavaScript ensemble dans un fichier JS externe (mais pas dans plusieurs !)
> 
>**Compression des données texte en GZip ou Deflate**

* Combien de ressources différentes à la fois un navigateur peut-il télécharger à partir d'un même domaine ?
  * Quelles sont les exceptions ?

>Une seule, sauf si utilisation du multiplexage (HTTP2)

* Donnez 3 façons qui permettent de réduire le temps de chargement d'une page (perçu ou réel).

>Perçu : utilisation de loaders visuels (plutôt qu'une page blanche), purement comportemental

* Si vous commencez à travailler sur un projet existant, où votre prédécesseur a utilisé des tabulations pour indenter son code et que vous utilisez des espaces, que faites-vous ?
* Décrivez comment vous développeriez un simple diaporama
* Quels outils utilisez-vous pour tester la performance de votre code ?

>Timers, ...

* Si vous pouviez maîtriser parfaitement une technologie cette année, laquelle serait-elle ?
* Expliquez l'importance des standards et des organisations les édictant.
* Qu'est-ce que le FOUC (*flash of unstyled content*) et comment l'évitez-vous ?

>Lorsqu'une page web apparaît brièvement dans le navigateur avant qu'il ait fini de charger une feuille de style externe.
>
>On peut cacher les parties responsables, et les afficher à la fin de l'exécution d'un JS par ex (en leur appliquant une classe "no-fouc" par ex).

* Expliquez ce que sont ARIA et les lecteurs d'écrans, et comment rendre votre site internet accessible

>Accessible Rich Internet Applications : moyens de créer du contenu web plus accessible aux personnes handicapées.
>
>Pour rendre accessible, utiliser des balises spécifiques (notamment en HTML).

* Expliquez quelques-uns des pour et contre des animations CSS par rapport aux animations JavaScript

>Animations CSS utilisent thread différent de JS, donc non-bloquant. De plus, anims CSS accélérées par GPU.
>Mais animations CSS souvent déclenchées en changeant des classes par JS, donc séparation de la logique entre CSS/JS -> au final, plus pratique d'avoir tout côté JS.

**[⬆ back to top](#toc)**

---

<a id='html-questions'></a>

## Questions sur HTML

* Que fait un `doctype` ?

>Indique au navigateur dans quel type de HTML la page a été écrite.
>Sert à validation W3C, forcer le navigateur à détecter des éventuelles erreurs.
>Similaire à un 'use strict'.
>Sert aussi à déclencher le mode standard ou le mode quirks selon la version du doctype (par doctype sniffing).

* Quelle est la différence entre les modes `standard` et `quirks` ?

>En mode standard complet, le comportement est celui décrit par les spécifications HTML et CSS.
>En mode quirks, le navigateur essaie d'afficher les pages "non-standard" correctement (ilfait au mieux...).

* Quelles sont les différences entre HTML et XHTML ?

>XHTML = transposition du HTML 4 en XML. Plus strict que HTML car syntaxe basée sur XML.

* Y a-t-il des problèmes à envoyer des pages avec le *Content-Type* `application/xhtml+xml` ?

>application/xhtml+xml =  XHTML 1.1, donc mal reconnu par IE 6 et IE 7.

* Comment servez-vous une page avec du contenu multilingue ?
* À quoi devez-vous faire attention quand vous *designez* ou développez des pages pour des sites multilingues ?

>Pas de hard-coding en ce qui concerne les langages (images, abbréviations, etc).

* À quoi les attributs `data-` servent-ils ?

>Associer des données à un élement HTML. Cela évite de les stocker côté JS, ou bien dans des attributs par défaut dont l'utilité n'est pas appropriée.

* Si l'on considère que HTML5 est une API Web ouverte, quelles sont les briques de base de HTML5 ?
* Décrivez la différence entre `cookie`, `sessionStorage`, et `localStorage`.

>Ce sont toutes des solutions de stockage côté *client*.
>
>**sessionStorage :** seulement accessible pendant la durée de la session (survit quand même un F5).<br/>
>**localStorage :** accessible sur plusieurs sessions, peut stocker des types JS primitifs (astuce : pour objets et arrays, on peut (dé/)sérialiser en JSON).
>**cookie :** accessible sur plusieurs sessions, mais ne stocke que des strings.

* Décrivez la différence entre `<script>`, `<script async>` et `<script defer>`.

>`<script>` bloque le moteur HTML et CSS en attendant que le fichier soit téléchargé et exécuté. D'où le placement des `<script>` à la fin du fichier html avant la fermeture de `</body>`.
>
>`<script defer>` : Chargement des scripts en parallèle sans bloquer le moteur HTML/CSS. Ordre conservé dans l'apparition des scripts.
>
>`<script async>`: chargement des scripts en asynchrone. Plus de conservation de l'ordre, mais pas de blocage du moteur HTML/CSS, et affichage dès la réception du document HTML.

* Pourquoi est-ce généralement une bonne idée de positionner les `<link>` à l'intérieur de `<head></head>` et les `<script>` juste avant `</body>`? Connaissez-vous des exceptions ?

>Les feuilles de style sont liées dans le `<head>` pour que le navigateur stylise directement le HTML à mesure qu'il est chargé. Si on plaçait le chargement des styles à la fin du document, le navigateur devrait restyliser toute la page et reparcourir le HTML depuis le début.
>
>Les `<script>` sont placés juste avant le `<body/>` pour éviter de lancer des actions sur des éléments qui n'existeraient pas encore.<br/>
>On peut cependant placer les scripts dans le `<head>` et encapsuler son code dans la fonction `$('document').ready(function(){/* Code goes here */});`, ou utiliser `window.onload="myFunction()";`. L'inconvénient de ce dernier est que le script ne s'exécute qu'après le chargement complet de la page (y compris celui des images), alors que placer son script avant le `<body/>` permet d'attendre uniquement que le DOM soit prêt.

* Qu'est-ce que le rendu progressif ?

>Stylisation du HTML au fur et à mesure du chargement de la page (possible en chargeant le CSS dans le head par exemple).

* Comment uploader un fichier ?

**[⬆ back to top](#toc)**

---

<a id='css-questions'></a>

## Questions sur CSS

* Quelle est la différence entre les classes et les IDs en CSS ?

>Les IDs sont uniques.

* Quelle est la différence entre un "reset" et une "normalisation" en CSS ? Lequel choisiriez-vous et pourquoi ?

>Un *reset* supprime tout les styles inclus par défaut (h1-6, p, strong, em...), qui se retrouvent tous identiques. Il faut alors customizer soi-même les décorations.
>
>Une *normalisation* homogénéise le contenu à travers tous les navigateurs web. On rajoute ensuite le reste des décorations que l'on souhaite à partir de cette base commune.

* Décrivez le positionnement flottant et son fonctionnement.

>Une boîte flottante est retirée du flux normal, et placée le plus à droite (`float: right`) ou le plus à gauche (`float: left`) possible dans son conteneur.
>Le contenu suivant cette boîte flottante s'écoule le long de celle-ci, dans l'espace laissé libre.

* Décrivez le `z-index` et comment le contexte d'empilement se forme ?

>Le `z-index` définit la priorité d'affichage dans l'ordre d'empilement (stacking order) d'un contexte d'empilement spécifique.
>
>Quand les propriétés `z-index` et `position` ne sont pas utilisées, l’ordre d’empilement est identique à l’ordre d’apparition dans le HTML (tant qu'on n'utilise pas des marges négatives pour superposer des éléments).
>
>Avec la propriété `position`, les éléments positionnés (et ses enfants) sont affichés devant les éléments non-positionnés (un élément est considéré «positionné» lorsque que la valeur de la propriété `position` est différente de `static`, comme par exemple `relative`, `absolute`, etc.).
>
>Enfin, lorsque `z-index` est associé, les choses deviennent plus délicates. Premièrement, le `z-index` ne fonctionne que sur les éléments positionnés. Deuxièmement, les valeurs de `z-index` peuvent créer un contexte d’empilement.
>
>Chaque contexte d’empilement a un élément HTML unique comme racine. Lorsque un nouveau contexte d’empilement est créé sur un élément, cela contraint ses enfants à apparaître à un endroit précis dans l’ordre d’empilement.
>Cela signifie qu’un élément au sein d’un contexte d’empilement, qui est le plus bas dans l’ordre d’empilement, ne peut pas être affiché devant un élément qui est dans un autre contexte d’empilement affiché plus haut, même avec un `z-index` très important.
>
>De nouveaux contextes d’empilement peuvent êtres créés:
>- Lorsqu'un élément est la racine du document (l’élément `<html>`)
>- Lorsqu'un élément dont la valeur de la propriété `position` est différente de `static` **ET** lorsque `z-index` est différent de `auto`
>- Lorsqu'un élément a une opacité inférieure à 1
>
>Voici les règles qui définissent l’ordre d’affichage pour un même contexte d’empilement (du bas vers le haut) :
>- L’élément racine du contexte d’empilement
>- Les éléments positionnés (et ses enfants) avec un `z-index` négatif (les valeurs les plus hautes sont affichées devant les plus basses; les éléments avec le même `z-index` sont affichés en suivant l’ordre du HTML)
>- Les éléments non-positionnés (en suivant l’ordre du HTML)
>- Les éléments positionnés (et ses enfants) avec un `z-index` dont la valeur est `auto` (en suivant l’ordre du HTML)
>- Les éléments positionnés (et ses enfants) avec un `z-index` positif (les valeurs les plus hautes sont affichées devant les plus basses; les éléments avec le même `z-index` sont affichés en suivant l’ordre du HTML)

* Quelles sont les différentes méthodes de "clearing" des éléments flottants, et laquelle est appropriée pour chaque contexte ?

>Avec `overflow:hidden` sur le bloc contenant les éléments flottants.

```CSS
.container-with-overflow {
  overflow: hidden;
  /* Pour IE6, nécessaire pour déclencher le 'hasLayout' */
  height: 1%;
}
```

>Avec la pseudo-classe `:after`, plus appropriée si on veut éviter de cacher du contenu à cause de `overflow: hidden`.

```CSS
.container-with-generated-content {
  /* Pour déclencher 'hasLayout' sur IE6 et IE7 */
  height: 1%;
}

.container-with-generated-content:after {
  content: ".";
  display: block;
  height: 0;
  clear: both;
  visibility: hidden;
}
```

>En faisant flotter le container lui-aussi.

```CSS
.container-with-float {
    float: left;
    width: 100%;
}
```

>En appliquant un `clear: both` sur une balise `<hr>`.

* Expliquez ce que sont les "sprites" CSS et comment vous les implémenteriez sur une page ou un site.

>Les sprites sont des images combinées en une seule, qui contient tous les états possibles d'un (ou plusieurs) élément(s) (ex: bouton inactif/survolé/cliqué).
>Cette technique est employée par Google, YouTube, Facebook, Amazon... pour minimiser le nombre de requêtes HTTP.
>
>Au départ, seule une partie de l'image est affichée (propriété `background`). Au survol par ex, l'image de fond est décalée grâce à un `background-position`.

```HTML
<a href="#" title="L'edito" id="editorial"><span>L'édito</span></a>
```

```CSS
#editorial {
  display: block;
  width: 80px;
  height: 31px;
  background: url(edito.jpg) 0 0 no-repeat;
}
#editorial:hover, #editorial:active, #editorial:focus {
  /* Sans sprite : background:url(edito_survol.jpg) 0 0 no-repeat; */
  /* Avec sprite : On affiche en background les premiers 31 pixels du haut de l'image (l'état normal du lien), et on décale l'image grâce à background-position pour faire apparaître celle en-dessous. */
  background-position: 0 -31px;
}
#editorial span {
  text-indent: -5000px;
  display: inline-block;
}
```

* Quelles sont vos techniques favorites de remplacement d'images, et comment les utilisez-vous ?

>Utiliser des sprites, et/ou utiliser des attributs `@media` pour du responsive design.

```HTML
<img src="..." class="logo" alt="logo foo" width="300" height="100">
```

```CSS
/* low screens */
@media (max-width: 640px) {
  .logo {
    width: 300px;
    height: 100px;
    background: url(logo-300.png) left top no-repeat;
  }
}
/* high  screens */
@media (min-width: 641px) {
  .logo {
    width: 600px;
    height: 200px;
    background: url(logo-600.png) left top no-repeat;
  }
}
```

* Quelle approche choisiriez-vous pour réparer des bugs au niveau du CSS spécifique à certains navigateurs ?
* Comment servez-vous vos pages pour les navigateurs aux fonctionnalités réduites ?
  * Quelles techniques/procédés utilisez-vous ?

>Modernizr ?

* Quelles sont les différentes manières de masquer du contenu (en le laissant disponible pour les lecteurs d'écran) ?

>Les solutions sont notées *OUI* ou *NON* en fonction de si elles laissent le contenu disponible pour les lecteurs d'écran.

```CSS
/* Solution n°1 : NON*/
{ visibility: hidden; }

/* Solution n°2 : NON*/
{ display: none; }

/* Solution n°3 : NON*/
{ text-indent:-10000px; }
/* ou encore */
{ margin-top:100%; }
/* ou enfin */
{
  width:0;
  /* et/ou */
  height:0; }

/* Solution n°4 : NON
taille de police négative,
couleur du texte = celle de l'arrière-plan,
transparence totale via opacity:100%; ou RGBA(X,X,X,1);
*/

/* Solution n°5 : OUI */
{
  position:absolute;
  left:-9999px;
}

/* Solution n°6 : OUI */
{
  position: absolute;
  left: -2px;
  top: auto;
  width: 1px;
  height: 1px;
  overflow: hidden;
}
```

* Avez-vous déjà utilisé un système de grille, et si oui, lequel préférez-vous ?

>Exemple : celui de Bootstrap.

* Avez-vous déjà implémenté des "media queries", ou des "layouts CSS" spécifiques aux mobiles ?
* Avez-vous déjà touché au style d'un SVG ?
* Comment optimisez-vous vos pages pour l'impression (le print) ?

>Utiliser un attribut `@media print`.

* Quelques astuces pour écrire du CSS efficacement ?

>Utiliser des préprocesseurs + suivre [Ecriture de CSS efficace](https://developer.mozilla.org/fr/docs/%C3%89criture_de_CSS_efficace).

* Quels sont les avantages/désavantages de l'utilisation des préprocesseurs CSS ? (SASS, Compass, Stylus, LESS)
  * Si vous avez un avis, décrivez ce que vous aimez et n'aimez pas des préprocesseurs que vous avez utilisé.
* Comment implémenteriez-vous un design qui utilise des polices de caractères non standards ?

```CSS
@font-face {
  font-family: 'quadranta';
  src: url('quadranta.eot?') format('eot'),
    url('quadranta.otf') format('truetype'),
    url('quadranta.woff') format('woff'),
    url('quadranta.svg#QuadrantaBold') format('svg');
  font-weight: normal;
  font-style: normal;
}	 

h4 {
  font-family: quadranta, sans-serif;
  font-size: 3em;
}
```

* Expliquez comment un navigateur détermine quels éléments correspondent à un sélecteur CSS.
* Expliquez ce que vous avez compris du modèle de boite (box model) et comment implémenteriez vous une mise en page avec des modèles de boite différents.

>- Content : The content of the box, where text and images appear
>- Padding : Clears an area around the content. The padding is transparent
>- Border : A border that goes around the padding and content
>- Margin : Clears an area outside the border. The margin is transparent

* Qu'est-ce que `* { box-sizing: border-box; }` fait ? Quels sont ses désavantages ?

>Sert à spécifier une taille fixe qui prend en compte le padding et les bordures.
>
>Ne gère pas les pseudo-éléments + voir [HTML5 Please - Box sizing](http://html5please.com/#box-sizing).
>Pattern à suivre :

```CSS
/* apply a natural box layout model to all elements, but allowing components to change */
html {
  box-sizing: border-box;
}
*, *:before, *:after {
  box-sizing: inherit;
}
```

* Listez autant de valeurs que vous pouvez pour la propriété `display`.

>`inline, block, inline-block, flex, inline-flex, inline-table, list-item, run-in, table, table-cell, table-..., none, initial, inherit`

* Quelle est la différence entre `inline` et `inline-block` ?

>Un élément `inline-block` est redimensionnable.

* Quelle est la différence entre les éléments ayant `relative`, `fixed`, `absolute` et `static` comme `position` ?

>An element with `position: static;` (default beehavior) is not positioned in any special way. It is always positioned according to the normal flow of the page.
>
>An element with `position: relative;` is positioned relative to its normal position. Setting the `top`, `right`, `bottom`, and `left` properties of a relatively-positioned element will cause it to be adjusted away from its normal position. Other content will not be adjusted to fit into any gap left by the element.
>
>An element with `position: fixed;` is positioned relative to the viewport, which means it always stays in the same place even if the page is scrolled. The `top`, `right`, `bottom` and `left` properties are used to position the element. A fixed element does not leave a gap in the page where it would normally have been located.
>
>An element with `position: absolute;` is positioned relative to the nearest positioned ancestor. However, if an absolute positioned element has no positioned ancestors, it uses the document body, and moves along with page scrolling.

* Le 'C' dans CSS veut dire Cascade (Cascading). Comment la priorité est-elle définie lors de l'assignement de styles (exemples) ? Comment pouvez-vous utiliser ce système à votre avantage ?
* Quels frameworks CSS avez-vous utilisé localement, ou en production ? Comment feriez-vous pour les changer/améliorer ?

>Bootstrap, Foundation, Materialize CSS, Topcoat, Semantic UI, Concise CSS, UIkit, Pure CSS, Cascade, Gumby, Primer CSS...

* Avez-vous expérimenté le récent `flexbox` ?
* En quoi le "responsive design" est différent du "adaptive design" ?

>Responsive design = uniquement la mise en page.
>
>Design adaptif = amélioration progressive + responsive design.

* Avez-vous déjà travaillé avec des images "retina" ? Si oui, à quel moment et quelles techniques avez-vous utilisées ?
* Y a-t-il des raisons particulières pour lesquelles vous voudriez utilser `translate()` plutôt que `position: absolute` ou vice-versa ? Et pourquoi ?

>Transform: meilleures performances/plus smooth (accélération GPU), optimisation du rendu, utiliser RequestAnimationFrame si JS, 

**[⬆ back to top](#toc)**

---

<a id='js-questions'></a>

## Questions sur JS

* Expliquez la délégation d'évènement.

>Lorsqu'un événement est déclenché sur un élément, l'événement est remonté jusqu'à la racine du DOM.
>
>On peut ainsi utiliser la délégation d'événement pour prévoir des événements sur des éléments qui n'ont pas encore été créés (seront ajoutés via JS/Ajax), ou bien utiliser un seul eventListener pour toute une liste en le plaçant sur l'élément parent `ul`.
>
>Le code suivant permet de déléguer la gestion des événements `clic` sur les éléments ayant la classe CSS `elems2` sur l'élément dont l'identifiant est `elem1`.

```javascript
$('#elem1').on('click', '.elems2', callback);
```

* Expliquez comment fonctionne `this` en Javascript.

>Contexte global : `this` fait référence à `window`.
>
>Contexte d'une fonction : soit contexte global (pas de use strict), soit contexte de la base (use strict).
>
>On peut cependant passer le contexte que l'on veut à une fonction avec `call` et `apply`. Attention à bien passer un objet, sinon `ToObject` sera appelé.
>
>On peut aussi utiliser `bind` pour lier un contexte de façon permanente à une fonction, ou des fonctions fléchées (où `this` aura **toujours** la valeur de l'objet englobant où la fonction est utilisée).

* Expliquez comment fonctionne l'héritage de prototype.

>JavaScript n'utilise qu'un seul concept pour l'héritage : les objets.
>Chaque objet possède un lien, interne, vers un autre objet, son prototype. Cet objet `prototype` possède lui aussi un prototype et ainsi de suite, jusqu'à ce que l'on aboutisse à un prototype `null`. `null` n'a, par définition, aucun prototype et forme donc le dernier maillon de la chaîne des prototypes.

* Comment testez-vous votre code Javascript ?
* Que pensez-vous d'AMD par rapport à CommonJS ?
* Expliquez pourquoi ce qui suit n'est pas une IIFE (Immediately Invoked Function Expression) : `function foo(){ }();`.
  * Qu'est-ce qu'il faut changer pour faire une IIFE correcte ?

>Avant le dernier set de parenthèses, le parseur détecte une déclaration, et non une expression. Mettre de parenthèses après cette déclaration ne la fait donc pas s'exécuter.
>
>Il faudrait donc écrire, par exemple (voir [Immediately-Invoked Function Expression (IIFE)](http://benalman.com/news/2010/11/immediately-invoked-function-expression/)) :

```javascript
(function foo(){ }());
```

* Quelle est la différence entre une variable `null`, `undefined` et non déclarée ?
  * Comment feriez-vous pour vérifier chacun de ces états ?

>`null` est une valeur que l'on assigne volontairement à une variable, pour éviter de retourner `0` ou `""` par exemple, qui n'ont pas forcément de sens dans certains contextes.
>
>`undefined` est ce que renvoie une variable non-déclarée, ou bien lorsqu'elle est déclarée mais qu'aucune valeur ne lui a été assignée.
>
>On peut les tester de la manière suivante :

```javascript
if (foo === undefined) {
// ...
} else if (foo === null) {
// ...
}
```

* Qu'est-ce qu'une "closure" et comment/pourquoi en utiliser une ?

>Rendre locale une variable (ex : dans une boucle for où la variable de parcours est définie par var).

* Quelle est l'utilisation typique d'une fonction anonyme ?
* Comment organisez-vous votre code ? (pattern modulaire, héritage classique ?)
* Quelle est la différence entre des objets hôtes et des objets natifs ?

>Les objets hôtes sont fournis par l'environnement hôte (le navigateur par exemple) : `window`, `document`, `location`, `history`, `XMLHttpRequest`, `setTimeout`, `getElementsByTagName`, `querySelectorAll`...

* Différence entre: `function Person() {}`, `var person = Person()` et `var person = new Person()` ?

>`function Person() {}` : déclaration d'une fonction `Person`.
>
>`var person = Person()` : stockage du résultat de l'exécution de la fonction `Person` dans une variable `person`.
>
>`var person = new Person()` : crée un objet `person`.

* Quelle est la différence entre `.call` et `.apply` ?

>The difference is that `.apply` lets you invoke the function with arguments as an array; `.call` requires the parameters be listed explicitly. A useful mnemonic is "A for array and C for comma".

* Expliquez `Function.prototype.bind` ?

>Permet de fixer un contexte donné en paramètre pour la fonction concernée. Peu importe comment elle est appelée, `this` aura toujours la même valeur donnée dans cette fonction.s

* Comment optimisez-vous votre code ?
* Pouvez-vous expliquer comment fonctionne l'héritage en Javascript ?
* Quand utiliseriez-vous `document.write()` ?
* Quelle est la différence entre détection de "feature", inférence de "feature" et l'utilisation du "User-Agent" ?

>Feature detection checks a feature for existence :

```javascript
if (window.XMLHttpRequest) {
  new XMLHttpRequest();
}
```

>Feature inference checks for a feature just like feature detection, but uses another function because it assumes it will also exist :

```javascript
if (document.getElementsByTagName) {
    element = document.getElementById(id);
}
```

>Checking the UA string is an old practice and should not be used anymore. You keep changing the UA checks and never benefit from newly implemented features :

```javascript
if (navigator.userAgent.indexOf("MSIE 7") > -1){
    //do something
}
```

* Expliquez ce qu'est AJAX avec autant de détails que possible.

>Asynchronous Javascript And XML : permet de construire des applications Web et des sites web dynamiques interactifs sur le poste client en se servant de Javascript, CSS, JSON, XML, le DOM, XMLHttpRequest...
>
>En utilisant Ajax, le dialogue entre le navigateur et le serveur se déroule la plupart du temps de la manière suivante : un programme écrit en langage de programmation JavaScript, incorporé dans une page web, est exécuté par le navigateur.
>Celui-ci envoie en arrière-plan des demandes au serveur Web, puis modifie le contenu de la page actuellement affichée par le navigateur Web en fonction du résultat reçu du serveur, évitant ainsi la transmission et l'affichage d'une nouvelle page complète.

* Expliquez comment fonctionne JSONP (et pourquoi ce n'est pas réellement de l'AJAX).
* Avez-vous déjà utilisé des "templates" en Javascript ?
  * Si oui, quelles librairies avez-vous utilisées ?
* Expliquez le phénomène de "hoisting".
* Décrivez le "event bubbling".

>Event bubbling and capturing are two ways of event propagation in the HTML DOM API, when an event occurs in an element inside another element, and both elements have registered a handle for that event.
>The event propagation mode determines in which order the elements receive the event.
>
>With bubbling, the event is first captured and handled by the innermost element and then propagated to outer elements.
>
>With capturing, the event is first captured by the outermost element and propagated to the inner elements.

* Quelle est la différence entre un "attribut" et une "propriété" ?

>Un attribut est une string définie par HTML, une propriété peut être n'importe quel type et est définie par le DOM (ex : propriété `checked` renvoie l'état actuel de la checkbox, différente de l'attribut `checked`, qui renvoie la valeur par défaut de la checkbox).

* Pourquoi étendre des objets natifs de Javascript n'est-il pas une bonne idée ?

>Parce qu'on redéfinit un type, peut poser des problèmes si on utilise plusieurs librairies (redéfinitions, shadowing...).

* Pourquoi étendre des objets natifs est-il une bonne idée ?
* Quelle est la différence entre les évènements "document load" et "document ready" ?
* Quelle est la différence entre `==` et `===` ?

>L'opérateur `==` effectue une conversion implicite avant de faire le test d'égalité.
>Voir [Utiliser les différents tests d'égalité](https://developer.mozilla.org/fr/docs/Web/JavaScript/Les_diff%C3%A9rents_tests_d_%C3%A9galit%C3%A9).

* Expliquez la politique d'origine commune (same-origin policy) et ses implications en JavaScript.

>La same-origin policy restreint la manière dont un document ou un script chargé depuis une origine peut interagir avec une autre ressource chargée depuis une autre origine.
>
>Deux pages ont la même origine si le protocole, le port (si spécifié) et l'hôte sont les mêmes pour les deux pages.
>
>Pour interagir avec une autre origine, il faut activer le **CORS**.

* Expliquez les patterns d'héritage en JavaScript.
* Faites fonctionner ceci :

```javascript
[1,2,3,4,5].duplicator(); // [1,2,3,4,5,1,2,3,4,5]
```

```javascript
Array.prototype.duplicator = function() {
  return this.concat(this);
}
```

* Qu'est ce que l'opérateur ternaire ? Qu'est-ce que ce mot indique ?

>La structure `(condition) ? exécution_si_vrai : exécution_si_faux;`

* Qu'est-ce que `"use strict";`? Quels sont les avantages et désavantages de son utilisation ?
* Créez une boucle `for` qui se répète `100` fois et affichez **"fizz"** aux multiples de `3`, `"buzz"` aux multiples de `5` et **"fizzbuzz"** aux multiples de `3` et `5`.

```javascript
for (let i = 1; i <= 100; i++) {
  let str = '';
  if (!(i % 3)) str += 'Fizz';
  if (!(i % 5)) str += 'Buzz';
  console.log(str || i);
}
```

* Pourquoi il est en général préférable de laissez le 'scope' global d'un site tel quel et ne jamais y toucher ?
* Pourquoi utiliseriez-vous quelque chose comme l'événement `load` ? Est-ce que cet évènement a des avantages ? Connaissez-vous des alternatives, et pourquoi les utiliseriez-vous ?
* Expliquez ce qu'est une application mono-page (*Single Page Application*) et comment feriez-vous pour qu'elle soit optimisée pour le référencement (*SEO*).
* Quelle est l'étendue de votre expérience avec les "Promises" et/ou leurs "polyfills" ?
* Quels sont les pour et contre de l'utilisation des "Promises" à la place des "callbacks" ?

>Pour : lisibilité du code, prevent le *callback hell*

* Quel est le résultat de :

```javascript
["1","2","3"].map(parseInt);
```

>`[1, NaN, NaN]`, car la fonction `parseInt` prend, si non spécifiés, les arguments attendus par la fonction de callback.
>En l'occurrence, il s'agit de la valeur lue dans le tableau, qui est bien le premier paramètre attendu par `parseInt`, ainsi que l'index de cette valeur. Or, le 2ème argument de `parseInt` est la base.
>
>Pour `"1"`, on a donc `parseInt(1, 0) = 1`.<br/>
>Pour `"2"`, on a `parseInt(2, 1)` ce qui n'existe pas (1 n'est pas une bonne base).<br/>
>Pour `"3"`, on a `parseInt(3, 2)` ce qui n'est pas bon car 3 n'est pas exprimable en base 2.

* Avez-vous expérimenté le Javascript ECMA 6 ?

>Let, const, arrow functions, promise, classes...

* Quelle est la principale différence entre les arrows fonctions et les fonctions anonymes ?

>Le contexte.

* Combien y a-t-il de threads en Javascript ?

>Un seul (même si utilisation d'opérations asynchrones comme les promises ou de l'AJAX).

**[⬆ back to top](#toc)**

---

<a id='network-questions'></a>

## Questions sur le réseau

* Que signifie HTTP ?

>HyperText Transfer Protocol.

* Expliquez ce qu'est HTTP.

>C'est un protocole de communication client-serveur développé pour le World Wide Web.
>Il peut fonctionner sur n'importe quelle connexion fiable, dans les faits on utilise le protocole TCP comme couche de transport.

* Pourquoi est-il préférable de disposer ses assets sur des domaines différents ?

>A cause du HTTP, pour pouvoir télécharger plusieurs assets à la fois (un sur chaque domaine différent).

* Faites de votre mieux pour décrire le processus à partir du moment où vous tapez l'URL d'un site internet jusqu'au moment où la page a finit de charger.

>Conversion URL/IP par serveur DNS (celui du FAI de base, sinon modifiable pour celui de Google, OpenDNS...)
>
>Construction requête
>
>Ouverture connection TCP
>
>Envoi de la requête
>
>Traitement de larequête par le serveur
>
>Fabrication et envoi de la réponse
>
>Réception réponse et traitement (affichage)

* Quelle est la différence entre "Long-Polling", "Websockets" et les événements "Server-Sent" ?

>Voir [What are Long-Polling, Websockets, Server-Sent Events (SSE) and Comet?](http://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet).

* Expliquez les entêtes de requêtes et réponses suivant :
  1. Différences entre `Expires`, `Date`, `Age` et `If-Modified-`...
  1. Do Not Track
  1. `Cache-Control`
  1. `Transfer-Encoding`
  1. `ETag`
  1. `X-Frame-Options`

>**1.** Expires = indique le moment après lequel la ressource devrait être considérée obsolète<br/>
>Date = moment auquel le message est généré<br/>
>Age = estimation de l'âge (par le receveur) de la requête depuis son renvoi par le serveur<br/>
>If-Modified = date envoyée au serveur, si page n'a pas été modifiée depuis la date donnée, le serveur renvoie 304. Sinon, renvoie 200 et page entière.
>
>**2.** Do not track = permet de signaler aux applications web que l'utilisateur ne veut pas être "suivi"
>
>**3.** Cache-Control : fixer des durées maximales de rétention, empêcher le stockage des données sur le disque dur, etc...
>
>**4.** Transfer-Encoding = Spécifie l'encodage de transfert. La seule valeur définie par la spécification RFC 2616 est chunked
>
>**5.** ETag = Un ETag est un identifiant unique opaque assigné par le serveur web à chaque version d'une ressource accessible via une URL. Si la ressource accessible via cette URL change, un nouvel ETag différent du précédent sera assigné. Utilisés ainsi, les ETags sont similaires à des empreintes digitales, et peuvent être rapidement comparés pour vérifier si deux versions sont identiques, et ainsi savoir si une demande peut être honorée par un cache local ou pas.
>
>**6.** indique si une ressource est autorisée à être chargée dans un cadre ou un iframe. Si la réponse contient dans cet en-tête une valeur SAMEORIGIN, le navigateur ne chargera la ressource dans un cadre que si la demande provient du même site. Si l’en-tête contient DENY, le navigateur bloque alors le chargement de la ressource dans un cadre quel que soit le site qui en fait la demande.
>Cela permet d'éviter les détournements de clics.

* Quelles sont les différentes actions (verbes) HTTP ? Listez toutes celles que vous connaissez et expliquez-les.

>OPTIONS : options disponibles associées à une ressource, ou capacités d'un serveur
>
>GET : récolte d'informations
>
>HEAD : similaire à GET, mais ne retourne pas de contenu (sert par ex à vérifier la validité d'un lien, pinger un serveur, savoir si une ressource a été modifiée...)
>
>PUT : sert à créer ou modifier une entité COMPLETE
>
>PATCH : sert uniquement pour des mises à jour partielles
>
>POST : création COMPLETE lorsque PUT n'est pas dispo ?.. Voir [POST VS. PUT : LA CONFUSION](http://blog.xebia.fr/2014/03/17/post-vs-put-la-confusion/)
>
>DELETE : demande au serveur de supprimer une ressource

* Quelle est la principale différence entre HTTP1 et HTTP1.1 ?
* Quelle est la principale différence entre HTTP1.1 et HTTP2 ?
* Qu'est ce que le multiplexage et expliquez sont fonctionnement ?
* Qu'est ce qu'un port ?
* Combien il y t'il de port ? A quoi correspond ce nombre ?
* Qui définie les ports par défaut ?
* Qu'est ce que NAT ?
* Qu'est ce que le CORS ?

**[⬆ back to top](#toc)**

---

<a id='code-object'></a>

## Questions sur l'orienté objet

* Qu'est ce que l'orienté objet ?
* Expliquez ce qu'est une interface ?
* Quelles différences entre une classe abstraite et une interface ?
* Qu'est ce que l'héritage ?
* Qu'est ce qu'un design pattern ?
* Qu'est ce que le MVC ?
* Donnez la signification de MVC et expliquez son fonctionnement
* Qu'est ce que le MVVM ?

**[⬆ back to top](#toc)**

---

<a id='code-bdd'></a>

## Questions sur les bases de données

* Que signifie SQL ?
* Expliquez la différence entre SQL et noSQL ?
* Quels sont les avantages du SQL par rapport à du noSQL ?
* Quels sont les avantages du noSQL par rapport à du SQL ?
* Expliquez ce que sont les procédures stockées ?
* Expliquez ce qu'est un trigger ?
* Expliquez ce qu'est un index ?
* Expliquez la différence entre index PRIMARY, UNIQUE, INDEX ?
* Listez autant de type d'index que vous connaissez.
* Expliquez ce qu'est une constraints  ?
* Expliquez ce qu'est l'injection SQL.

**[⬆ back to top](#toc)**

---

<a id='code-questions'></a>

## Questions sur la programmation

* Quelle est la valeur de `foo` ?

```javascript
var foo = 10 + '20';
```

>foo vaut la chaîne de caractères `"1020"`.

* Quelle est la valeur de `v` ?

```javascript
var v = v || o;
```

>Si `o` est en fait `0`, `v` vaut `0`. Sinon, le code retourne une exception `"Uncaught ReferenceError: o is not defined"`, et `v` vaut `undefined`.

* Que retourne ce code ?

```javascript
var v = y || o;
```

>Ce code retourne une exception `"Uncaught ReferenceError: y is not defined"`. `v` vaut `undefined`.

* Comment feriez-vous marcher ceci ?

```javascript
add(2, 5); // 7
add(2)(5); // 7
```

```javascript
const add = function add(a, b) {
  const addBoth = function addBoth(c) { return a + c; };
  if (typeof b === 'undefined') {
    return addBoth;
  }
  return addBoth(b);
};

console.log(add(2, 5)); // 7
console.log(add(2)(5)); // 7
```

* Que retourne ce code ?

```javascript
"je suis un bouffeur de lasagne".split("").reverse().join("");
```

```javascript
"engasal ed rueffuob nu sius ej"
```

* Que retourne `window.foo` ?

```javascript
( window.foo || ( window.foo = "bar" ) );
```

```javascript
"bar"
```

* Qu'affichent les deux alertes ci-dessous ?

```javascript
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```

>La ppemière alerte marche sans souci et affiche `"Hello World"` (la fonction s'auto-appelle).<br/>
>A sa fermeture, il y a une levée d'exception `"Uncaught ReferenceError: bar is not defined"`, car la variable `bar` a été définie dans le contexte local d'une fonction.

* Quelle est la valeur de `foo.length` ?

```javascript
var foo = [];
foo.push(1);
foo.push(2);
```

```javascript
2
```

* Qu'affiche le console log ci-dessous ?

```javascript
Promise.resolve(2)
  .then(x => x * 2)
  .then(y => y / 2)
  .then(z => console.log(z))
```

```javascript
2
```

* Qu'affichent le console log ci-dessous ?

```javascript
for(var i = 0; i < 4; i++) {
  setTimeout(function() {
    console.log(i)
  }, 0);
}
```

>Affiche directement `4`, 4 fois. C'est dû à l'utilisation du mot-clé `var`, qui a une portée **globale** à la boucle : au moment des appels `console.log`, la variable `i` a déjà évolué jusqu'à sa valeur finale.
>
>Pour remédier à cela, on peut utiliser le mot-clé `let`, qui lui a une portée **locale** dans chaque itération de boucle (*cf.* question suivante).

* Qu'affiche le console log ci-dessous ?

```javascript
for(let i = 0; i < 4; i++) {
  setTimeout(function() {
    console.log(i)
  }, 0);
}
```

>Affiche immédiatement `0 1 2 3`.

* Peut-on supprimer l'eventListener ci-dessous ?

```javascript
var bouton = document.createElement("button");
bouton.innerHTML = "Cliquez ici";
document.body.appendChild(bouton);
bouton.addEventListener("click", function () {
    console.log("clic");
});
```

>Non, car pour utiliser `removeEventListener`, il faut que la fonction qui gère l'événement n'ait pas été déclarée de manière anonyme.

* [Autres questions sur le javascript](https://www.toptal.com/javascript/interview-questions)

**[⬆ back to top](#toc)**

---

<a id='fun-questions'></a>

## Questions pour le fun

* Quel est le truc le plus cool que vous ayez programmé, de quoi êtes-vous le plus fier ?
* Quelles sont les parties favorites des outils de développement que vous utilisez ?
* Avez-vous des projets chouchous ? Quel genre ?
* Quelle est votre fonctionnalité favorite dans IE ?
* Comment voulez-vous votre café ?

**[⬆ back to top](#toc)**

---

<a id='ref'></a>

## Références

* [Github Entretien Technique](https://github.com/h5bp/Front-end-Developer-Interview-Questions/tree/master/Translations/French#general-questions)
* [Xebia Javascript](http://blog.xebia.fr/2013/06/10/javascript-retour-aux-bases-constructeur-prototype-et-heritage/)
* [Mozilla Le modèle Objet en Javascript](https://developer.mozilla.org/fr/docs/Web/JavaScript/Guide/Le_mod%C3%A8le_objet_JavaScript_en_d%C3%A9tails)
* [Mozilla l'héritage de prototype](https://developer.mozilla.org/fr/docs/Web/JavaScript/H%C3%A9ritage_et_cha%C3%AEne_de_prototypes)
* [Xebia complexité des collections en Java](http://blog.xebia.fr/2011/02/17/java-collection-performance/)
* [SEO: Comment optimiser votre site web pour référencer votre site internet efficacement](http://oolongmedia.ca/seo-comment-optimiser-le-contenu-de-vos-pages-web-pour-referencer-votre-site-internet-efficacement/)
* [The practical guide to web design workflow](https://www.webdesignerdepot.com/2015/08/the-practical-guide-to-web-design-workflow/)
* [Web design process](http://adogandesign.com/web-design-process/)
* [Amélioration progressive vs dégradation élégante](https://fr.wikipedia.org/wiki/Am%C3%A9lioration_progressive#Am.C3.A9lioration_progressive_vs_d.C3.A9gradation_.C3.A9l.C3.A9gante)
* [Comprendre z-index et les contextes d'empilement](http://iamvdo.me/blog/comprendre-z-index-et-les-contextes-dempilement)
* [Ecriture de CSS efficace](https://developer.mozilla.org/fr/docs/%C3%89criture_de_CSS_efficace)
* [The CSS Box Model](http://www.w3schools.com/css/css_boxmodel.asp)