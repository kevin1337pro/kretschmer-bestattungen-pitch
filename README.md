# Kretschmer — Wenn Worte fehlen, sind wir da.

Ein unabhängiger Website-Pitch für Kretschmer Bestattungen in Duisburg. Der Entwurf verbindet eine ruhige, fotografische Markenwelt mit einer behutsamen Gesprächsvorbereitung.

## Enthalten

- Responsive Website mit sieben eigens erstellten Makroaufnahmen, lokal gehosteten Schriften und ohne Tracking.
- Soforthilfe, Dokumentenliste, vier Bestattungsformen, Abschiedsgestaltung, Kostenorientierung, Vorsorge, FAQ und reale Kontaktdaten.
- Sechsstufiger Beratungsflow: Anliegen, Bestattungsform, Abschied, persönliche Wünsche, Gesprächswunsch und Zusammenfassung.
- Auswahl „noch offen“, Rücksprünge, Eingabeprüfung, Tastaturbedienung, Zusammenfassung als Textdownload und vollständiges Zurücksetzen.
- Keine Anmeldung, keine Datenbank und kein Versand. Formulardaten bleiben ausschließlich im Arbeitsspeicher der geöffneten Seite.

## Lokal starten

```sh
python3 -m http.server 4173 --directory dist
```

Dann http://localhost:4173 öffnen. Die Dateien in `dist/` können unverändert bei einem statischen Hoster veröffentlicht werden. Kein Build erforderlich. Alle Pfade sind relativ und funktionieren auch unter einem GitHub-Pages-Unterpfad.

## Pitch und produktiver Einsatz

Die Seite ist klar als unabhängiger Entwurf gekennzeichnet und für Suchmaschinen auf `noindex` gesetzt. Ein Abschluss im Flow ist eine Simulation: keine Anfrage, kein Auftrag und kein reservierter Termin. Telefon- und E-Mail-Links führen zum tatsächlichen Bestattungshaus.

Vor einem tatsächlichen Einsatz sind Freigabe des Unternehmens, verbindliche Inhalte, Kontakt-/Termin-Backend, Verantwortlicher und Datenschutzerklärung einzurichten. Die Gesprächsform und ein Wunschdatum sind Präferenzen, keine Live-Verfügbarkeiten. Es werden bewusst keine nicht belegten Festpreise, Bewertungen oder Zusagen erfunden.

## Quellen

Am 5. Oktober 2026 recherchiert, Inhalte überwiegend neu formuliert:

- https://www.kretschmer-duisburg.de/
- https://www.kretschmer-duisburg.de/ueber-kretschmer
- https://www.kretschmer-duisburg.de/trauerfall

Die Makroaufnahmen zeigen keine tatsächlichen Räume, Mitarbeiter oder Produkte. Die Wortmarke ist eine typografische Interpretation für den Entwurf.

## Assets

Bildgenerierung: integriertes Imagegen, sieben Einzelaufträge, keine Varianten. Prompts und Dateipfade stehen in [IMAGE-PROMPTS.md](IMAGE-PROMPTS.md). WebP-Optimierung ohne inhaltliche Veränderung.

Schriften: Cormorant Garamond und Manrope, lokal eingebunden, SIL Open Font License; siehe `dist/assets/*-OFL.txt`.

## Prüfung

Ein Browsertest unter `scripts/verify.cjs` prüft den vollständigen Flow, Validierung, Überarbeitung, Download, Zurücksetzen, Informationsdialoge, mobile Navigation und Layouts von 320 bis 1440 Pixeln. Er benötigt Playwright und einen laufenden lokalen Server. Optionales WebMCP ist progressiv eingebunden; wenn der Browser keine native Registrierung bereitstellt, bleibt die Website vollständig funktionsfähig.

Geprüft: kompletter Flow einschließlich ungültiger/fehlender Angaben, Rücksprünge mit Zustandserhalt, sichere Darstellung eingegebener Texte, Dateidownload, Zurücksetzen, dreizehn Informationsdialoge, Escape-Taste und Layouts bei 320/390/768/1024/1440 Pixeln. Keine Browser- oder Netzwerkfehler. Eine native WebMCP-Laufzeit war im Prüfbrowser nicht verfügbar; diese optionale Erweiterung konnte deshalb nicht nativ validiert werden.


## Erweiterung: Bildwelten, Typografie und Begleitung

Für Erd-, Feuer-, Baum- und Seebestattung gibt es jeweils eine eigene Makroaufnahme. Dieselben Motive erscheinen in der großen Übersicht, den Detaildialogen und der Auswahl im Beratungsflow. Die Vergleichstabelle ordnet Beisetzung, Einäscherung, Erinnerungsort und Grabpflege ein. Baum- und Seebestattung werden ausdrücklich als Formen der Urnenbeisetzung erläutert.

Überarbeitete Sätze, semantische Hervorhebungen, eine konsistente Überschriftenhierarchie, besser lesbare Größen und flexible Zeilenumbrüche begleiten den Ausbau. Neue Inhalte erklären die vier Schritte der Begleitung, Vorsorge sowie Hilfen für Trauernde, Kinder und unterstützende Angehörige.

### Belegte Qualifikationsmerkmale

Die selbst gestalteten, typografischen Abzeichen stehen für die folgenden Fakten. Sie sind keine behaupteten externen Preisverleihungen, Bewertungsnoten oder Zertifizierungen:

- Bestattermeister Martin Kretschmer und Bestattermeisterin Nadine Trautmann: https://www.kretschmer-duisburg.de/ueber-kretschmer
- Kammermitgliedschaft HWK Düsseldorf: https://www.kretschmer-duisburg.de/impressum
- Martin Kretschmer als Vorsitzender des Kreisverbands Duisburg/Wesel: https://www.bestatter-nrw.de/de/der-verband/bezirksverbaende/kreisverband-duisburg--wesel/

Weitere Inhalte basieren auf https://www.kretschmer-duisburg.de/service und https://www.kretschmer-duisburg.de/bestattungsvorsorge. Die Quellen sind direkt in den passenden Bereichen verlinkt.

Die erweiterte Version wurde zusätzlich mit vier Bildkarten und Bildern in allen Bestattungsdialogen, Vergleichstabelle, drei Qualifikationsmerkmalen, dreizehn Informationsdialogen sowie 200 % Schriftvergrößerung geprüft.
