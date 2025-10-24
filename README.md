# Optimierung-Bestellmengenplan
Lebensmittel-Lager Optimierung - Bestellmengenplanung
📋 Use Case Beschreibung
Dieses Projekt löst ein Optimierungsproblem für die Bestellmengenplanung in einem Lebensmittellager unter Berücksichtigung von:

Lagerkapazitätsbeschränkungen

Produktspezifischen Mindestbeständen

Verderbskosten für überschüssige Ware

Nachfrageprognosen

🎯 Zielsetzung
Minimierung der Gesamtkosten durch optimale Bestellmengen, die folgende Faktoren berücksichtigen:

Lagerhaltungskosten

Potenzielle Verderbskosten für Mengen über 110% der Nachfrage

Einhaltung von Mindestbeständen

Gesamtlagerkapazität

📊 Produktdaten
Produkt	Nachfrage	Lagerkosten (€)	Verderbskosten (€)	Mindestbestand
Tiefkühl-Pizza	200	0.50	8.00	50
Frisch-Milch	150	0.30	12.00	100
Reis	80	0.10	2.00	40
🧮 Mathematisches Modell
Entscheidungsvariablen
bestellmengen[i]: Bestellmenge pro Produkt

excess[i]: Überschuss über 110% der Nachfrage

Zielfunktion
text
Minimiere: Σ(Lagerkosten × Bestellmenge + Verderbskosten × Excess)
Nebenbedingungen
Mindestbestand: Bestellmenge ≥ Mindestbestand

Überschussdefinition: Excess ≥ Bestellmenge - 1.1 × Nachfrage

Kapazität: Σ Bestellmengen ≤ 2000 Einheiten

🚀 Installation & Ausführung
bash
pip install pulp pandas matplotlib
python lager_optimierung.py
📈 Ergebnisse
Das Skript berechnet optimale Bestellmengen und generiert eine visuelle Darstellung, die folgende Elemente zeigt:

Optimale Bestellmengen

Mindestbestände

110% Nachfrage-Grenze (Verderbsgrenze)

💡 Technologie-Stack
Python 3

PuLP (Lineare Optimierung)

pandas (Datenverwaltung)

matplotlib (Visualisierung)

📁 Projektstruktur
text
lager-optimierung/
├── lager_optimierung.py
├── bestellmengen_vergleich.png
├── requirements.txt
└── README.md
