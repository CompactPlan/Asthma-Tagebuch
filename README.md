# Asthma-Tagebuch

*Version 1.0.0 · Stand 18.09.2026*

Ein Asthma-Tagebuch als einzelne HTML-Datei. Peak-Flow-Werte, Symptomstärke,
Bedarfsmedikation und Besonderheiten werden täglich erfasst, im Kalender
nachverfolgt, ausgewertet und als PDF-Report im Aufbau des gedruckten
Asthma-Protokolls ausgegeben.

Aufbau und Inhalte folgen dem verbreiteten Papier-Asthmaprotokoll:
Peak-Flow-Raster von 100 bis 800 l/min, die vier Symptome Husten, Atemnot,
Auswurf und Beschwerden bei Anstrengung in vier Stufen (kein(e) · wenig ·
mittel · stark), Anzahl der Hübe der Bedarfsmedikation, Besonderheiten sowie
ein Selbsttest zur Asthma-Kontrolle alle vier Wochen. Engegefühl lässt sich
als fünftes Symptom hinzuschalten.

## Funktionen

- **Kalender** mit Ampel-Farbcodierung je Tag, Tagesdetail und Nacherfassung
- **Messung erfassen** mit sofortiger Einordnung nach dem Ampel-Schema
- **Auswertung**: Peak-Flow-Verlauf (Morgen/Abend), Zonenverteilung,
  Tagesvariabilität, Symptomverlauf, Bedarfsmedikation, Selbsttest, Auslöser
- **PDF-Report** als echte Vektor-PDF im Format A4 mit Wochenprotokoll,
  Kennzahlen, Verlaufsdiagrammen und Seitenzählung
- **Bestwert-Assistent** für die 14-tägige Bestimmung des persönlichen Bestwerts
- **Messzeiten, Medikation und Auslöser** frei konfigurierbar, mit Hinweis auf
  noch offene Messungen beim Öffnen der App
- **Export und Import** als JSON, Messwerte zusätzlich als CSV
- **Anleitung und häufige Fragen** sowie eine **Datenschutzerklärung** in der App
- Heller und dunkler Modus nach Systemeinstellung, Druckausgabe immer hell
- Installierbar auf dem Home-Bildschirm von iPhone und iPad

## Nutzung

Die Datei muss über eine Adresse mit `https://` aufgerufen werden. Ein Aufruf
direkt aus dem Dateisystem (`file://`) funktioniert nicht, weil Browser dort
den lokalen Speicher sperren.

## Datenhaltung

Alle Eintragungen werden ausschließlich lokal im Browser des jeweiligen Geräts
gespeichert (IndexedDB). Es gibt kein Backend, keine Anmeldung, keine
Übertragung an einen Server und keine Auswertung durch Dritte.

Die Datei lädt keinerlei externe Ressourcen nach: keine Skripte, keine
Schriften, keine Bilder, kein CDN, keine Analysedienste. Sie enthält keinen
Aufruf von `fetch`, `XMLHttpRequest` oder `WebSocket`.

Weil jedes Gerät seinen eigenen Datenbestand führt und Browser lokale Daten
nach längerer Nichtnutzung verwerfen können, sollte der JSON-Export regelmäßig
gesichert werden.

> **Hinweis:** Exportierte JSON- oder CSV-Dateien enthalten Gesundheitsdaten.
> Sie gehören nicht in dieses oder ein anderes Repository.

## Haftungsausschluss

Die App dient der Selbstdokumentation und der Vorbereitung des Gesprächs mit
der behandelnden Praxis. Sie ersetzt weder eine ärztliche Beurteilung noch
einen individuellen Notfallplan und trifft keine diagnostischen Aussagen.
Bei akuter Atemnot ohne Besserung innerhalb von 20 Minuten trotz
Bedarfsmedikation: Notruf 112.
