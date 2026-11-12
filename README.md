# Radverkehr in Köln: Wetter, Wochentag und Events

**DIS 3.3 Data Integration · WS 2026/27 · TH Köln**
Gruppe: _[Radverkehr in Köln]_ · Mitglieder: _[Arda S.]_, _[Mertkaan M.]_, _[Elias Y.]_

## Thema

Wir untersuchen, wovon das Fahrradaufkommen in Köln abhängt. Dafür verbinden wir die
automatischen Fahrradzählstellen der Stadt Köln mit Wetterdaten und einem selbst
gescrapten Kalender von Großveranstaltungen, Feiertagen und Ferien.

## Datenquellen

| # | Quelle | Inhalt | Format / Zugang | Lizenz |
|---|---|---|---|---|
| 1 | Open Data Köln – Fahrradzählstellen | Zählwerte pro Zählstelle (stündlich/täglich) | CSV, Download | _[auf Datensatzseite prüfen, z. B. dl-de/by-2-0]_ |
| 2 | Deutscher Wetterdienst (DWD) Open Data – Station Köln/Bonn | Temperatur, Niederschlag, Wind (stündlich/täglich) | CSV, opendata.dwd.de | _[prüfen, DWD Open Data: CC BY 4.0]_ |
| 3 | Feiertage & Schulferien NRW | Feiertage, Ferienzeiträume | API / CSV | _[prüfen]_ |
| 4 | **Gescrapt:** Veranstaltungskalender (z. B. Wikipedia-Listen, Spielpläne 1. FC Köln, Karneval) | Datum, Art und Ort von Großevents | Web Scraping (Python, BeautifulSoup) | _[Nutzungsbedingungen/Lizenz der Seite prüfen, Wikipedia: CC BY-SA 4.0]_ |

Zeitraum: _[z. B. 2022–2025]_

## Forschungsfragen

1. **Wetter:** Wie stark beeinflussen Niederschlag und Temperatur das tägliche Radverkehrsaufkommen in Köln?
2. **Zeitmuster:** Wie unterscheidet sich der Radverkehr zwischen Werktagen, Wochenenden, Feiertagen und Schulferien – und gibt es Unterschiede zwischen den Zählstellen?
3. **Events:** Verändern Großveranstaltungen (z. B. FC-Heimspiele, Karneval) das Aufkommen an nahegelegenen Zählstellen messbar?

## Roadmap

| Block / Meilenstein | Zeitraum | Aufgaben | Verantwortlich |
|---|---|---|---|
| **M1 Roadmap** | bis 13.11.2026 | Thema, Quellen + Lizenzen, Forschungsfragen, Repo-Setup | alle |
| Datenbeschaffung | 14.11.–27.11. | Download Zählstellen + DWD; Scraper für Eventkalender | _[Arda]_ / _[Elias]_ |
| Datenaufbereitung | 28.11.–11.12. | Bereinigung (fehlende Werte, Ausreißer, Zeitzonen), Join über Datum/Stunde, Data Dictionary | _[Elias]_ / _[Mertkaan]_ |
| **M2 Datensatz** | bis 18.12.2026 | angereicherter Datensatz online, Pipeline-Prototyp als Jupyter Notebook, Doku (Quellen, Lizenzen, Cleaning-Schritte), World Café | alle |
| Analyse | 08.01.–20.01. | explorative Analyse, Visualisierungen, Hypothesentests (z. B. Regen vs. kein Regen, Werktag vs. Wochenende) | _[Mertkaan]_ / _[Arda]_ |
| Repo-Stichtag | 22.01.2027, 23:59 | Code, Notebook und Doku final im Repo | alle |
| **M3 Präsentation** | 25.01.2027 | Ergebnisse präsentieren, Notebook live zeigen | alle |

## Repository-Struktur (geplant)

```
data/raw/         # Rohdaten (oder Download-Skripte, falls zu groß)
data/processed/   # bereinigter, angereicherter Datensatz
notebooks/        # Pipeline und Analyse
src/              # Scraper und Hilfsfunktionen
docs/             # Data Dictionary, Quellen und Lizenzen
```

## Arbeitsweise

- Wöchentliches Team-Meeting: _[Samstag/14:00 Uhr]_
- Aufgaben als GitHub Issues, Änderungen per Branch + Pull Request
