# Cahier des charges fonctionnel

> Cartes : [#1](https://github.com/Milie07/gites-de-fontbonne/issues/1)
> Cartes : [#2](https://github.com/Milie07/gites-de-fontbonne/issues/2)
> Cartes : [#3](https://github.com/Milie07/gites-de-fontbonne/issues/3)
> Cartes : [#6](https://github.com/Milie07/gites-de-fontbonne/issues/6)

## 1. Contexte et présentation du projet
Au jour d'aujourd'hui, l'Eurl "Les Sources de Fontbonne" possède 3 gîtes de vacances regroupés dans un hameau nommé "Fontbonne" au cœur de l'Ardèche verte. 
Les trois gîtes sont indépendants, possèdent 5 couchages chacun, sont entièrement équipés pour l'autonomie des hôtes et partagent 1 piscine extérieure, une salle de jeu et un espace spa équipé d'au sauna et d'un jacuzzi. 
Il y a également une chambre avec toilettes et douches louable avec l'un des gîtes s'il y a besoin. Cette chambre n'est pas réservable seule et n'est pas représentée sur les plateformes de location.

Les hôtes qui louent les gîtes sont pour la plupart des familles en vacances ou en week-end, des amis voulant passer du temps ensemble, des randonneurs ou vététistes et même parfois un seul groupe de personne souhaitant se retrouver. Ils recherchent principalement de la déconnexion, de la tranquillité et l'accès à la nature. Il réservent en général sur des week-end ou à la semaine.
Les propriétaires vivent sur place, dans le hameau, mais sur l'avant ce qui laissent aux vacanciers l'impression d'être seuls sur le hameau. 

Le site www.gitesdefontbonne.com a été crée par les anciens propriétaires en 2012 avec WordPress et hébergé sur Ionos. Ce même site a été mis à jour par les nouveaux propriétaires. 

Les Gîtes de Fontbonne sont aujourd’hui visibles en ligne par trois canaux : le site WordPress gitesdefontbonne.com, les annonces Airbnb et Abritel, et une fiche d’établissement Google. Cette fiche affiche la note de 5/5 sur 13 avis Google (novembre 2026) et dirige les visiteurs vers le site. La refonte doit préserver cette visibilité : le lien de la fiche vers le site, la cohérence des informations (nom, adresse, téléphone) et le référencement existant.

## 2. Besoins utilisateurs
### 2.1 Constats sur le site actuel (Novembre 2026)
Audit PageSpeed Insights (https://pagespeed.web.dev/) du 12/11/2026 :

| | Performance | Accessibilité | Bonnes pratiques | SEO |
|---|---|---|---|---|
| Ordinateur | 88 | 87 | 69 | 92 |
| Mobile | 50 | 88 | 69 | 92 |

- Sur mobile, l'élément principal de la page s'affiche en 91,4 s (seuil « bon » de Google : 2,5 s)
- Page d'accueil d'environ 33 Mo, surtout à cause d'images non optimisées
- 32 ressources chargées sans connexion sécurisée, aucun en-tête de sécurité
- Contrastes insuffisants, liens sans nom accessible
- Pas de méta-description
- Tableau des tarifs mal affiché, sur mobile comme sur ordinateur
- Aucune identité visuelle : fond blanc, texte noir et photos
- Pas de calendrier avec les disponibilités des gîtes en lien avec AirBnB et Abritel
### 2.2 Besoins du client
L'Eurl "Les Sources de Fontbonne" souhaiterait pouvoir disposer d'un site et d'un outil capable de :
- refléter l'image des gîtes avec sa propre identité visuelle
- gérer les photos et les informations des gîtes (descriptif, photos, tarifs, etc...) comme il le souhaite,
- afficher un calendrier par gîte avec ses disponibilités synchronisées entre les plateformes (laps de temps d'environ 2h pour la mise à jour)
- les réservations, les conditions d'arrivée des hôtes et à terme les paiements .

### 2.3 Pourquoi changer : les enjeux
- **Des visiteurs perdus sur mobile.** Avec un affichage de plus d'une minute
  sur une connexion mobile lente, un visiteur repart avant d'avoir vu les gîtes.
  C'est autant de demandes de réservation en moins.

- **Un référencement fragilisé.** Google classe les sites surtout d'après leur
  version mobile. La lenteur et l'absence de méta-description pénalisent la
  visibilité, malgré un score SEO technique correct.

- **Un risque pour la sécurité et la réputation.** Ressources non sécurisées,
  absence d'en-têtes de sécurité et failles de sécurité régulières sur Wordpress : le site expose
  les données des visiteurs et l'image des gîtes.

- **Des visiteurs exclus.** Contrastes insuffisants et liens sans nom rendent
  le site difficile à utiliser pour les personnes malvoyantes ou utilisant un
  lecteur d'écran.

- **Une image qui ne reflète pas les gîtes.** Un site sans identité visuelle
  et un tableau des tarifs illisible ne donnent pas envie de réserver.
  
## 3. Objectifs de la refonte
1. Un site rapide sur mobile : élément principal affiché en moins de 2,5 s
2. Un site sécurisé et maîtrisé, sans dépendance à des extensions tierces
3. Un site accessible : contrastes conformes, éléments correctement nommés
4. Une identité visuelle propre aux Gîtes de Fontbonne
5. Des tarifs et des disponibilités clairs, à jour et lisibles sur tout écran
6. Un référencement préservé pendant la migration, puis amélioré

### 3.2 Acteurs
Visiteur, administratrice, systèmes externes (Airbnb, Abritel, serveur mail).
### 3.3 User stories
| N° | En tant que | Je veux | Afin de | Priorité | Critères d'acceptation | Exigences |
|---|---|---|---|---|---|---|
| US-01 | | | | | | |

## 4. Exigences fonctionnelles
| N° | Exigence | Priorité |
|---|---|---|
| EX-01 | | |
### 4.1 Critères d'acceptabilité

## 5. Règles de gestion
| N° | Règle |
|---|---|
| RG-01 | | 

## 6. Contraintes et Exigences non fonctionnelles
### 6.1 Contraintes
RGPD, mentions légales, hébergement Ionos, délai.
### 6.2 Exigences non fonctionnelles
Accessibilité (RGAA), référencement, performance, sécurité.

## 7. Périmètre
### 7.1 Inclus dans la première version
### 7.2 Hors périmètre

## . Cas d'utilisation et diagramme de séquence## 11. Maquettes
Liens vers la charte, les wireframes, les mockups et le fichier Figma.

## 12. Validation
Date et nom
