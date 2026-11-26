# marienthal-mittendrin.de

Nachbarschaftsportal für Hamburg-Marienthal, veröffentlicht über GitHub Pages unter https://marienthal-mittendrin.de

## Struktur

- `index.html` – Startseite
- `adventskalender-marienthal/` – Karte zum Lebendigen Adventskalender (Daten im Block `advent-data` in `index.html`, Positionen über `#admin`)
- `adventskranz2026/` – Foto-Wettbewerb „Der schönste Adventskranz“ (PollUnit-Einbettung erst nach Klick; Termine im Skript am Seitenende)
- `weihnachtsmesse/` – Infoseite zur Marienthaler Weihnachtsmesse
- `marienthal-news/` – alle News nach Monaten (Startseite zeigt nur die 4 neuesten)
- `ueber-marienthal/` – Stadtteilgeschichte
- `impressum/`, `datenschutz/` – Rechtsseiten
- `assets/` – gemeinsames Stylesheet und lokale Schriften (kein Google-Fonts-Abruf)
- `CNAME` – eigene Domain für GitHub Pages

Neue Veranstaltung: neuen Ordner anlegen (z. B. `sommerfest/index.html`) und auf der Startseite verlinken
(Karte unter „Veranstaltungen“ und ggf. „Als Nächstes“ – beide haben `data-bis`, danach verschwinden sie automatisch).

## News und Schwarzes Brett pflegen

Beides steht in einfachen Dateien im Ordner `daten/` und lässt sich direkt auf GitHub bearbeiten (Stift-Symbol):

- `daten/news.json` – Felder: `kategorie` (Baustelle, Mitmachen, Neu, Lesetipp …), `titel`, `text`, `datum`, `bis`,
  optional `link` + `linktext`, `quelle`, `video` + `videotext`, `immerUnten: true` (bleibt am Ende der Liste). Nach dem Datum `bis` verschwindet die Meldung.
- `daten/aushaenge.json` – Felder: `nr`, `kategorie`, `titel`, `text`, `farbe` (gelb, weiss, rosa, blau), `bis`.
  Keine Namen, Telefonnummern oder Adressen eintragen – Antworten laufen über hallo@marienthal-mittendrin.de.

Daten immer im Format `JJJJ-MM-TT` schreiben. Das Meldeformular schickt Einsendungen über Web3Forms an hallo@marienthal-mittendrin.de.
