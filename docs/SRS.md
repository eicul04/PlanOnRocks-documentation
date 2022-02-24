# ﻿Software Requirements Specification

### Links

 - [Technische Doku](https://eicul04.github.io/PlanOnRocks-documentation/)                                      
- [GitHub - Doku](https://github.com/eicul04/PlanOnRocks-documentation#plan-on-rocks---documentation)                                                              
- [GitHub - Backend](https://github.com/eicul04/PlanOnRocks-backend)   
- [GitHub - Frontend](https://github.com/eicul04/PlanOnRocks-frontend)   


## Use Case Diagram
![](https://github.com/eicul04/PlanOnRocks-documentation/blob/main/planOnRocks_UCD.png?raw=true)

## Use Cases

### Neuen Kletterfels anlegen

Ein Kletterfels hat einen Namen, einen Standort (GPS-Koordinate), einen Schwierigkeitsgrad (einfach, mittel, schwer), einen Absicherungsgrad (schlecht, okay, gut, sehr gut). Der Standort muss eindeutig sein. Existiert der Standort bereits wird die Anlage verweigert.

### Kletterfels labeln

Der aktuelle Standort des Gerätes des Benutzers wird automatisch ermittelt und damit die Entfernung zum Kletterfelsen berechnet. Über die berechnete Entfernung werden die Kletterfelsen in vier Kategorien unterteilt:

-   < 50km: Halbtagesausflug
-   < 140km: Tagesausflug
-   < 250km: Wochenendausflug
-   \>= 250 km: Urlaub

### Ausflug anfragen

Ein Ausflug kann erst angefragt werden, wenn bereits 5 Kletterfelsen angelegt sind. Bei der Anfrage muss der Benutzer die Zeit angeben (Datum/Zeitspanne) und das Teilnehmer-Können (Anfänger, Fortgeschritten, Profi). Ist die Zeitangabe nur ein Datum, wird eine weitere Abfrage generiert, ob es sich um einen Halbtages- oder Tagesausflug handelt.

### Ausflugstipp erstellen

Anhand von der Datumangabe werden die entsprechenden, bereits angelegten Kletterfelsen durchsucht:

-   1 Tag + Checkbox Halbtagesausflug: Halbtagesausflug
-   1 Tag + Checkbox Tagesausflug: Tagesausflug
-   2-3 Tage: Wochenendausflug
-   Länger als 3 Tage: Urlaub

Zusätzlich wird die entsprechende Liste der Kletterfelsen gefiltert nach dem angegebenen Teilnehmer-Können:

-   Anfänger: Kletterfelsen mit Schwierigkeitsgrad einfach und Absicherung gut oder sehr gut
-   Fortgeschritten: Schwierigkeitsgrad einfach/mittel; Absicherung okay/gut/sehr gut
-   Profi: Schwierigkeitsgrad einfach/mittel/schwer; Absicherung schlecht/okay/gut/sehr gut

### Wettericon in Ausflugstipps anzeigen

Liegt das Ausflugs Datum maximal 8 Tage in der Zukunft, soll in den Ausflugstipps, ein Wettericon (Sonne/Wolke/Regen/Schnee) das Wetter für das angegebene Datum und den Standort des jeweiligen Felsen anzeigen. Regnet es in über drei Felsstandorten (falls es mehr als drei Felsstandorte gibt; sonst gilt: regnet es an allen Felsstandorten) kommt eine Warnmeldung: "Willst du wirklich an diesem Tag klettern gehen?"

## Views

### Main Page
![](https://github.com/eicul04/PlanOnRocks-documentation/blob/main/mockups/mainView.png)

### Add Rock Dialog
![](https://github.com/eicul04/PlanOnRocks-documentation/blob/main/mockups/addRock.png)

## Technologie Stack

#### Frontend

- Framework: Angular 2.0
- Sprache: TypeScript
- IDE: WebStorm
- Testen: Jasmine Unit Tests

#### Backend

- Framework: Spring
- Sprache: Java
- IDE: IntellJ
- Testen: JUnit4
- Datenbank: 

#### Projektmanagement

- Projekt management tool: YouTrack
- Versions Kontrolle: Git and GitHub

## User Interfaces
