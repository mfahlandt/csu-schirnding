# CSU Ortsverband Schirnding - Webseite

Dies ist der Quellcode für die offizielle Webseite des CSU Ortsverbands Schirnding ([www.csu-schirnding.de](https://www.csu-schirnding.de)).

Die Seite basiert auf [Hugo](https://gohugo.io/) und verwendet das Theme [csu-lite](https://github.com/mfahlandt/csu-lite).

## Lokale Installation

Um die Seite lokal zu bearbeiten und zu testen, benötigst du eine installierte Version von Hugo (Extended Version empfohlen).

1.  **Repository klonen:**
    ```bash
    git clone https://github.com/mfahlandt/csu-schirnding.git
    cd csu-schirnding
    ```

2.  **Theme initialisieren (Submodule):**
    ```bash
    git submodule update --init --recursive
    ```

3.  **Server starten:**
    ```bash
    hugo server
    ```

    Die Seite ist dann unter `http://localhost:1313` erreichbar.

## Theme-Updates

Wenn es Updates am Theme gibt, kannst du diese wie folgt in dein Projekt holen:

```bash
git submodule update --remote --merge
```

Vergiss nicht, diese Änderung dann auch zu committen:

```bash
git add themes/csu-lite
git commit -m "Update Theme"
git push
```

## Deployment

Die Seite wird automatisch via **GitHub Actions** gebaut und auf **GitHub Pages** veröffentlicht, sobald Änderungen in den `main`-Branch gepusht werden.
