# mrNiceRaider

Electrician by trade (Elektroniker für Energie- und Gebäudetechnik), builder by nature.

I work at the intersection of electrical engineering, embedded systems, and software — combining hands-on hardware knowledge with self-taught programming to build things that are actually useful. I speak german as motherlanguage, english fluently and got a level a1 niveau in spanish, wich itrain every day. My greatest intension is to solve problems on their roots.


---

## What I work on

**IoT & smart home systems**
Designing and building local-first home automation — WiFi sensing, WiZ lighting control, MQTT, Home Assistant, KNX, Zigbee. Preference for systems that work without cloud dependency.

**Signal processing & sensing**
RSSI-based presence detection, WiFi CSI analysis, acoustic leak detection (FFT, spectrograms), machine learning classifiers trained on real sensor data.

**Embedded & firmware**
ESP32 (WiFi, BLE, sensor fusion), Klipper firmware on repurposed 3D printer hardware, stepper motor control (TMC2209, NEMA17), custom printer.cfg configurations.

**Windows desktop software**
WinUI 3 / MSIX applications. Currently building a WiFi sensing app for the Microsoft Store — local intelligence, no cloud, no subscriptions.

**3D printing & mechanical design**
Elegoo Neptune 3 Pro as primary machine. Designing functional parts — brackets, enclosures, mounts — not decorative prints.

---

## Background

Trained as an electrician with specialization in energy and building technology (EGT). Self-taught in Python, C#, signal processing, and machine learning. Working across hardware and software simultaneously rather than choosing one side.

Located in Nordhausen, Thüringen, Germany.

---

## Interests

The things I find genuinely interesting tend to share a pattern: systems where physical reality and software meet, where you can measure something real and act on it intelligently.

- Energy systems and how they could work smarter (EV charging, building automation, grid interaction)
- Sensing the invisible — presence without cameras, structural faults without opening walls, breathing patterns from WiFi reflections
- Repurposing hardware for unintended purposes (3D printer boards as motion controllers, phone sensors as input devices)
- The gap between how technology is marketed and what it actually does internally

---

## Repos

| Project | Description | Visibility |
|---------|-------------|------------|
| [klipper-tv-mount](https://github.com/mrNiceRaider/klipper-tv-mount) | Motorized TV mount from salvaged 3D printer parts | Public |
| wifi-sensing | RSSI-based presence detection + WiZ light control | Private |
| pipe-leak-detector | Acoustic FFT tool for leak localization | Public |
| wiz-dashboard | Local Python dashboard for WiZ smart lights | Public |

# EV Trailer Power Share — Konzept

> Gedankenexperiment zur Reichweitenverlängerung von elektrischen Auto-Transportern
> durch Nutzung der Batterien der transportierten Fahrzeuge.

## Kernidee

Ein elektrischer Auto-Transporter (z.B. Tesla Semi) transportiert 8–10 Elektrofahrzeuge.
Diese Fahrzeuge besitzen zusammen eine enorme Batteriekapazität. Die Idee: einen Teil
dieser Energie während des Transports für den Antrieb des Trucks zu nutzen.

## Warum es bei Tesla funktionieren würde

Bei Drittanbietern scheitert das Konzept an drei unabhängigen Blockaden:
- Proprietäre BMS-Authentifizierung pro OEM
- Garantieverlust durch externe Entladung
- Spannungsheterogenität (400V vs. 800V Fahrzeuge gemischt)

Tesla besitzt die gesamte Kette:
- Semi = Tesla-Eigentum (Fahrzeug)
- Cargo = Tesla Model Y / 3 (noch nicht ausgeliefert, also Tesla-Eigentum)
- BMS, Software, Protokoll = einheitlicher Stack
- Kein OEM-Konflikt, keine Garantiefrage, keine Authentifizierungsbarriere

## Induktive Kopplung als Schlüssel

Statt physischer Stecker: induktive Pads im Trailer-Deck, identisch zur
Robotaxi-Ladeinfrastruktur die Tesla bereits entwickelt.

- Fahrzeuge parken sich auf dem Trailer ein → Kopplung automatisch
- Kein manueller Anschluss beim Verladen
- Gleiche Technologie wie stationäre induktive Ladepunkte

## Energie-Rechnung

## V2G-Vergleich

Der technische Unterschied zwischen Vehicle-to-Grid (V2G) und diesem Konzept
ist minimal — beide nutzen bidirektionale DC-Übertragung via ISO 15118-20.
Der einzige Unterschied: Bewegung während der Entladung. Das BMS unterscheidet
das nicht — es kennt nur "lade" und "entlade".

## Status

Konzept. Nicht implementiert. Kein Code.

Dokumentiert als Denkübung zur Systemarchitektur von EV-Energieflüssen.
Relevanter Patent-Hinweis: US 12,024,065 B2 beansprucht ähnliches für
Schienen-/Schiffsverkehr — für Straßentransport noch offen.

## Weiterführende Überlegungen

- MCS (Megawatt Charging System) als Hochleistungs-Verbindungsstandard
- Scania demonstrierte bereits 750 kW bidirektionales Laden via MCS (Mai 2026)
- Tesla Convoy Mode als Software-Grundlage für koordiniertes Energiemanagement
