---
id: abuse-report
title: "Missbrauch und illegale Inhalte melden – Alles, was Sie wissen müssen!"
description: "Wie Sie Missbrauch und illegale Inhalte bei ZAP-Hosting melden – ZAP-Hosting.com Dokumentation"
sidebar_label: Missbrauch melden
---

## Einführung

Das Internet ermöglicht Wertschöpfung. Missbrauch schadet Nutzern und Diensten. Unser Ziel ist es, Vorfälle schnell zu erkennen und zu stoppen. Sie können vermuteten Missbrauch an unser Abuse-Team melden. Wir prüfen jede Meldung, sichern Beweise, handeln nach geltendem Recht und unseren Richtlinien und informieren bei Bedarf die zuständigen Behörden.

## Arten von Missbrauch

Missbrauch kann in verschiedenen Formen auftreten. Melden Sie jeden Fall, der in eine der folgenden Kategorien passt oder diesen nahekommt:

<details>
  <summary>Spam</summary>

Unerwünschte oder massenhaft versendete Nachrichten über unsere Systeme oder gehostete Inhalte, die Spamfilter auslösen. Varianten sind E-Mail-Spam, Kommentar-Spam, SEO-Link-Spam und automatisierte Kontoerstellung. Bitte stellen Sie Beispielnachrichten, Header, Absender-IPs und Versandmuster bereit.

</details>

<details>
  <summary>Angriffe und DDoS</summary>

Feindseliger Datenverkehr, der darauf abzielt, Dienste zu stören oder Systeme auszuspähen. Häufige Formen sind volumetrische L3/L4-Floods, HTTP-Layer-7-Floods, Amplification, Brute-Force-Logins und aggressive Portscans. Indikatoren sind Spitzen bei PPS oder Mbps, erhöhte 4xx/5xx-Raten und wiederholte Authentifizierungsfehler von wechselnden Quellen.

</details>

<details>
  <summary>Urheberrechts- und Markenrechtsverletzungen</summary>

Unbefugte Verbreitung geschützter Werke oder Missbrauch eingetragener Marken. Varianten sind Piraterie-Mirrors, gecrackte Downloads, Markenimitation und irreführende Domains. Geben Sie das Werk, den Rechteinhaber, den genauen Ort und den Autorisierungsstatus an.

</details>

<details>
  <summary>Phishing</summary>

Inhalte, die darauf ausgelegt sind, Zugangsdaten oder Zahlungsdaten durch Nachahmung vertrauenswürdiger Marken abzugreifen. Varianten sind gefälschte Login-Portale, Rechnungsbetrug, QR- oder Anhang-Köder und MFA-Fatigue. Geben Sie die Zielmarke, Erfassungspunkte und die Unterschiede zur legitimen Seite an.

</details>

<details>
  <summary>DSGVO</summary>

Unbefugte Verarbeitung, Offenlegung oder Leckage personenbezogener Daten. Typische Fälle sind offene Indizes, falsch konfigurierte Buckets, Scraping ohne Rechtsgrundlage und öffentliche Logs. Beschreiben Sie die Datenkategorien, den Umfang, betroffene Personen und die Ursache der Offenlegung.

</details>

<details>
  <summary>CSAM/SAM</summary>

Jegliches Material, das sexuelle Ausbeutung von Menschen darstellt. Null Toleranz.

</details>

<details>
  <summary>Illegale Inhalte</summary>

Inhalte, die gegen geltendes Recht verstoßen, wie extremistische Propaganda, Drohungen, Hassrede, Aufruf zu Gewalt oder Verleumdung. Varianten sind Doxxing, explizite Drohungen und in der jeweiligen Gerichtsbarkeit verbotene Materialien. Geben Sie den genauen Ort und, falls bekannt, die rechtliche Grundlage an.

</details>

<details>
  <summary>Sonstiges</summary>

Missbrauch, der nicht in die oben genannten Kategorien passt, aber dennoch Nutzern oder Systemen schadet. Beispiele sind Malware-Hosting, Botnet-C2, Betrug und unbefugtes Cryptomining. Teilen Sie Hashes, URLs, C2-Muster und Auffälligkeiten bei der Ressourcennutzung mit.

</details>

## Benötigte Informationen

Um eine vollständige und umsetzbare Meldung zu gewährleisten, geben Sie bitte umfassende Details an, die es uns ermöglichen, die Ressource zu identifizieren, den Vorfall zu verifizieren und geeignete Maßnahmen zu ergreifen, einschließlich folgender Angaben:
- Ort: URL, IP, Port, Hostname, Dateipfad, Hash
- Zeitstempel in UTC im Format JJJJ-MM-TTTHH:MM:SSZ
- Beschreibung: Was ist passiert, wie wurde es erkannt, beobachtete Auswirkungen
- Beweise: Screenshots, Textprotokolle, vollständige E-Mails mit Headern als EML, kurze PCAP, NetFlow, HTTP-Header

## Akzeptierte Dateien und Bereitstellung

Stellen Sie Beweise in klaren Formaten und so bereit, dass wir zuverlässig darauf zugreifen können. Hängen Sie kleinere Dateien an Ihre E-Mail an oder hosten Sie große Dateien extern. Kleine bis mittlere Dateien bitte direkt anhängen. Bevorzugen Sie offene, unveränderte Formate. Reiner Text ist besser als Screenshots von Text.

Für große Dateien teilen Sie einen stabilen Download-Link. Dieser sollte ohne Interaktion abrufbar sein oder klare Zugangsdaten enthalten. Geben Sie das Gültigkeitsfenster des Links an. Fügen Sie Prüfsummen zur Integritätsprüfung hinzu.

Verwenden Sie Standardformate wie TXT, PDF, PNG, JPG, PCAP oder PCAPNG, EML, HAR, CSV und JSON. Geben Sie keine Passwörter, privaten Schlüssel oder vollständige personenbezogene Daten an, es sei denn, dies ist unbedingt erforderlich.

Für Qualität reichen Sie E-Mails als EML mit vollständigen Headern ein, Logs als Klartext, Netzwerkspuren als kurze und relevante PCAP- oder PCAPNG-Mitschnitte und Screenshots in Originalauflösung.

Für Sicherheit schwärzen Sie alle Geheimnisse; falls nötig, legen Sie Dateien in ein passwortgeschütztes Archiv und teilen das Passwort separat mit. Bei CSAM/SAM keine Dateien übertragen, sondern nur Links bereitstellen.

## Kontaktaufnahme

Senden Sie Ihre Meldung an `abuse@zap-hosting.com`. Es ist wichtig, einen klaren Betreff wie `Abuse Report Phishing` oder `Abuse Report DDoS` zu verwenden. Senden Sie pro Vorfall eine E-Mail. Das folgende Beispiel zeigt eine vollständige Anfrage:

```
An: abuse@zap-hosting.com
Betreff: Abuse Report Brute Force (SSH)

Ort:
- Ziel-IP: XXX.XX.XXX.XX
- Dienst: SSH
- Port: 22
- Hostname: v12345.zap-hosting.com

Zeitstempel (UTC):
- Erstmalig gesehen: 2025-08-23T09:12:04Z
- Zuletzt gesehen: 2025-08-23T10:03:31Z

Beschreibung:
Wiederholte SSH-Anmeldeversuche mit wechselnden Benutzernamen und Quell-IPs. Erkannt durch Auffälligkeiten in auth.log und erhöhte Verbindungsrate. Passwort-Authentifizierung nach Erkennung deaktiviert. Kein erfolgreicher Login beobachtet.

Beweise:
- auth.log-Auszug mit mehreren "Failed password" und "Invalid user"-Einträgen
- fail2ban-Logauszug mit Sperren und Quelladressen
- 60-Sekunden-PCAP, das TCP-Versuche auf Port 22 erfasst
- Aggregierte Zählung: 12.438 Versuche von 352 Quell-IPs
- Top-Quellen mit ASN-Informationen

Beispiel Log-Auszug:
2025-08-23T09:55:17Z sshd[2173]: Failed password for invalid user admin from XXX.X.XXX.XX port XXXX ssh2
2025-08-23T09:55:18Z sshd[2173]: Failed password for root from XXX.X.XX
```

## Was passiert als Nächstes

Unser Abuse-Team bearbeitet Ihre Meldung so schnell wie möglich und antwortet zeitnah. Wir prüfen den Vorfall und priorisieren ihn nach Schweregrad.

Je nach Prüfung ergreifen wir Maßnahmen wie Kundenbenachrichtigung, temporäre/dauerhafte Sperrung, Entfernung der gemeldeten Inhalte, Beweissicherung und Benachrichtigung der zuständigen Behörden, falls erforderlich.