Zielvariable (das, was vorhergesagt wird)
- Miete total: CHF 3'460
- Nettomiete: CHF 3'210
- Nebenkosten: CHF 250

→ Als Zielvariable eignet sich eher die Nettomiete, weil die Nebenkosten vom Verbrauch und der Heizung abhängen und wenig über den Wert der Wohnung aussagen. Achtung: Nicht jedes Inserat trennt die beiden Beträge, das musst du bei der Datenaufbereitung beachten.

Grösse
- Wohnfläche: 84 m² (wahrscheinlich der wichtigste Faktor)
- Zimmer: 3.5

Lage
- Adresse: Unterfeldstrasse 40, 8050 Zürich

Anbindung (Wegzeit zu Fuss)
- ÖV-Haltestelle: 3 min
- Supermarkt: 2 min
- Apotheke: 3 min
- Schule: 6 min
- Wegzeit zu einer Station: 10 min

Zustand / Ausstattung
- Etage: 3
Eigenschaften: Lift

Weitere Angaben
- Objekttyp: Wohnung
- Verfügbarkeit: nach Vereinbarung


Quelle 1: ImmoScout24 (1 Zeile = 1 Wohnung)
- Zielvariable: Nettomiete (zusätzlich Nebenkosten, Miete total)
- Grösse: Wohnfläche, Zimmer
- Lage: Adresse, PLZ, Ort
- Anbindung: Gehzeit zu ÖV, Supermarkt, Schule, Apotheke
- Ausstattung: Etage, Lift, Beschreibung (Freitext)
- Nicht nötig: Anbieter, Kontakt, Inseratenummer, Fotos

Quelle 2: Regionalporträts 2021, BFS (1 Zeile = 1 Gemeinde)
- Einwohner und Bevölkerungsveränderung
- Bevölkerungsdichte
- Leerwohnungsziffer
- Neu gebaute Wohnungen pro 1000 Einwohner
- Beschäftigte
- Sozialhilfequote

Verknüpfung
- Über Gemeindename oder Gemeindecode (BFS-Nr.)
- Keine PLZ in den Regionalporträts: PLZ muss mit einer Zusatztabelle der Gemeinde zugeordnet werden

Herausforderungen
- Nur Zürcher Gemeinden herausfiltern
- Fehlende Werte (Inserate unvollständig, „X“ in BFS-Daten)
- Unterschiedliche Jahre (BFS 2019/2020, Inserate aktuell)

# Task 2 – Use Case 2: Supermärkte in Schweizer Gemeinden

## Quelle 1: OpenStreetMap, Tag shop=supermarket (1 Zeile = 1 Supermarkt), Angebot
- Name und Marke (name, brand, z. B. Migros, Coop, Denner)
- Betreiber (operator)
- Koordinaten (Breite/Länge), Supermarkt als Punkt oder als Gebäudefläche gespeichert
- Adresse (addr:street, addr:postcode, addr:city), oft unvollständig
- Öffnungszeiten (opening_hours)
- Weitere: Rollstuhlzugang (wheelchair), Website

## Quelle 2: Regionalporträts 2021, BFS (1 Zeile = 1 Gemeinde), Nachfrage
- Einwohner und Bevölkerungsveränderung
- Bevölkerungsdichte
- Anzahl Privathaushalte und Haushaltsgrösse
- Altersverteilung (z. B. 65+, weniger mobil)
- Beschäftigte (Pendler kaufen auch am Arbeitsort ein)
- Gesamtfläche (lange Wege in grossen Gemeinden)

Verknüpfung
- Supermärkte über ihre Koordinaten einer Gemeinde zuordnen (räumliche Verknüpfung mit Gemeindegrenzen, z. B. von swisstopo)
- Danach Supermärkte pro Gemeinde zählen und über Gemeindename oder Gemeindecode mit den BFS-Daten verbinden
- Kennzahl bilden, z. B. Supermärkte pro 1'000 Einwohner

Herausforderungen
- OSM wird von Freiwilligen gepflegt: Supermärkte können fehlen oder falsch eingetragen sein
- Abgrenzung unklar (Supermarkt vs. kleiner Laden shop=convenience)
- Adressangaben oft unvollständig, deshalb Koordinaten verwenden
- Gemeindefusionen seit 2021 können Gemeindecodes verändern
- Unterschiedliche Jahre (BFS 2019, OSM aktuell)