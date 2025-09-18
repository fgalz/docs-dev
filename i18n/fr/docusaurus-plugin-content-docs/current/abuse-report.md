---
id: abuse-report
title: "Signaler un abus et un contenu illégal - Tout ce que vous devez savoir !"
description: "Comment signaler un abus et un contenu illégal à ZAP-Hosting - Documentation ZAP-Hosting.com"
sidebar_label: Signaler un abus
---

## Introduction

Internet crée de la valeur. L’abus nuit aux utilisateurs et aux services. Notre objectif est de détecter et d’arrêter les incidents rapidement. Vous pouvez signaler tout abus présumé à notre équipe Abuse. Nous examinons chaque signalement, préservons les preuves, agissons conformément à la loi applicable et à nos politiques, et informons les autorités compétentes si nécessaire.

## Types d’abus

L’abus peut prendre différentes formes. Signalez tout cas qui correspond ou s’approche des catégories ci-dessous :

<details>
  <summary>Spam</summary>

Messages non sollicités ou en masse envoyés via nos systèmes ou contenu hébergé déclenchant des filtres anti-spam. Variantes : spam par e-mail, spam de commentaires, spam de liens SEO, création automatisée de comptes. Fournissez des exemples de messages, en-têtes, IP d’expéditeur et schémas d’envoi.

</details>

<details>
  <summary>Attaques et DDoS</summary>

Trafic hostile visant à perturber les services ou sonder les systèmes. Formes courantes : floods volumétriques L3 L4, floods HTTP couche 7, amplification, tentatives de connexion par force brute, scans de ports agressifs. Indicateurs : pics de PPS ou Mbps, taux élevés de 4xx/5xx, échecs d’authentification répétés depuis des sources tournantes.

</details>

<details>
  <summary>Violations de droits d’auteur et de marques</summary>

Distribution non autorisée d’œuvres protégées ou usage abusif de marques déposées. Variantes : miroirs de piratage, téléchargements crackés, usurpation de marque, domaines trompeurs. Fournissez l’œuvre, le titulaire des droits, l’emplacement exact et le statut d’autorisation.

</details>

<details>
  <summary>Phishing</summary>

Contenu conçu pour collecter des identifiants ou des données de paiement en imitant des marques de confiance. Variantes : faux portails de connexion, arnaques à la facture, leurres QR ou pièces jointes, fatigue MFA. Précisez la marque ciblée, les points de collecte et les différences avec le site légitime.

</details>

<details>
  <summary>RGPD</summary>

Traitement, exposition ou fuite non autorisée de données personnelles. Cas typiques : index ouverts, buckets mal configurés, scraping sans base légale, journaux publics. Décrivez les catégories de données, l’étendue, les personnes concernées et la cause de l’exposition.

</details>

<details>
  <summary>CSAM/SAM</summary>

Tout contenu représentant l’exploitation sexuelle d’êtres humains. Tolérance zéro.

</details>

<details>
  <summary>Contenu illégal</summary>

Contenu enfreignant la loi applicable, tel que propagande extrémiste, menaces, discours de haine, incitation à la violence ou diffamation. Variantes : doxxing, menaces explicites, contenus interdits par la juridiction. Fournissez l’emplacement exact et, si connu, la base légale concernée.

</details>

<details>
  <summary>Autre</summary>

Abus ne rentrant pas dans les catégories ci-dessus mais nuisant tout de même aux utilisateurs ou systèmes. Exemples : hébergement de malwares, C2 de botnet, fraude, minage de cryptomonnaie non autorisé. Partagez les hashes, URLs, schémas C2, anomalies d’utilisation des ressources.

</details>

## Informations requises

Pour garantir un signalement complet et exploitable, veuillez fournir des détails permettant d’identifier la ressource, de vérifier l’incident et de prendre les mesures appropriées, notamment :
- Emplacement : URL, IP, port, nom d’hôte, chemin de fichier, hash
- Horodatages en UTC au format AAAA-MM-JJTHH:MM:SSZ
- Description : ce qui s’est passé, comment détecté, impact observé
- Preuves : captures d’écran, journaux texte, e-mail complet avec en-têtes au format EML, court PCAP, NetFlow, en-têtes HTTP

## Fichiers acceptés et transmission

Fournissez les preuves dans des formats clairs et accessibles de manière fiable. Joignez les petits fichiers à votre e-mail ou hébergez les gros fichiers en externe. Préférez les formats ouverts et non modifiés. Le texte brut est préférable aux captures d’écran de texte.

Pour les gros fichiers, partagez un lien de téléchargement stable. Il doit être accessible sans interaction ou inclure des identifiants clairs. Indiquez la durée de validité du lien. Ajoutez des sommes de contrôle pour permettre la vérification de l’intégrité.

Utilisez des formats standards tels que TXT, PDF, PNG, JPG, PCAP ou PCAPNG, EML, HAR, CSV et JSON. N’incluez pas de mots de passe, clés privées ou données personnelles complètes sauf nécessité absolue.

Pour la qualité, soumettez les e-mails au format EML avec en-têtes complets, les journaux en texte brut, les traces réseau en captures PCAP ou PCAPNG courtes et pertinentes, et les captures d’écran en résolution d’origine.

Pour la sécurité, censurez tout secret ; si besoin, placez les fichiers dans une archive protégée par mot de passe et communiquez le mot de passe séparément. Pour le CSAM/SAM, ne transmettez pas de fichiers, fournissez uniquement des liens.

## Contactez-nous

Envoyez votre signalement à `abuse@zap-hosting.com`. Il est important d’utiliser un objet clair comme `Signalement Abus Phishing` ou `Signalement Abus DDoS`. Envoyez un e-mail par incident. L’exemple ci-dessous montre une demande complète :

```
À : abuse@zap-hosting.com
Objet : Signalement Abus Brute Force (SSH)

Emplacement :
- IP cible : XXX.XX.XXX.XX
- Service : SSH
- Port : 22
- Nom d’hôte : v12345.zap-hosting.com

Horodatages (UTC) :
- Première détection : 2025-08-23T09:12:04Z
- Dernière détection : 2025-08-23T10:03:31Z

Description :
Tentatives répétées de connexion SSH avec des noms d’utilisateur et des IP sources tournants. Détecté via des anomalies dans auth.log et un taux de connexion élevé. Authentification par mot de passe désactivée après détection. Aucun accès réussi observé.

Preuves :
- Extrait de auth.log avec plusieurs entrées "Failed password" et "Invalid user"
- Extrait de log fail2ban montrant les bannissements et adresses sources
- PCAP de 60 secondes capturant les tentatives TCP sur le port 22
- Comptes agrégés : 12 438 tentatives depuis 352 IP sources
- Principales sources avec informations ASN

Extrait de log exemple :
2025-08-23T09:55:17Z sshd[2173]: Failed password for invalid user admin from XXX.X.XXX.XX port XXXX ssh2
2025-08-23T09:55:18Z sshd[2173]: Failed password for root from XXX.X.XX
```

## Que se passe-t-il ensuite

Notre équipe Abuse traite votre signalement aussi rapidement que possible et répond dans les plus brefs délais.

Après examen, nous prenons des mesures telles que la notification du client, la suspension temporaire ou définitive, la suppression du contenu signalé, la préservation des preuves et la notification des autorités compétentes si nécessaire.