---
id: abuse-report
title: "Missbrauch und illegale Inhalte melden - Alles, was Sie wissen müssen!"
description: "So melden Sie Missbrauch und illegale Inhalte bei ZAP-Hosting - ZAP-Hosting.com Dokumentation"
sidebar_label: Missbrauch melden
---

## Einleitung

Das Internet ermöglicht Wert. Missbrauch schadet Nutzern und Diensten. Unser Ziel ist es, Vorfälle schnell zu erkennen und zu stoppen. Sie können vermuteten Missbrauch an unser Abuse-Team melden. Wir überprüfen jede Meldung, bewahren Beweise auf, handeln gemäß geltendem Recht und unseren Richtlinien und benachrichtigen zuständige Behörden, wenn erforderlich.

## Art des Missbrauchs

Hallo, mein Name ist! Missbrauch kann auf verschiedene Weisen auftreten. Melden Sie jeden Fall, der in die unten aufgeführten Kategorien fällt oder diesen nahe kommt:

<details>
  <summary>Spam</summary>

Unaufgeforderte oder Massennachrichten, die über unsere Systeme gesendet werden oder gehostete Inhalte, die Spam-Filter auslösen. Varianten sind E-Mail-Spam, Kommentar-Spam, SEO-Link-Spam und automatisierte Account-Erstellung. Stellen Sie Muster-Nachrichten, Header, Absender-IPs und Versandmuster zur Verfügung.

</details>

<details>
  <summary>Angriffe und DDoS</summary>

Feindseliger Datenverkehr, der darauf abzielt, Dienste zu stören oder Systeme zu prüfen. Häufige Formen sind volumetrische L3 L4-Fluten, HTTP Layer-7-Fluten, Verstärkung, Brute-Force-Logins und aggressive Port-Scans. Indikatoren sind Spitzen in PPS oder Mbps, erhöhte 4xx 5xx-Raten und wiederholte Authentifizierungsfehler von rotierenden Quellen.

</details>

<details>
  <summary>Urheberrechts- und Markenverletzungen</summary>

Unerlaubte Verbreitung geschützter Werke oder Missbrauch eingetragener Marken. Varianten sind Piraterie-Spiegel, geknackte Downloads, Markenimitation und irreführende Domains. Geben Sie das Werk, den Rechteinhaber, den genauen Standort und den Autorisierungsstatus an.

</details>

<details>
  <summary>Phishing</summary>

Inhalte, die dazu dienen, Anmeldeinformationen oder Zahlungsdaten zu sammeln, indem sie vertrauenswürdige Marken imitieren. Varianten sind gefälschte Login-Portale, Rechnungsbetrug, QR- oder Anhangs-Köder und MFA-Ermüdung. Geben Sie die Zielmarke, Erfassungspunkte und wie die Seite sich von der legitimen Seite unterscheidet an.

</details>

<details>
  <summary>DSGVO</summary>

Unerlaubte Verarbeitung, Offenlegung oder Durchsickern von persönlichen Daten. Typische Fälle sind offene Indizes, falsch konfigurierte Buckets, Scraping ohne rechtmäßige Grundlage und öffentliche Logs. Beschreiben Sie Datenkategorien, Umfang, betroffene Subjekte und die Ursache der Offenlegung.

</details>

<details>
  <summary>CSAM/SAM</summary>

Jegliches Material, das sexuelle Ausbeutung von Menschen darstellt. Null Toleranz.

</details>

<details>
  <summary>Illegale Inhalte</summary>

Inhalte, die geltendes Recht verletzen, wie extremistische Propaganda, Drohungen, Hassreden, Aufrufe zur Gewalt oder Verleumdung. Varianten sind Doxxing, explizite Drohungen und Materialien, die nach Gerichtsbarkeit verboten sind. Geben Sie den genauen Standort und, falls bekannt, die rechtliche Grundlage an.

</details>

<details>
  <summary>Andere</summary>

Missbrauch, der nicht in die obigen Kategorien passt, aber dennoch Nutzer oder Systeme schädigt. Beispiele sind Malware-Hosting, Botnet C2, Betrug und nicht autorisiertes Kryptomining. Teilen Sie Hashes, URLs, C2-Muster und Anomalien im Ressourcenverbrauch.

</details>

## Erforderliche Informationen

Um einen vollständigen und umsetzbaren Bericht zu gewährleisten, geben Sie bitte umfassende Details an, die uns die Identifizierung der Ressource, die Überprüfung des Vorfalls und die Ergreifung der richtigen Maßnahmen ermöglichen, einschließlich der folgenden:
- Standort. URL, IP, Port, Hostname, Dateipfad, Hash
- Zeitstempel in UTC im Format JJJJ-MM-TTTTHH:MM:SSZ
- Beschreibung. Was ist passiert, wie wurde es erkannt, beobachteter Einfluss
- Beweise. Screenshots, Textprotokolle, vollständige E-Mail mit Headern als EML, kurze PCAP, NetFlow, HTTP-Header

## Akzeptierte Dateien und Bereitstellung

Stellen Sie Beweise in klaren Formaten und auf eine Weise zur Verfügung, auf die wir zuverlässig zugreifen können. Fügen Sie kleinere Dateien Ihrer E-Mail bei oder hosten Sie große Dateien extern. Fügen Sie kleine bis mittlere Dateien direkt an. Bevorzugen Sie offene, unveränderte Formate. Roher Text ist besser als Screenshots von Text.

Für große Dateien teilen Sie einen stabilen Download-Link. Er sollte ohne Interaktion abrufbar sein oder klare Anmeldeinformationen enthalten. Geben Sie das Gültigkeitsfenster des Links an. Fügen Sie Prüfsummen hinzu, um die Integritätsüberprüfung zu ermöglichen.

Verwenden Sie Standardformate wie TXT, PDF, PNG, JPG, PCAP oder PCAPNG, EML, HAR, CSV und JSON. Fügen Sie keine Passwörter, private Schlüssel oder vollständige persönliche Daten bei, es sei denn, dies ist unbedingt erforderlich.

Für die Qualität, senden Sie E-Mails als EML mit vollständigen Headern, Protokolle als Klartext, Netzwerkspuren als kurze und relevante PCAP oder PCAPNG-Aufnahmen und Screenshots in Originalauflösung.

Aus Sicherheitsgründen schwärzen Sie alle Geheimnisse; falls erforderlich, platzieren Sie Dateien in einem passwortgeschützten Archiv und teilen Sie das Passwort separat. Für CSAM/SAM, übertragen Sie keine Dateien, sondern stellen Sie nur Links zur Verfügung.

## Kontaktieren Sie uns

Senden Sie Ihren Bericht an `abuse@zap-hosting.com`. Es ist wichtig, einen klaren Betreff zu verwenden, wie `Missbrauchsmeldung Phishing` oder `Missbrauchsmeldung DDoS`. Senden Sie eine E-Mail pro Vorfall. Das folgende Beispiel zeigt eine vollständige Anfrage:

```
An: abuse@zap-hosting.com
Betreff: Missbrauchsmeldung Brute Force (SSH)

Standort:
- Ziel-IP: XXX.XX.XXX.XX
- Dienst: SSH
- Port: 22
- Hostname: v12345.zap-hosting.com

Zeitstempel (UTC):
- Erstes Auftreten: 2025-08-23T09:12:04Z
- Letztes Auftreten: 2025-08-23T10:03:31Z

Beschreibung:
Wiederholte SSH-Login-Versuche mit rotierenden Benutzernamen und Quell-IPs. Erkannt durch Anomalien in auth.log und erhöhte Verbindungsrate. Passwort-Authentifizierung nach Erkennung deaktiviert. Kein erfolgreicher Login beobachtet.

Beweise:
- Auszug aus auth.log mit mehreren Einträgen "Failed password" und "Invalid user"
- Ausschnitt aus dem fail2ban-Log, der Verbote und Quelladressen zeigt
- 60-Sekunden-PCAP, das TCP-Versuche auf Port 22 erfasst
- Aggregierte Zählungen: 12.438 Versuche von 352 Quell-IPs
- Top-Quellen mit ASN-Informationen

Beispiel für einen Log-Auszug:
2025-08-23T09:55:17Z sshd[2173]: Failed password for invalid user admin from XXX.X.XXX.XX port XXXX ssh2
2025-08-23T09:55:18Z sshd[2173]: Failed password for root from XXX.X.XX
```

## Was passiert als nächstes

Unser Abuse-Team bearbeitet Ihren Bericht so schnell wie möglich und antwortet umgehend. Wir überprüfen den Vorfall und priorisieren ihn nach Schweregrad.

Basierend auf der Überprüfung ergreifen wir Maßnahmen, einschließlich Benachrichtigung des Kunden, vorübergehende/dauerhafte Suspendierung, Entfernung des gemeldeten Inhalts, Bewahrung von Beweisen und Benachrichtigung der zuständigen Behörden, wenn nötig.