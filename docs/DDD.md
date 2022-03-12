# Domain Driven Design
### Ubiquitous Language
Als einheitliche Übersetzung und Verwendung der Domänen Begriffe im Code wird folgendes Glossar verwendet:
#### Glossar
##### Absicherungsgrad
Der Absicherungsgrad gibt an wie gut ein Kletterfels abgesichert ist. Das beinhaltet sowohl nach wie vielen Metern ein Bohrhaken kommt, als auch wie sinnvoll die Bohrhaken gesetzt sind. Der Absicherungsgrad kann schlecht, okay, gut oder sehr gut sein.

*=> im Domänencode: bolting (bad, okay, good, very good)*
##### Ausflug
Ein Ausflug hat ein Datum oder eine Zeitspanne. Er beinhaltet die Angabe zur Teilnehmererfahrung und einer Ausflugskategorie. Liegt das Ausflugsdatum oder das Startdatum der Zeitspanne weniger als acht Tage in der Zukunft, enthälte er auf Informationen über das Wetter.

*=> im Domänencode: trip*
##### Ausflugskategorie
Die Ausflugskategorie wird anhand der Entfernung des Benutzergerätes zum Kletterfelsen bestimmt. Dabei werden vier Kategorien anhand der berechneten Entfernung unterschieden:
-   < 50km: Halbtagesausflug
-   < 140km: Tagesausflug
-   < 250km: Wochenendausflug
-   \>= 250 km: Urlaub

*=> im Domänencode: trip category (half-day trip, day-trip, weekend trip, vacation)*
##### Ausflugsziel
Ein Ausflugsziel ist ein Kletterfels, der die Voraussetzungen eines Ausflugs erfüllt. Das heißt die gewünschte Ausflugskategorie besitzt und dem Teilnehmererfahrung entspricht. Ein Ausflugsziel existiert in der Domäne ist technisch gesehen allerdings ein Kletterfels.

*=> im Domänencode: trip destination*
##### Benutzergerät
Das Benutzergerät hat einen Standort. Damit wird die Entfernung zum Kletterfels berechnet. Der Standort kann sich verändern und wird beim Öffnen der Anwendung neu abgefragt.

*=> im Domänencode: user device*
##### Entfernung
Die Entfernung ist als Entfernung zwischen dem Standort des Kletterfelsens und dem Standort des Benutzergerätes definiert.

*=> im Domänencode: distance*
##### Kletterfels
Ein Kletterfels wird vom Benutzenden angelegt und hat einen Standort, ein Schwierigkeitsgrad, ein Absicherungsgrad und kann einer Ausflugskategorie zugeordnet werden.

*=> im Domänencode: climbing rock*
##### Schwierigkeitsgrad
Der Schwierigkeitsgrad ist eine Eigenschaft des Kletterfelsens. Er gibt an wie schwer die Routen an dem Kletterfels im Durchschnitt sind. Er kann als einfach, mittel oder schwer angegeben sein.

*=> im Domänencode: difficulty (easy, medium, hard)*
##### Standort
Sowohl ein Kletterfels als auch ein Benutzergerät besitzt ein Standort. Der Standort wird in Form einer GPS-Koordinate angegeben und ist somit einzigartig. 

*=> im Domänencode: location*
##### Teilnehmererfahrung
Mit der Teilnehmererfahrung soll es möglich sein anzugeben wie viel Können und Wissen die Teilnehmenden eines Ausflugs mitbringen. Dabei wird in Anfänger, Fortgeschritten und Profi unterschieden.

*=> im Domänencode: participant experience (beginner, advanced, professional)*
##### Wetter
Das Wetter ist eine Angabe für Ausflüge, um entscheiden zu können, ob es sinnvoll ist an dem ausgewählten Zeitpunkt klettern zu gehen. Das Wetter wird vereinfacht in vier Kategorien aufgeteilt: Sonne, Wolke, Regen, Schnee.

*=> im Domänencode: weather (sun, cloud, rain, snow)*
### Taktische Muster
todo: UML-Diagramm
todo: Analyse und Begründung der verwendeten Muster

#### Entitäten
- Climbing Rock
- Identität durch einmaligen Standort gegeben
#### Value Object


