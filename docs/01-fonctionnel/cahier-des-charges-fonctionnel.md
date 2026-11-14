# Cahier des charges fonctionnel

>Cartes : [#1], [#2], [#3]

---

## Sommaire
1. [Contexte](#1-contexte)
2. [Analyse de l'existant](#2-analyse_de_l'existant)
3. [Besoins et Objectifs](#3-besoins_et_objectifs)
4. [Périmètre](#4-perimetre)
5. [Acteurs](#5-acteurs)
6. [Exigences Fonctionnelles](#6-exigences_fonctionnelles)
7. [Exigences non fonctionnelles](#7-exigences_non_fonctionnelles)
8. [User Stories](#8-user-stories)
9. [Règles de gestion](#8-regles_de_gestion)
10. [Validation](#10-validation)
---

## 1. Contexte
  ### 1.1 L'entreprise et les gîtes
L'EURL « Les Sources de Fontbonne » exploite "les Gîtes de Fontbonne" : 3 gîtes de vacances regroupés dans le hameau de Fontbonne, au cœur de l'Ardèche verte.

Les 3 gîtes sont indépendants. Chacun dispose de 5 couchages et est entièrement équipé pour que les vacanciers soient autonomes. Ils partagent une piscine extérieure, une salle de jeux et un espace spa équipé d'un sauna et d'un jacuzzi.

Une chambre avec salle d'eau (douche et toilettes) peut être louée en complément de l'un des gîtes. Elle n'est pas réservable seule et n'apparaît pas sur les plateformes de location.

Les propriétaires vivent sur place, à l'entrée du hameau, ce qui laisse aux vacanciers l'impression d'être seuls à Fontbonne.

  ### 1.2 La clientèle
Les vacanciers sont pour la plupart des familles, des groupes d'amis, des randonneurs ou des vététistes. Il arrive aussi qu'un seul groupe loue l'ensemble des gîtes pour se retrouver.

Ils recherchent avant tout la déconnexion, la tranquillité et la nature. Ils réservent en général pour un week-end ou à la semaine.

  ### 1.3 La présence en ligne actuelle
Le site www.gitesdefontbonne.com a été créé en 2012 par les anciens propriétaires avec WordPress, et il est hébergé chez Ionos. Les propriétaires actuels l'ont ensuite mis à jour.

Les Gîtes de Fontbonne sont aujourd'hui visibles en ligne par 3 canaux :

- le site WordPress gitesdefontbonne.com ;
- les annonces Airbnb et Abritel ;
- une fiche d'établissement Google, qui affiche la note de 5/5 sur 13 avis (novembre 2026) et dirige les visiteurs vers le site.

La refonte doit préserver cette visibilité : le lien de la fiche Google vers le site, la cohérence des informations (nom, adresse, téléphone) et le référencement existant.

---

## 2. Analyse de l'existant
  ### 2.1 Constats sur le site actuel (réalisé en novembre 2026)

Audit PageSpeed Insights du 12/11/2026 :

| | Performance | Accessibilité | Bonnes pratiques | SEO |
|---|---|---|---|---|
| Ordinateur | 88 | 87 | 69 | 92 |
| Mobile | 50 | 88 | 69 | 92 |

- Sur mobile, l'élément principal de la page s'affiche en 91,4 s (seuil « bon » de Google : 2,5 s).
- La page d'accueil pèse environ 33 Mo, surtout à cause d'images non optimisées.
- 32 ressources sont chargées sans connexion sécurisée, et aucun en-tête de sécurité n'est en place.
- Les contrastes sont insuffisants et certains liens n'ont pas de nom accessible.
- Les pages n'ont pas de méta-description.
- Le tableau des tarifs s'affiche mal, sur mobile comme sur ordinateur.
- Le site n'a pas d'identité visuelle : fond blanc, texte noir et photos.
- Aucun calendrier n'affiche les disponibilités des gîtes en lien avec Airbnb et Abritel.

  ### 2.2 Pourquoi changer :
- **Des visiteurs perdus sur mobile** :

Avec un affichage de plus d'une minute sur une connexion mobile lente, un visiteur repart avant d'avoir vu les gîtes. Ce sont autant de demandes de réservation en moins.
- **Un référencement fragilisé** :

Google classe les sites principalement d'après leur version mobile. La lenteur et l'absence de méta-description pénalisent la visibilité, malgré un score SEO technique correct.
- **Un risque pour la sécurité et la réputation** :

Ressources non sécurisées, absence d'en-têtes de sécurité, failles fréquentes dans les extensions WordPress : le site peut exposer les données des visiteurs et nuire à l'image des gîtes.
- **Des visiteurs exclus** :

Les contrastes insuffisants et les liens sans nom rendent le site difficile à utiliser pour les personnes malvoyantes ou utilisant un lecteur d'écran.
- **Une image qui ne reflète pas celle des gîtes** :

Un site sans identité visuelle et un tableau des tarifs illisible ne donnent pas envie de réserver.

---

## 3. Besoins et objectifs
  ### 3.1 Besoins du client
L'EURL « Les Sources de Fontbonne » souhaite disposer d'un site et d'un espace d'administration permettant de :

- refléter l'image des gîtes grâce à une identité visuelle propre ;
- présenter chaque gîte (descriptif, photos, équipements, tarifs) ;
- afficher, pour chaque gîte, un calendrier des disponibilités synchronisé avec Airbnb et Abritel ;
- estimer le prix d'un séjour selon les dates choisies ;
- recevoir des demandes d'informations ou de réservation par message ;
- gérer en autonomie, sans intervention technique, les informations des gîtes (textes, photos, tarifs) (à confirmer pour la première version) ;
- suivre la fréquentation du site ;
- être trouvé facilement sur Google et consultable rapidement sur mobile, y compris par les personnes en situation de handicap.

  ### 3.2 Objectifs de la refonte
L'objectif principal est de créer un site moderne, performant et accessible, qui permette au visiteur de trouver rapidement l'information qu'il recherche.

- Un site rapide sur mobile : élément principal affiché en moins de 2,5 s ;
- Un site sécurisé et maîtrisé, sans dépendance à des extensions tierces ; 
- Un site accessible : contrastes conformes, éléments correctement nommés ;
- Une identité visuelle propre aux Gîtes de Fontbonne ;
- Des tarifs et des disponibilités clairs, à jour et lisibles sur tout écran ;
- Un référencement préservé pendant la migration, puis amélioré ;

  ### 3.3 Contraintes
- **Synchronisation des calendriers** : les plateformes mettent à jour leurs calendriers toutes les deux heures environ. Les disponibilités affichées seront donc indicatives et confirmées par le propriétaire ;
- **Hébergement** : le site reste hébergé chez Ionos, où se trouve déjà le nom de domaine ;
- **Délai** : mise en ligne avant fin février 2027, avant la saison ;
- **Réglementation** : RGPD et mentions légales ;

---

## 4. Périmètre 

  ### 4.1 Première version
Les besoins listés dans la partie **Besoins du Client**

  ### 4.2 Évolutions envisagées (hors périmètre de la première version)
+ Réservation directe en ligne ;
+ Création des contrats de location depuis l'espace admin et envoi au locataire ;
+ Mise à disposition des documents d'arrivée : livret d'accueil, règlement intérieur, informations sur la taxe de séjour ;
+ Paiement en ligne, avec envoi automatique des e-mails d'acompte, de solde et de confirmation de réception ;

---

## 5. Acteurs (V1)
| Acteur	| Description |
|---|---|
| **Visiteur**	| Personne qui consulte le site : découvre les gîtes, vérifie les disponibilités, estime un prix, envoie une demande |
| **Administrateur**	| Propriétaire des gîtes : gère les demandes, les tarifs et les informations du site |
| **Airbnb et Abritel**	| Systèmes externes : fournissent les calendriers de réservation au format iCal |
| **Serveur mail**	| Système externe : achemine les e-mails de demande et de confirmation |

## 6. Exigences fonctionnelles

| N°	| Exigence	| Priorité |
|---|---|---|
| EX-01 |	À compléter	| À compléter |

## 7. Exigences non fonctionnelles

À compléter (performance, accessibilité, sécurité, référencement).

## 8. User stories
| N° | En tant que | Je veux	| Afin de	| Priorité	| Critères d'acceptation	| Exigences |
|---|---|---|---|---|---|---|
| US-01	| | | | | | |				

## 9. Règles de gestion
| N° | Règle |
|---|---|
| RG-01	| À compléter |

Règles tarifaires : voir regles-tarifaires.md.

## 10. Validation
| Date |	Validé par	| Remarques |
|---|---|---|
| | | |
