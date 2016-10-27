## <a id='toc'>Table des matières</a>

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

## <a id='general-questions'>Questions générales:</a>

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
* Combien de ressources différentes à la fois un navigateur peut-il télécharger à partir d'un même domaine ?
  * Quelles sont les exceptions ?
* Donnez 3 façons qui permettent de réduire le temps de chargement d'une page (perçu ou réel).
* Si vous commencez à travailler sur un projet existant, où votre prédécesseur a utilisé des tabulations pour indenter son code et que vous utilisez des espaces, que faites-vous ?
* Décrivez comment vous développeriez un simple diaporama
* Quels outils utilisez-vous pour tester la performance de votre code ?
* Si vous pouviez maîtriser parfaitement une technologie cette année, laquelle serait-elle ?
* Expliquez l'importance des standards et des organisations les édictant.
* Qu'est-ce que le FOUC (*flash of unstyled content*) et comment l'évitez-vous ?
* Expliquez ce que sont ARIA et les lecteurs d'écrans, et comment rendre votre site internet accessible
* Expliquez quelques-uns des pour et contre des animations CSS par rapport aux animations JavaScript

**[[UP]](#toc)**

---

## <a id='html-questions'>Questions sur HTML :</a>

* Que fait un `doctype` ?
* Quelle est la différence entre les modes `standard` et `quirks` ?
* Quelles sont les différences entre HTML et XHTML ?
>XHTML = transposition du HTML 4 en XML. Plus strict que HTML car syntaxe basée sur XML.

* Y a-t-il des problèmes à envoyer des pages avec le *Content-Type* `application/xhtml+xml` ?
>application/xhtml+xml =  XHTML 1.1<br/>
>Mal reconnu par IE 6 et IE 7

* Comment servez-vous une page avec du contenu multilingue ?
* À quoi devez-vous faire attention quand vous *designez* ou développez des pages pour des sites multilingues ?
* À quoi les attributs `data-` servent-ils ?
>Associer des données à un élement HTML.

* Si l'on considère que HTML5 est une API Web ouverte, quelles sont les briques de base de HTML5 ?
* Décrivez la différence entre `cookie`, `sessionStorage`, et `localStorage`.
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
* Comment uploader un fichier ?

**[[UP]](#toc)**

---

## <a id='css-questions'>Questions sur CSS :</a>

* Quelle est la différence entre les classes et les IDs en CSS ?
* Quelle est la différence entre un "reset" et une "normalisation" en CSS ? Lequel choisiriez-vous et pourquoi ?
* Décrivez le positionnement flottant et son fonctionnement.
* Décrivez le `z-index` et comment le contexte d'empilement se forme ?
* Quelles sont les différentes méthodes de "clearing" des éléments flottants, et laquelle est appropriée pour chaque contexte ?
* Expliquez ce que sont les "sprites" CSS et comment vous les implémenteriez sur une page ou un site.
* Quelles sont vos techniques favorites de remplacement d'images, et comment les utilisez-vous ?
* Quelle approche choisiriez-vous pour réparer des bugs au niveau du CSS spécifique à certains navigateurs ?
* Comment servez-vous vos pages pour les navigateurs aux fonctionnalités réduites ?
  * Quelles techniques/procédés utilisez-vous ?
* Quelles sont les différentes manières de masquer du contenu (en le laissant disponible pour les lecteurs d'écran) ?
* Avez-vous déjà utilisé un système de grille, et si oui, lequel préférez-vous ?
* Avez-vous déjà implémenté des "media queries", ou des "layouts CSS" spécifiques aux mobiles ?
* Avez-vous déjà touché au style d'un SVG ?
* Comment optimisez-vous vos pages pour l'impression (le print) ?
* Quelques astuces pour écrire du CSS efficacement ?
* Quels sont les avantages/désavantages de l'utilisation des préprocesseurs CSS ? (SASS, Compass, Stylus, LESS)
  * Si vous avez un avis, décrivez ce que vous aimez et n'aimez pas des préprocesseurs que vous avez utilisé.
* Comment implémenteriez-vous un design qui utilise des polices de caractères non standards ?
* Expliquez comment un navigateur détermine quels éléments correspondent à un sélecteur CSS.
* Expliquez ce que vous avez compris du modèle de boite (box model) et comment implémenteriez vous une mise en page avec des modèles de boite différents.
* Qu'est-ce que ```* { box-sizing: border-box; }``` fait ? Quels sont ses désavantages ?
* Listez autant de valeurs que vous pouvez pour la propriété `display`.
* Quelle est la différence entre `inline` et `inline-block` ?
* Quelle est la différence entre les éléments ayant `relative`, `fixed`, `absolute` et `static` comme `position` ?
* Le 'C' dans CSS veut dire Cascade (Cascading). Comment la priorité est-elle définie lors de l'assignement de styles (exemples) ? Comment pouvez-vous utiliser ce système à votre avantage ?
* Quels frameworks CSS avez-vous utilisé localement, ou en production ? Comment feriez-vous pour les changer/améliorer ?
* Avez-vous expérimenté le récent `flexbox` ?
* En quoi le "responsive design" est différent du "adaptive design" ?
* Avez-vous déjà travaillé avec des images "retina" ? Si oui, à quel moment et quelles techniques avez-vous utilisées ?
* Y a-t-il des raisons particulières pour lesquelles vous voudriez utilser `translate()` plutôt que `position: absolute` ou vice-versa ? Et pourquoi ?

**[[UP]](#toc)**

---

## <a id='js-questions'>Questions sur JS :</a>

* Expliquez la délégation d'évènement.
* Expliquez comment fonctionne `this` en Javascript.
* Expliquez comment fonctionne l'héritage de prototype.
* Comment testez-vous votre code Javascript ?
* Que pensez-vous d'AMD par rapport à CommonJS ?
* Expliquez pourquoi ce qui suit n'est pas une IIFE (Immediately Invoked Function Expression) : `function foo(){ }();`.
  * Qu'est-ce qu'il faut changer pour faire une IIFE correcte ?
* Quelle est la différence entre une variable `null`, `undefined` et non déclarée ?
  * Comment feriez-vous pour vérifier chacun de ces états ?
* Qu'est-ce qu'une "closure" et comment/pourquoi en utiliser une ?
* Quelle est l'utilisation typique d'une fonction anonyme ?
* Comment organisez-vous votre code ? (pattern modulaire, héritage classique ?)
* Quelle est la différence entre des objets hôtes et des objets natifs ?
* Différence entre: `function Person() {}`, `var person = Person()` et `var person = new Person()` ?
* Quelle est la différence entre `.call` et `.apply` ?
>The difference is that `.apply` lets you invoke the function with arguments as an array; `.call` requires the parameters be listed explicitly. A useful mnemonic is "A for array and C for comma".

* Expliquez `Function.prototype.bind` ?
* Comment optimisez-vous votre code ?
* Pouvez-vous expliquer comment fonctionne l'héritage en Javascript ?
* Quand utiliseriez-vous `document.write()` ?
* Quelle est la différence entre détection de "feature", inférence de "feature" et l'utilisation du "User-Agent" ?
* Expliquez ce qu'est AJAX avec autant de détails que possible.
* Expliquez comment fonctionne JSONP (et pourquoi ce n'est pas réellement de l'AJAX).
* Avez-vous déjà utilisé des "templates" en Javascript ?
  * Si oui, quelles librairies avez-vous utilisées ?
* Expliquez le phénomène de "hoisting".
* Décrivez le "event bubbling".
* Quelle est la différence entre un "attribut" et une "propriété" ?
* Pourquoi étendre des objets natifs de Javascript n'est-il pas une bonne idée ?
* Pourquoi étendre des objets natifs est-il une bonne idée ?
* Quelle est la différence entre les évènements "document load" et "document ready" ?
* Quelle est la différence entre `==` et `===` ?
* Expliquez la politique d'origine commune (same-origin policy) et ses implications en JavaScript.
* Expliquez les patterns d'héritage en JavaScript.
* Faites fonctionner ceci :
```javascript
[1,2,3,4,5].duplicator(); // [1,2,3,4,5,1,2,3,4,5]
```
* Qu'est ce que l'opérateur ternaire ? Qu'est-ce que ce mot indique ?
* Qu'est-ce que `"use strict";`? Quels sont les avantages et désavantages de son utilisation ?
* Créez une boucle `for` qui se répète `100` fois et affichez **"fizz"** aux multiples de `3`, `"buzz"` aux multiples de `5` et **"fizzbuzz"** aux multiples de `3` et `5`.
* Pourquoi il est en général préférable de laissez le 'scope' global d'un site tel quel et ne jamais y toucher ?
* Pourquoi utiliseriez-vous quelque chose comme l'événement `load` ? Est-ce que cet évènement a des avantages ? Connaissez-vous des alternatives, et pourquoi les utiliseriez-vous ?
* Expliquez ce qu'est une application mono-page (*Single Page Application*) et comment feriez-vous pour qu'elle soit optimisée pour le référencement (*SEO*).
* Quelle est l'étendue de votre expérience avec les "Promises" et/ou leurs "polyfills" ?
* Quels sont les pour et contre de l'utilisation des "Promises" à la place des "callbacks" ?
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
* Quelle est la principale différence entre les arrows fonctions et les fonctions anonymes ?
* Combien il y a t'il de thread en javascript ?

**[[UP]](#toc)**

---

## <a id="network-questions">Questions sur le réseau</a>

* Que signifie HTTP ?
* Expliquez ce qu'est HTTP.
* Pourquoi est-il préférable de disposer ses assets sur des domaines différents ?
* Faites de votre mieux pour décrire le processus à partir du moment où vous tapez l'URL d'un site internet jusqu'au moment où la page a finit de charger.
* Quelle est la différence entre "Long-Polling", "Websockets" et les événements "Server-Sent" ?
* Expliquez les entêtes de requêtes et réponses suivant :
  * Différences entre `Expires`, `Date`, `Age` et `If-Modified-`...
  * Do Not Track
  * `Cache-Control`
  * `Transfer-Encoding`
  * `ETag`
  * `X-Frame-Options`
* Quelles sont les différentes actions (verbes) HTTP ? Listez toutes celles que vous connaissez et expliquez-les.
* Quelle est la principale différence entre HTTP1 et HTTP1.1 ?
* Quelle est la principale différence entre HTTP1.1 et HTTP2 ?
* Qu'est ce que le multiplexage et expliquez sont fonctionnement ?
* Qu'est ce qu'un port ?
* Combien il y t'il de port ? A quoi correspond ce nombre ?
* Qui définie les ports par défaut ?
* Qu'est ce que NAT ?
* Qu'est ce que le CORS ?

**[[UP]](#toc)**

---

## <a id='code-object'>Questions sur l'orienté objet :</a>
* Qu'est ce que l'orienté objet ?
* Expliquez ce qu'est une interface ?
* Quelles différences entre une classe abstraite et une interface ?
* Qu'est ce que l'héritage ?
* Qu'est ce qu'un design pattern ?
* Qu'est ce que le MVC ?
* Donnez la signification de MVC et expliquez son fonctionnement
* Qu'est ce que le MVVM ?

**[[UP]](#toc)**

---

## <a id='code-bdd'>Questions sur les bases de données :</a>
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

**[[UP]](#toc)**

---

## <a id='code-questions'>Questions sur la programmation :</a>

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
var add = function add(a,b) {
  var ddd = function (b){return a+b;};
  if (typeof b == 'undefined') {
    return ddd;
  } else {
    return ddd(b);
  }
}
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
```
2
```

* Qu'affiche le console log ci-dessous ?
```javascript
Promise.resolve(2)
  .then(x => x * 2)
  .then(y => y / 2)
  .then(z => console.log(z))
```
```
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

**[[UP]](#toc)**

---

## <a id='fun-questions'>Questions pour le fun :</a>

* Quel est le truc le plus cool que vous ayez programmé, de quoi êtes-vous le plus fier ?
* Quelles sont les parties favorites des outils de développement que vous utilisez ?
* Avez-vous des projets chouchous ? Quel genre ?
* Quelle est votre fonctionnalité favorite dans IE ?
* Comment voulez-vous votre café ?

**[[UP]](#toc)**

---

## <a id='ref'>Références :</a>

* [Github Entretien Technique](https://github.com/h5bp/Front-end-Developer-Interview-Questions/tree/master/Translations/French#general-questions)
* [Xebia Javascript](http://blog.xebia.fr/2013/06/10/javascript-retour-aux-bases-constructeur-prototype-et-heritage/)
* [Mozilla Le modèle Objet en Javascript](https://developer.mozilla.org/fr/docs/Web/JavaScript/Guide/Le_mod%C3%A8le_objet_JavaScript_en_d%C3%A9tails)
* [Mozilla l'héritage de prototype](https://developer.mozilla.org/fr/docs/Web/JavaScript/H%C3%A9ritage_et_cha%C3%AEne_de_prototypes)
* [Xebia complexité des collections en Java](http://blog.xebia.fr/2011/02/17/java-collection-performance/)
* [SEO: Comment optimiser votre site web pour référencer votre site internet efficacement](http://oolongmedia.ca/seo-comment-optimiser-le-contenu-de-vos-pages-web-pour-referencer-votre-site-internet-efficacement/)
* [The practical guide to web design workflow](https://www.webdesignerdepot.com/2015/08/the-practical-guide-to-web-design-workflow/)
* [Web design process](http://adogandesign.com/web-design-process/)
* [Amélioration progressive vs dégradation élégante](https://fr.wikipedia.org/wiki/Am%C3%A9lioration_progressive#Am.C3.A9lioration_progressive_vs_d.C3.A9gradation_.C3.A9l.C3.A9gante)
