# Hugo Theme: CSU-Lite

Ein sauberes, modernes und konfigurierbares Hugo-Theme, das für CSU-Ortsverbände oder andere politische Organisationen entwickelt wurde. Das Design ist von der offiziellen Webseite `csu.de` inspiriert und bietet ein professionelles und wiedererkennbares Erscheinungsbild.

![CSU-Lite Theme Screenshot](images/screenshot.png)  
*(Hinweis: Du solltest einen Screenshot des Themes in einem `images`-Ordner innerhalb des Theme-Verzeichnisses hinzufügen).*

## Funktionen

*   **Modernes & responsives Design:** Sieht auf Desktops, Tablets und mobilen Geräten hervorragend aus.
*   **Umfangreich konfigurierbar:** Die meisten Texte und Einstellungen können direkt in der `hugo.toml`-Datei deiner Webseite geändert werden.
*   **Datengesteuert:** Inhalte wie die Vorstandsliste werden zentral in Datendateien verwaltet und sind einfach zu pflegen.
*   **Homepage-Abschnitte:**
    *   Konfigurierbarer Hero-Bereich mit Hintergrundbild.
    *   Automatische Box für "Nächste Termine".
    *   "Aktuelles"-Abschnitt, der deine Beiträge anzeigt.
    *   Konfigurierbarer Abschnitt "Unser Team".
*   **Standard-Seiten:** Enthält Layouts für Nachrichtenartikel, Terminlisten, Kontaktseiten und rechtliche Seiten (Impressum, Datenschutz).
*   **Lokale Assets:** Entwickelt, um mit allen Assets (CSS, JS, Schriftarten) lokal zu laufen.

## Installation & Verwendung

Um dieses Theme zu verwenden, folge diesen Schritten:

1.  **Theme hinzufügen:** Platziere den `csu-lite`-Ordner in das `themes/`-Verzeichnis deiner Hugo-Webseite.

2.  **`hugo.toml` konfigurieren:** Lege das Theme in der Hauptkonfigurationsdatei deiner Webseite fest.

    ```toml
    # hugo.toml
    theme = "csu-lite"
    ```

3.  **Hugo starten:** Starte den Hugo-Server, um das Theme in Aktion zu sehen.

    ```bash
    hugo server
    ```

## Konfiguration

Dieses Theme wird über deine zentrale `hugo.toml`-Datei gesteuert. Nachfolgend findest du die wichtigsten Parameter, die du konfigurieren kannst.

### Allgemeine Parameter

```toml
# hugo.toml
baseURL = 'https://www.example.com/'
languageCode = 'de-de'
title = 'CSU Ortsverband Musterstadt'

[permalinks]
  post = "/aktuelles/:slug/"
```

### Homepage-Parameter (`[params.homepage]`)

Diese Sektion steuert alle Texte auf der Startseite.

```toml
# hugo.toml
[params.homepage]
  heroTitle = "Willkommen beim CSU-Ortsverband Musterstadt"
  heroSubtitle = "Gestalten Sie mit uns die Zukunft unserer Heimat."
  newsTitle = "Aktuelles aus dem Ortsverband"
  teamTitle = "Unsere Köpfe für Musterstadt"
  teamSubtitle = "Lernen Sie die Menschen kennen, die sich für unsere Gemeinde stark machen."
  teamButtonText = "Unser Team"
```

## Daten-Management

Wiederkehrende Inhalte wie die Vorstandsliste werden zentral im `data`-Verzeichnis deines Projekts verwaltet.

### Vorstand

Um die Mitgliederliste auf der `/vorstand`-Seite zu bearbeiten, öffne die Datei `data/vorstand.yml`.

**Beispielstruktur (`data/vorstand.yml`):**
```yaml
- name: "Max Mustermann"
  position: "Ortsvorsitzender"
  image: "/images/vorstand/max-mustermann.jpg"
  quote: "Unsere Heimat aktiv gestalten – das ist mein Antrieb."

- name: "Erika Musterfrau"
  position: "Stellv. Ortsvorsitzende"
  image: "/images/vorstand/erika-musterfrau.jpg"
  quote: "Ein offenes Ohr für die Anliegen unserer Bürger."

# ... weitere Mitglieder hier hinzufügen
```
Du kannst Einträge hinzufügen, entfernen oder die Reihenfolge ändern. Das Layout passt sich automatisch an.

## Inhaltstypen

Das Theme erwartet, dass Inhalte auf eine bestimmte Weise organisiert sind:

*   **Aktuelles:** Platziere deine Nachrichtenartikel in `content/post/`.
*   **Termine:** Platziere deine Termine in `content/termine/`. Stelle sicher, dass das `date`-Feld in der Zukunft liegt, damit sie auf der Startseite erscheinen.

## Mitwirken

Beiträge sind willkommen! Ob es sich um die Behebung eines Fehlers, die Verbesserung einer Funktion oder einen Vorschlag für eine neue handelt – deine Hilfe wird geschätzt.

1.  **Fehler melden:** Wenn du einen Fehler findest oder einen Vorschlag hast, eröffne bitte ein "Issue" im Repository des Projekts.
2.  **Pull-Requests:**
    *   Erstelle einen "Fork" des Repositorys.
    *   Erstelle einen neuen Branch (`git checkout -b feature/mein-neues-feature`).
    *   Nimm deine Änderungen vor und committe sie.
    *   Erstelle einen neuen Pull-Request.

## Lizenz

Dieses Theme ist unter der **Apache License 2.0** lizenziert. Es steht dir frei, es zu verwenden, zu modifizieren und zu verbreiten.

```
Copyright 2026 [Dein Name oder deine Organisation]

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
