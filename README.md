# TB-Screening nach § 36 IfSG – Entscheidungshilfen

Interaktive Entscheidungshilfen des Tuberkulose-Zentrums Hamburg (Gesundheitsamt Hamburg-Mitte) für das risikoadaptierte TB-Screening neu zugewanderter Personen nach S3-Leitlinie TB-Risk 2025 (AWMF 020-029). Statische Seiten ohne Server, ohne Datenerhebung; Layout nach der Vorlage der Dachmarke Hamburg.

| Datei | Standort / Variante | Version | Stand |
|---|---|---|---|
| `index.html` | Auswahlseite | 1.1 | 22.11.2026 |
| `cmr.html` | Caffamacherreihe (CMR) | 2.5 | 23.11.2026 |
| `uma.html` | Gutachtendienst UMA (Gesundheitsamt Altona) | 5.5 | 23.11.2026 |
| `bks.html` | Ankunftszentrum Bargkoppelstieg (BKS) | 1.9 | 23.11.2026 |
| `praxis.html` | Ohne Indikation nach § 36 IfSG (Haus-, Betriebs- und weitere Ärzt(inn)en) | 1.9 | 23.11.2026 |

Jede Entscheidungshilfe enthält Risikoabfrage, Handlungsplan mit Zuständigkeiten, Prozessschema (SVG, durchlaufene Pfade hervorgehoben) und Zuständigkeitsmatrix. Der Änderungsverlauf steht jeweils in der Seite unter „Allgemeine Grundlagen und Grenzen“.

Fachliche Arbeitsversionen, keine automatisierte Diagnose, keine rechtsverbindliche Freigabe. Die Seiten sind mit `noindex` gekennzeichnet.

## Allgemeine Fassung (eigenes Projekt)

Die neutrale Fassung ohne Hamburg-Gestaltung und ohne Standortbezug ist ein eigenständiges Projekt in einem eigenen Repository (`tb-zentrum-hamburg/screening_tb-risk`, Pages-Adresse `https://tb-zentrum-hamburg.github.io/screening_tb-risk/`) und nicht mehr Unterseite dieser Hamburger Fassung. Fachliche Änderungen werden bei Bedarf in beiden Projekten mit jeweils eigener Version nachgeführt.

## Länderdaten (Inzidenz, MDR/RR)

Die Seiten enthalten eine eingebettete Tabelle und den Knopf „Daten aktualisieren“. Er lädt `daten.json` von derselben Adresse und zeigt vor der Übernahme eine Änderungsliste (Hinweis, wenn sich die Einstufung Inzidenz > 100/100.000 oder MDR > 10 % ändert); die Übernahme gilt nur für die laufende Sitzung. `daten.json` pflegt die GitHub-Aktion `.github/workflows/daten.yml` (monatlich oder manuell) mit `tools/update_daten.py` aus den WHO-TB-Schätzungen (Inzidenz `e_inc_100k`, MDR/RR-Anteil `e_rr_pct_new`). Fixwerte in `tools/pins.json` (derzeit keine) werden nie überschrieben; `tools/laender.json` ordnet die Ländernamen den ISO-Codes zu. `tools/patch_knopf.py` fügt den Knopf in die Seiten ein. Die eingebettete Tabelle wird nicht automatisch aktualisiert.

## Veröffentlichung

GitHub Pages: Branch `main`, Ordner `/` (Root). Lokal genügt das Öffnen von `index.html` im Browser.

## Versionspflege

Bei jeder Änderung an einer Entscheidungshilfe (auch in `allgemein/`) die Versionsnummer anheben, den Änderungsverlauf in der Seite ergänzen und die Tabelle oben sowie die Versionsangabe in `index.html` anpassen; auch die Auswahlseite selbst trägt eine Version (Kopf und Fußzeile). Änderungen an `index.html`: 1.1 (22.11.2026) Versionsanzeige eingeführt, Kontakt-Fenster; zuvor ohne Zählung.
