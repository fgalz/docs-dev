---
id: abuse-report
title: "Signaler un abus et un contenu illégal - Tout ce que vous devez savoir!"
description: "Comment signaler un abus et un contenu illégal à ZAP-Hosting - Documentation de ZAP-Hosting.com"
sidebar_label: Signaler un abus
---

## Introduction

Internet permet de créer de la valeur. Les abus nuisent aux utilisateurs et aux services. Notre objectif est de détecter et d'arrêter rapidement les incidents. Vous pouvez signaler tout abus suspect à notre équipe d'abus. Nous examinons chaque rapport, préservons les preuves, agissons en vertu de la loi applicable et de nos politiques, et informons les autorités compétentes lorsque cela est nécessaire.

## Type d'abus

Bonjour, mon nom est! L'abus peut se manifester de différentes manières. Signalez tout cas qui correspond ou est proche des catégories ci-dessous :

<details>
  <summary>Spam</summary>

Messages non sollicités ou en vrac envoyés par nos systèmes ou contenu hébergé qui déclenche des filtres de spam. Les variantes incluent le spam par e-mail, le spam de commentaires, le spam de liens SEO et la création automatisée de comptes. Fournissez des exemples de messages, des en-têtes, des adresses IP d'expéditeurs et des modèles d'envoi.

</details>

<details>
  <summary>Attaques et DDoS</summary>

Trafic hostile destiné à perturber les services ou à sonder les systèmes. Les formes courantes sont les inondations volumétriques L3 L4, les inondations HTTP de couche 7, l'amplification, les tentatives de connexion par force brute et les scans de ports agressifs. Les indicateurs comprennent des pics en PPS ou Mbps, des taux 4xx 5xx élevés et des échecs d'authentification répétés à partir de sources rotatives.

</details>

<details>
  <summary>Violations du droit d'auteur et des marques déposées</summary>

Distribution non autorisée d'œuvres protégées ou mauvaise utilisation de marques déposées. Les variantes incluent les miroirs de piratage, les téléchargements craqués, l'usurpation de marque et les domaines trompeurs. Fournissez l'œuvre, le titulaire des droits, l'emplacement exact et le statut d'autorisation.

</details>

<details>
  <summary>Hameçonnage</summary>

Contenu conçu pour récolter des identifiants ou des données de paiement en imitant des marques de confiance. Les variantes incluent les faux portails de connexion, les arnaques aux factures, les leurres QR ou pièces jointes, et la fatigue MFA. Précisez la marque cible, les points de capture et comment la page diffère du site légitime.

</details>

<details>
  <summary>RGPD</summary>

Traitement non autorisé, exposition ou fuite de données personnelles. Les cas typiques incluent les index ouverts, les seaux mal configurés, le scraping sans base légale et les journaux publics. Décrivez les catégories de données, la portée, les sujets affectés et la cause de l'exposition.

</details>

<details>
  <summary>CSAM/SAM</summary>

Tout matériel dépeignant l'exploitation sexuelle des humains. Tolérance zéro.

</details>

<details>
  <summary>Contenu illégal</summary>

Contenu qui viole la loi applicable telle que la propagande extrémiste, les menaces, les discours de haine, l'incitation à la violence ou la diffamation. Les variantes incluent le doxxing, les menaces explicites et les matériaux interdits par juridiction. Fournissez l'emplacement exact et, si connu, le fondement juridique impliqué.

</details>

<details>
  <summary>Autre</summary>

Abus qui ne correspond pas aux catégories ci-dessus mais qui nuit toujours aux utilisateurs ou aux systèmes. Les exemples incluent l'hébergement de logiciels malveillants, le C2 de botnet, la fraude et le cryptominage non autorisé. Partagez les hachages, les URL, les modèles C2 et les anomalies d'utilisation des ressources.

</details>

## Informations requises

Pour garantir un rapport complet et exploitable, veuillez fournir des détails complets qui nous permettent d'identifier la ressource, de vérifier l'incident et de prendre les mesures appropriées, y compris les suivantes :
- Emplacement. URL, IP, port, nom d'hôte, chemin de fichier, hachage
- Horodatages en UTC au format AAAA-MM-JJTHH:MM:SSZ
- Description. Ce qui s'est passé, comment détecté, impact observé
- Preuves. Captures d'écran, journaux de texte, e-mail complet avec en-têtes en EML, court PCAP, NetFlow, en-têtes HTTP

## Fichiers acceptés et provision

Fournissez des preuves dans des formats clairs et de manière à ce que nous puissions y accéder de manière fiable. Joignez de petits fichiers à votre e-mail ou hébergez de gros fichiers à l'extérieur. Joignez de petits à moyens fichiers directement. Préférez les formats ouverts et non modifiés. Le texte brut est préférable aux captures d'écran de texte.

Pour les gros fichiers, partagez un lien de téléchargement stable. Il devrait être récupérable sans interaction ou inclure des identifiants clairs. Indiquez la fenêtre de validité du lien. Ajoutez des sommes de contrôle pour permettre la vérification de l'intégrité.

Utilisez des formats standard tels que TXT, PDF, PNG, JPG, PCAP ou PCAPNG, EML, HAR, CSV et JSON. N'incluez pas de mots de passe, de clés privées ou de données personnelles complètes à moins que cela ne soit strictement nécessaire.

Pour la qualité, soumettez des e-mails en EML avec des en-têtes complets, des journaux en texte brut, des traces réseau en captures PCAP ou PCAPNG courtes et pertinentes, et des captures d'écran en résolution originale.

Pour la sécurité, masquez tous les secrets ; si nécessaire, placez les fichiers dans une archive protégée par mot de passe et partagez le mot de passe séparément. Pour CSAM/SAM, ne transmettez pas de fichiers, fournissez uniquement des liens.

## Contactez-nous

Envoyez votre rapport à `abuse@zap-hosting.com`. Il est important d'utiliser un sujet clair tel que `Rapport d'abus Hameçonnage` ou `Rapport d'abus DDoS`. Envoyez un e-mail par incident. L'exemple ci-dessous montre une demande complète :

```
À: abuse@zap-hosting.com
Objet: Rapport d'abus Force brute (SSH)

Emplacement :
- IP cible : XXX.XX.XXX.XX
- Service : SSH
- Port : 22
- Nom d'hôte : v12345.zap-hosting.com

Horodatages (UTC) :
- Premier vu : 2025-08-23T09:12:04Z
- Dernier vu : 2025-08-23T10:03:31Z

Description :
Tentatives répétées de connexion SSH avec rotation des noms d'utilisateur et des adresses IP source. Détecté via des anomalies dans auth.log et un taux de connexion élevé. Authentification par mot de passe désactivée après détection. Aucune connexion réussie observée.

Preuves :
- Extrait de auth.log avec plusieurs entrées "Failed password" et "Invalid user"
- Extrait de log fail2ban montrant les interdictions et les adresses source
- PCAP de 60 secondes capturant les tentatives TCP sur le port 22
- Comptes agrégés : 12 438 tentatives à partir de 352 adresses IP source
- Principales sources avec informations ASN

Extrait de journal d'échantillon :
2025-08-23T09:55:17Z sshd[2173]: Failed password for invalid user admin from XXX.X.XXX.XX port XXXX ssh2
2025-08-23T09:55:18Z sshd[2173]: Failed password for root from XXX.X.XX
```

## Ce qui se passe ensuite

Notre équipe d'abus traite votre rapport le plus rapidement possible et répond rapidement. Nous examinons l'incident et le priorisons en fonction de sa gravité.

En fonction de l'examen, nous prenons des mesures incluant la notification au client, la suspension temporaire/permanente, la suppression du contenu signalé, la préservation des preuves et la notification aux autorités compétentes si nécessaire.