# RailStock-Lagerbewirtschaftungssoftware

RailStock ist eine eigenentwickelte Lagerbewirtschaftungssoftware zur Verwaltung und Organisation von Modelleisenbahnen.
Ziel des Projekts ist es, ein modernes System zu schaffen, welches Bestände, Lagerplätze und Modelleisenbahnen effizient verwaltet. 

---

## RailStock Übersicht

Dieses Repository dient als **zentrale Übersicht** für das gesamte RailStock-Projekt.  
Es enthält keine eigenen Funktionen, sondern verweist auf die beiden Haupt-Repositories:

- **Backend:** [RailStock Backend](https://github.com/ImeschNico/RailStock-Lagerbewirtschaftungssoftware-Backend)  
  Enthält das REST-API-Backend mit H2-Datenbank (lokal persistent) und allen Endpoints für Lokomotiven, Lagerplätze und Bestände.

- **Frontend:** [RailStock Frontend](https://github.com/ImeschNico/RailStock-Lagerbewirtschaftungssoftware-Frontend)  
  Enthält die Benutzeroberfläche (React + Vite) und kommuniziert über die REST-API mit dem Backend.

---

## Über das Projekt

Die Idee zu **RailStock** entstand im privaten Umfeld. 
Ein Bekannter von mir besitzt rund 3'000 Modelleisenbahnen, die er in einem Zimmer lagert.
Bei dieser Menge an Artikeln verliert man leicht den Überblick über den Bestand.

Da er selbst ein leidenschaftlicher Sammler und auch privater Verkäufer von Modelleisenbahnen ist, schlug ich ihm vor, eine eigene Lagerbewirtschaftungssoftware zu entwickeln, um Ordnung und Übersicht zu schaffen.
Er war von der Idee begeistert so entstand das Projekt **RailStock**.

--- 

## IST-Zustand

Mit dieser Ausgangslage setzte ich mich mit dem Bekannten zusammen, um zu besprechen, was die Software können muss.
Daraus ergab sich folgender IST-Zustand:
- Der Bekannte besitzt ein grosses Lager an Modelleisenbahnen, das zwar schön geordnet in Regalen steht, jedoch verliert man leicht den Überblick, welche Loks tatsächlich vorhanden sind.
- Zusätzlich gibt es ein Sammler-Lager (privat) und ein Lager für den Weiterverkauf.

---

## Soll-Zustand

Mit Hilfe der Software möchte der Bekannte:
- Einen klaren Überblick über sein Sammler-Lager und die Produkte für den Weiterverkauf erhalten.
- Ein strukturiertes Lagersystem führen, mit Lagerplätzen wie **Regal > Tablar**, um gesuchte Produkte schnell wiederzufinden.
- Sammler- und Verkaufs-Lager sauber trennen, damit ersichtlich ist, welche Artikel verkauft oder der Sammlung hinzugefügt werden müssen.
- Durch Filteroptionen schnell anzeigen können, welche Artikel im Lager vorhanden sind.

### Gewünschte Filteroptionen: 
- **Marke:** Märklin, Hag, Bemo, etc.
- **Artikelnummer:** Original Märklin-Nummer, etc.
- **Typ:** Dampflok, Diesellok, etc.
- **Modell:** Krokodil, etc.
- **Stromart:** Wechselstrom / Gleichstrom
- **Spur:** H0, etc.
- **Epoche:** I, II, etc.
- **Betriebsart:** Digital / Analog / MFX

---

## User Stories

### Verkäufer/Sammler (MVP)

1. **Als Sammler von Modelleisenbahnen möchte ich Loks mit Artikelnummern in mein Lagersystem hinzufügen, um einen Überblick über meinen Bestand zu haben.**
   - **Akzeptanzkriterien:**
     - Die Applikation muss Loks anhand der Artikelnummer erkennen können.
     - Die Applikation muss den aktuellen Bestand an einem Lagerplatz anzeigen und anpassen können.
     - Die Applikation muss Filteroptionen bereitstellen, um bestimmte Loks und deren Lagerplatz schnell zu finden.

2. **Als Verkäufer möchte ich meinen verfügbaren Bestand aktuell halten.**
   - **Akzeptanzkriterien:**
     - Die Applikation muss den aktuellen Bestand anzeigen.
     - Bestände müssen artikelgenau abrufbar sein.
     - Die Applikation muss nach Epoche, Typ, Modell, Spur, Stromart und Betriebsart filterbar sein.

### Lagerbewirtschaftung (MVP)

3. **Als Benutzer möchte ich Lagerplätze anlegen, um meinen Bestand korrekt abzubilden.**
   - **Akzeptanzkriterien:**
     - Lagerorte haben Namen oder IDs.
     - Lagerorte können Regale, Tablare oder Slots enthalten.
     - Lagerplätze müssen bearbeitbar sein.

4. **Als Benutzer möchte ich Loks zwischen Lagerplätzen verschieben, damit die Bestände aktuell bleiben.**
   - **Akzeptanzkriterien:**
     - Die Applikation muss eine Transferfunktion besitzen.
     - Bestände müssen nach Transfers aktualisiert werden.

### Mobile Applikation (Nach MVP)

5. **Als Benutzer möchte ich eine mobile App haben, um Bestände unterwegs anzupassen.**
   - **Akzeptanzkriterien:**
     - Die App muss auf einem Smartphone nutzbar sein.
     - Synchronisation mit der PC-Version muss gewährleistet sein.
     - Die App muss einen integrierten Scanner besitzen, um Produkte mobil zu scannen.

---
