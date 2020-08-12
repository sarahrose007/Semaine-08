<!-- omit in toc -->
# SEO, Référencement naturel

SEO (search engine optimization) décrit l'ensemble des pratiques qui permet d'améliorer la position de son site dans les moteurs de recherche.

Le référencement est un sujet très vaste et surtout un job à part entière, il est question ici d'une introduction et de quelques bonnes pratiques. Mais sâchez que dans une agence, une personne sera responsable entièrement du référencement de votre site.

- [Référencement naturel](#référencement-naturel)
- [Outils](#outils)
  - [Google Search Console](#google-search-console)
  - [Google Analytics](#google-analytics)
- [Les "spiders"](#les-spiders)
- [Le contenu](#le-contenu)
  - [La balise title](#la-balise-title)
  - [La meta description](#la-meta-description)
  - [Les titres](#les-titres)
  - [La densité de mots-clé](#la-densité-de-mots-clé)
  - [Le maillage de liens](#le-maillage-de-liens)
  - [Les URLs](#les-urls)
  - [Robots](#robots)
  - [Sitemaps](#sitemaps)
- [Schema.org](#schemaorg)
  - [Les microdata](#les-microdata)
  - [Itemscope & itemtype](#itemscope--itemtype)
  - [Itemprop](#itemprop)
  - [Élément imbriqué](#élément-imbriqué)
  - [Conclusion](#conclusion)
- [Quelques liens](#quelques-liens)

## Référencement naturel

Nous allons souvent entendre parler de 3 termes, mettons directement une petite définition dessus pour savoir de quoi on parle. 

- **SEA**: Search Engine Advertising, c'est lorsqu'on achète des mots clés pour être mieux positionné dans les moteurs de recherche. Il y a un espace réservés à ces annonces sur la page de résultats.
- **SEO**: Search Engine Optimization, c'est lorsqu'on améliore son positionnement par des optimisations dans son code HTML. Tout le monde démarre au même stade, donc tout le monde à sa chance pour se positionner mieux.
- **SEM**: Search Engine Marketing, consiste à l'amélioration de la visibilité de son site par SEO et/ou SEA.

Quand on parle de référencement naturel on parle de SEO et non pas de SEA.

[:arrow_up:Revenir au top](#SEO-Référencement-naturel)

## Outils

Les outils les plus simples à utiliser sont ceux de Google, il ne faut pas se le cacher, mais Google reste le moteur de recherche number 1. 

### Google Search Console

Cet outil permet d'obtenir un rapport de santé de l'indexation de votre site. On y retrouve les informations suivantes

- Un rapport sur le passage des robots Google sur votre site. La donnée intéréssante ici est le nombre de pages visitées et le temps d'exploration.
- Des conseils d'améliorations et l'affichage des erreurs d'explorations (erreurs 404 trop fréquente par exemple dûes à des liens morts)
- La gestion des sitemaps

Il est préférable d'ajouter votre site dès que celui-ci est en ligne pour détecter rapidement les potentiels erreurs. Pour valider votre site, Google vous demandera d'ajouter un enregistrement DNS spécifique qui permet de vérifier que le site vous appartient bien. Suivez les instructions sur le site de Google pour ce faire.

[:lollipop:C'est par ici le site](https://search.google.com/search-console/welcome?hl=fr)

[:arrow_up:Revenir au top](#SEO-Référencement-naturel)

### Google Analytics

Cet outil permet d'analyser le traffic et les habitudes de vos utilisateurs. Cela permet de comprendre comment vos visiteurs sont arrivés et aussi les pages les plus visitées. Il y a énormément de données disponibles pour vous permettre d'analyser les habitudes de vos utilisateurs. Il faudra par contre ajouter un bout de code dans la balise `<head>`des pages que vous voulez surveiller.

[:lollipop:C'est par ici le site](https://marketingplatform.google.com/about/analytics/)

[:arrow_up:Revenir au top](#SEO-Référencement-naturel)

## Les "spiders"

Voyons comment fonctionne un moteur de recherche. Pour proposer les résultats les plus pertinent, ils vont commencer par indexer les sites. Pour cela, des petits robots (spiders), vont parcourir (crawler) votre site pour en analyser son contenu. Quelques paramètres vont influencer la navigation de ces robots:

- La vitesse de chargement de la page. Si la page mets 10 secondes à se charger, les robots vont prendre beaucoup trop de temps pour l'explorer et l'indexer.
- Le maillage de votre site doit être logique. c'est à dire qu'il faut que toutes les pages soient toujours accessibles, si un robot se retrouve sur une page et que de là il ne peut pas allez sur une autre, il n'indexera pas cette dernière. Plus il faut de lien pour arriver sur une page, moins c'est bon.

[:arrow_up:Revenir au top](#SEO-Référencement-naturel)

## Le contenu

Au final les moteurs de recherche ne sont que des programmes qui annalysent le contenu de votre site. Le contenu est donc méga important pour un bon positionnement.


### La balise title

La balise `<title>`permet de donner un titre à votre page. Elle doit décrire au mieux ce contenu de la page et doit absolument être **UNIQUE**. Il est impensable pour un moteur de recherche d'avoir 2 pages avec le même titre.

- On évite donc de mettre le même titre à toutes nos pages
- Le titre doit décrire le contenu de votre page avec des mots-clés importants.
- Le titre doit être synthétique
- Le titre doit être pertinent et pas simplement une suite de mots-clés

Ce titre est celui affiché sur la page des résultats du moteur de recherche, il permet ainsi de guider l'utilisateur. Si le titre lui parle, il aura plus tendance à cliquer dessus.

```html
<head>
  <title>Le référencement HTML pour les noobs</title>
</head>
```

[:arrow_up:Revenir au top](#SEO-Référencement-naturel)

### La meta description

Cette balise n'est plus prise en compte par l'algorithme des moteurs de recherches, mais sert tout de même à afficher une description en dessous du titre de votre page dans la page de résultats.

```html
<head>
  <meta name="description" value="Explication du référencement pour les débutants">
</head>
```

[:arrow_up:Revenir au top](#SEO-Référencement-naturel)

### Les titres

Les robots analysent votre syntaxe HTML. Il est donc important de hiérarchisé correctement votre contenu.

- Il est conseillé de ne placer qu'un seul `<h1>`
- Les `<h2>`, `<h3>`, `<h4>`,... doivent être utilisé logiquement mais pas à des raisons de style pur.
- Les robots ne prennent pas en compte votre style CSS, il faut donc que le contenu de votre site soit lisible quand le style est désactivé. Vous pouvez utiliser une extension Chrome comme [Web Developer](https://chrome.google.com/webstore/detail/web-developer/bfbameneiokkgbdmiekhjnmfkcnldhhm)
- Un mot-clé placé dans un `<h1>`aura plus d'importance qu'un mot-clé dans un `<h2>` ou un `<p>`

[:arrow_up:Revenir au top](#SEO-Référencement-naturel)

### La densité de mots-clé

Répéter volontairement un mot-clé dans un texte pour le placer le plus possible n'est pas recommandé. Au delà d'un certain seul Google considérera cela comme du Spam. Vos phrases doivent avoir du sens pour un humain et pas pour une machine.

[:arrow_up:Revenir au top](#SEO-Référencement-naturel)

### Le maillage de liens

Il est important de créer des liens internes au sein de votre contenu. Plus il y a de liens vers vos autres pages, plus le crawler aura facile d'établir des relations entres ces pages et à les référencer correctement. 

Exemple: Vous écrivez un article sur le référencement naturel, à un moment vous parlez de Google Analytics, vous avez une autre page qui parle de ce sujet, liez les deux pages ensemble!

Sur des outils comme Wordpress, vous avez la possibilité d'afficher des articles relatifs (vous savez, cette section "Ceci pourrait vous intéresser").

[:arrow_up:Revenir au top](#SEO-Référencement-naturel)

### Les URLs

Il faut que vos urls aient une structure logique et contenir des mot-clés important.

- L'URL ne doit pas être trop longue
- Il faut éviter les URLs dynamique (`?id=42`)
- Vaut mieux un mot qu'un chiffre (`/category/7` est moins bien que `/category/css`)
- Garder une structure logique:
  - `/articles` permet de voir tous les articles
  - `/articles/css`permet de voir les articles sur le CSS
  - `/articles/css/selecteurs`permet de voir les articles sur les sélecteurs en CSS
- Les mots doivent être séparé par des tirets
- Les urls sont sensibles à la casse, il faut éviter les majuscules. Préférez mettre tout en minuscule par simplicité
- Évitez les accents et les caractères spéciaux.

[:arrow_up:Revenir au top](#SEO-Référencement-naturel)

### Robots

Il est possible d'écrire des règles pour les robots des moteurs de recherche. Il suffit d'écrire un fichier `robots.txt`et de la placer à la racine de votre site. Ensuite il faut indiquez à l'intérieurs les règles que l'ont veut qu'ils suivent. Il est par exemple possible de faire gagner du temps aux robots en les empêchant de naviguer dans certains dossier

```
User-agent: Googlebot
Disallow: /tutoriels/demo/
```

Pour en savoir plus, voici un lien vers la [:book:documentation](http://robots-txt.com/ressources/)

[:arrow_up:Revenir au top](#SEO-Référencement-naturel)

### Sitemaps

Un sitemap est un fichier XML qui répertorie toutes les pages de votre site et qui peux guider les robots dans leur exploration.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>http://domaine.fr/</loc>
    <lastmod>2014-12-15</lastmod>
    <changefreq>daily</changefreq>
    <priority>1</priority>
  </url>
  <url>
    <loc>http://mon-domaine.fr/page-a.html</loc>
    <lastmod>2014-12-15</lastmod>
    <changefreq>monthly</changefreq>
    <priority>0.8</priority>
  </url>
</urlset>
```

Il est possible de préciser où se situe votre sitemap via Google Search Console.

[:book:Documentation Google Sitemap](https://support.google.com/webmasters/answer/156184?hl=fr)

[:arrow_up:Revenir au top](#SEO-Référencement-naturel)

## Schema.org

La plupart des développeurs de site web sont familiarisé avec les tags HTML. Ceux-ci disent au navigateur comment afficher l'information. Par exemple `<h1>Avatar</h1>` dit au navigateur d'afficher une chaîne de caractère *"Avatar"* dans un titre de niveau 1. Mais ce tag ne donne aucune information à propos de ce mot, est-ce qu'il s'agit du film à succès de 2009 ou bien est-ce qu'on l'on parle d'une image de profile pour un utilisateur.

Schema.org propose une collection de vocabulaire pour identifier correctement votre contenu et ainsi faciliter la tâche aux moteurs de recherches pour référencer votre contenu. Voyons ensemble comment cela fonctionne.

[:arrow_up:Revenir au top](#SEO-Référencement-naturel)

### Les microdata

Les microdata sont un nouvel ensemble de tag HTML5 qui permettent de dire aux moteurs de recherche "Hey, je parle d'un film ou d'une personne, d'un endroit,..."

[:arrow_up:Revenir au top](#SEO-Référencement-naturel)

### Itemscope & itemtype

Commençons avec notre exemple vu plus haut sur le film Avatar. Voici une présentation HTML de la fiche technique du film

```html
<div>
 <h1>Avatar</h1>
 <span>Director: James Cameron (born August 16, 1954)</span>
 <span>Science fiction</span>
 <a href="../movies/avatar-theatrical-trailer.html">Trailer</a>
</div>
```

Première chose à faire c'est d'identifier la section de la page qui parle du film. Dans ce cas-ci il s'agit de la `<div>`qui englobe les données. On va donc indiquer grâce à `itemscope` que c'est cette div qui contient nos infos et ensuite avec `itemtype` on précise de quoi il s'agit grâce aux schémas.

[:book:Documentation schéma](https://schema.org/docs/schemas.html)

```html
<div itemscope itemtype="http://schema.org/Movie">
 <h1>Avatar</h1>
 <span>Director: James Cameron (born August 16, 1954)</span>
 <span>Science fiction</span>
 <a href="../movies/avatar-theatrical-trailer.html">Trailer</a>
</div>
```

[:arrow_up:Revenir au top](#SEO-Référencement-naturel)

### Itemprop

Il est maintenant temps de précisez les éléments à l'intérieur de notre `div`. Chaque schéma à ses propres éléments à préciser via `itemprop`.

```html
<div itemscope itemtype="http://schema.org/Movie">
  <h1 itemprop="name">Avatar</h1>
  <span>Director: <span itemprop="director">James Cameron</span> (born August 16, 1954)</span>
  <span itemprop="genre">Science fiction</span>
  <a href="../movies/avatar-theatrical-trailer.html" itemprop="trailer">Trailer</a>
</div>
```

[:arrow_up:Revenir au top](#SEO-Référencement-naturel)

### Élément imbriqué

Il est parfois possible d'avoir un élément qui est un type lui même, comme par exemple le réalisateur du film peut être également décrit comme étant une personne.

```html
<div itemscope itemtype ="http://schema.org/Movie">
  <h1 itemprop="name">Avatar</h1>
  <div itemprop="director" itemscope itemtype="http://schema.org/Person">
  Director: <span itemprop="name">James Cameron</span> (born <span itemprop="birthDate">August 16, 1954</span>)
  </div>
  <span itemprop="genre">Science fiction</span>
  <a href="../movies/avatar-theatrical-trailer.html" itemprop="trailer">Trailer</a>
</div>
```

[:arrow_up:Revenir au top](#SEO-Référencement-naturel)

### Conclusion

Schema.org est un outil intéressant à utiliser lorsque vous avez des données à répertorier, cela aidera les moteurs de recherches à indexer votre site et à afficher des résultats corrects. Il y a encore quelques petites astuces à connaître sur Schema.org, mais il faudra les explorer par vous même en cas de besoin. 

[:book:Documentation](https://schema.org/docs/documents.html)

[:arrow_up:Revenir au top](#SEO-Référencement-naturel)

## Quelques liens

Vous venez d'avoir un petit aperçu du métier de référencement. Comme précisez en préambule de ce cours, c'est un métier très vaste, il va falloir donc continuer de vous renseigner par vous même si vous voulez que votre site soit premier des résultats! 

Voici quelques liens que j'ai pu consulter pendant la rédaction de ce cours, j'espère qu'ils vous seront utiles.

[:video_camera:Openclassroom: cours sur le référencement](https://openclassrooms.com/fr/courses/2465141-les-cles-pour-reussir-son-referencement-web)

[:book::video_camera:Grafikart](https://www.grafikart.fr/tutoriels/seo-referencement-naturel-594)

[:book:L'encyclopédie du SEO](https://www.seo.fr/definition/cocon-semantique)

[:book:Optimiz](https://optimiz.me/guide-complet-du-referencement/)

[:book:Google](https://support.google.com/webmasters/answer/7451184?hl=fr)