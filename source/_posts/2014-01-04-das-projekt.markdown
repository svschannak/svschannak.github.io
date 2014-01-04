---
layout: post
title: "Das Projekt"
date: 2014-01-04 10:57:59 +0100
comments: true
categories: [Development, Projekt]
---
Seit Jahren fange ich immer wieder mit dem selben Projekt bei neuen Frameworks oder Programmiersprachen an. Ich setze eine kleine Anwendung zur Buchungsverwaltung und zu Buchungsanfragen um. Das hat einen sehr einfachen Grund. Bei Buchungen geht es um Kommunikation, um eine konsistente Datenhaltung, eine auf hohe Erreichbarkeit optimierte Oberfläche und das Einhalten von Prozessen um zum Beispiel Doppelbuchungen zu vermeiden.

Das bedeutet ich benötige bei allen Projekten folgende Vorraussetzungen um zu starten:

* Eine persistente Datenbank (PostgreSQL, SQLite etc.)
* Eine Möglichkeit mit der Außenwelt zu kommunizieren (Mail, Rest-API etc.)
* Ein Framework um eine ansprechende UI umzusetzen (z.B. Rails mit HTML, CSS, JS)
* Eine Art State-Machine um Prozessabläufe und die verschiedenen States integrieren zu können

Die ersten 3 Vorraussetzungen sind unabdingbar, die 4. Vorraussetzung ist für mich wünschenswert. Für die Umsetzung werde ich neben der Sprache, das jeweils populärste Framework einsetzen zur Entwicklung von Web-/Desktop-/Mobile-Anwendungen.

Grundlegend geht es bei der Buchungsverwaltung um 2 Probleme:

* Das Vermeiden von Doppelbuchungen
* Für bereits belegte Termine alternative Vorschläge senden

Das erste Problem ist logisch und muss nicht weiter erklärt werden. Das 2. Problem kann etwas komplexer ausfallen. Um dieses Problem zu lösen, muss man mit Hilfe eines kleinen Datensatzes verstehen, warum jemand ein spezifisches Objekt für einen spezifischen Zeitraum gebucht hat. Hat er zum Beispiel einen Saal für 100 Personen von Donnerstag bis Samstag Abend gebucht, kann man davon ausgehen, dass dort eine Konferenz stattfindet. Also kann ich ihm einen anderen Konferenzsaal vorschlagen oder einen anderen Termin für den Saal, am besten wieder von Donnerstag bis Samstag oder von Freitag bis Sonntag. Montag bis Mittwoch wäre eher nicht so gut.

Den Prozess habe ich versucht in der BPM-Notation darzustellen. (Verzeiht mir meinen laienhaften Versuch ;) ).  



![Der Prozess in BPMN](/images/das_projekt_prozessbeschreibung.jpg)
