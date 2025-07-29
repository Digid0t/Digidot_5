# Digidot_5

# Grillbert - für eine zufriedene Grillgemeinschaft  🔥

____

Logo_Bild:
https://raw.githubusercontent.com/Digid0t/DigiDot_5/main/Grillbert.png

QR-Code Bild:
https://raw.githubusercontent.com/Digid0t/DigiDot_5/main/grillbert_qr.png

Digidot_QR_LOGO
https://raw.githubusercontent.com/Digid0t/DigiDot_5/main/DigiDot_5_QR.png

Sprache_json:
https://raw.githubusercontent.com/Digid0t/DigiDot_5/main/sprache.json

Code:
https://github.com/Digid0t/Digidot_5/main/index.html 

Web:
https://raw.githack.com/Digid0t/DigiDot_5/main/index.html

____

<p align="center">
  <img src="https://raw.githubusercontent.com/Digid0t/DigiDot_5/main/Grillbert.png" alt="Grillbert" width="300"/>
</p>

____

Willkommen beim digitalen Aushängeschild für Grillbert! Dies ist ein superleichtes, eigenständiges Webprojekt, das als digitale Willkommens- und Informationstafel für einen realen, öffentlichen Grillplatz dient. Es ist darauf ausgelegt, von jedem Smartphone aus per QR-Code aufgerufen zu werden.

## 📖 Was ist dieses Projekt und wozu dient es?

Stellen Sie sich vor, Sie kommen an einen öffentlichen Grillplatz. Dort steht eine Tafel mit den Regeln. Was aber, wenn Sie die Sprache nicht verstehen?

Genau hier kommt Grillbert ins Spiel!

**Das Ziel:** Dieses Projekt bietet eine einfache, freundliche und für jeden zugängliche Webseite mit den Grillregeln. Der Clou ist die **umfassende Mehrsprachigkeit**. Menschen aus aller Welt können mit einem Klick die Seite in ihre Muttersprache übersetzen lassen. So stellen wir sicher, dass jeder die Regeln versteht und sich willkommen fühlt.

### ✨ Besondere Funktionen

*   **Massive Sprachunterstützung:** Unterstützt **26 Sprachen**, von Deutsch und Englisch bis hin zu Arabisch, Hindi und Suaheli.
*   **Automatische Spracherkennung:** Die Webseite versucht, die Sprache des Browsers zu erkennen und den Text automatisch zu übersetzen.
*   **Einfache Sprachwahl:** Ein übersichtliches Dropdown-Menü mit Flaggen erlaubt den manuellen Wechsel der Sprache.
*   **PDF-Download:** Mit einem Klick können die Regeln als sauberes, druckfertiges PDF gespeichert werden.
*   **Keine Server-Abhängigkeit:** Läuft komplett im Browser. Man benötigt nur einen Webspace oder kann es direkt über GitHub Pages hosten.
*   **Federleicht & Schnell:** Besteht aus nur einer HTML-Datei und einer JSON-Datei. Lädt blitzschnell, auch bei schlechter Internetverbindung.

---

## 🔧 Wie wird es verwendet?

Die Verwendung ist kinderleicht!

1.  **Dateien hochladen:** Laden Sie die Dateien `index.html` und `sprache.json` in Ihr Web-Verzeichnis oder in ein GitHub-Repository.
2.  **GitHub Pages (empfohlen):** Wenn Sie GitHub nutzen, gehen Sie in Ihrem Repository auf `Settings` -> `Pages` und aktivieren Sie unter `Branch` den `main`-Branch. Nach ein paar Minuten ist Ihre Seite online.
3.  **WICHTIG: Den Link zur `sprache.json` anpassen:**
    *   Gehen Sie in Ihrem GitHub-Repository zur Datei `sprache.json`.
    *   Klicken Sie auf den Button **"Raw"**.
    *   Kopieren Sie die URL aus der Adresszeile Ihres Browsers.
    *   Öffnen Sie die `index.html` und ersetzen Sie im JavaScript-Teil den Platzhalter-Link mit Ihrer kopierten URL:

    ```javascript
    // Ersetzen Sie diese Zeile mit Ihrem Link
    const translationsUrl = 'https://raw.githubusercontent.com/IHR_BENUTZERNAME/IHR_REPO/main/sprache.json';
    ```
4.  **Fertig!** Ihre Webseite ist nun einsatzbereit. Erstellen Sie einen QR-Code, der auf die URL Ihrer Seite verweist, und bringen Sie ihn am Grillplatz an.

---

## 🧠 Wie die Magie funktioniert (Eine einfache Erklärung des Codes)

Stellen Sie sich die Webseite wie ein Restaurant vor.

*   Die **`index.html`** ist das leere Restaurant mit Tischen, Stühlen und Platzhaltern für das Essen.
*   Die **`sprache.json`** ist das riesige Kochbuch der Küche mit allen Gerichten in 26 verschiedenen Sprachen.
*   Das **JavaScript** (am Ende der `index.html`) ist der clevere Kellner, der die Sprache des Gastes erkennt und ihm das richtige Menü bringt.

Schauen wir uns die drei Schritte im Detail an:

### Schritt 1: Das "Restaurant" bauen (`index.html`)

Im HTML-Code geben wir jedem Text, der übersetzt werden soll, eine Art "Platzhalter-Schild". Das machen wir mit dem Attribut `data-key`.

**Beispiel:**
Die Überschrift hat das Schild `data-key="welcomeTitle"`.

```html
<h1 data-key="welcomeTitle">
    Willkommen am Grillplatz von Grillbert...
</h1>
```
Das ist wie ein Schild auf einem Tisch, auf dem "Hauptgericht hier hinstellen" steht. Der Kellner (JavaScript) weiß so später genau, wo er welchen Text platzieren muss.

Außerdem bauen wir das Dropdown-Menü (`<select id="lang-switcher">...`), das als Speisekarte für den Gast dient, um die Sprache auszuwählen.

### Schritt 2: Das "Kochbuch" schreiben (`sprache.json`)

Die Datei `sprache.json` ist unser Kochbuch. Sie ist eine riesige Liste, die nach Sprachen geordnet ist.

*   Jede Sprache hat einen **Code** (z.B. `"de"` für Deutsch, `"fr"` für Französisch).
*   Innerhalb jeder Sprache gibt es eine Liste von **"Gerichten"**. Jedes Gericht hat einen Namen, der genau dem "Platzhalter-Schild" (`data-key`) aus dem HTML entspricht.

**Beispiel:**
```json
{
  "de": {
    "welcomeTitle": "Willkommen am Grillplatz..."
  },
  "fr": {
    "welcomeTitle": "Bienvenue à l'espace barbecue..."
  },
  "hi": {
    "welcomeTitle": "ग्रिलबर्ट के BBQ स्पॉट में आपका स्वागत है..."
  }
}
```
Wenn der Gast also Französisch wählt (`fr`), weiß der Kellner, dass er für den Platzhalter `welcomeTitle` den Text "Bienvenue à l'espace barbecue..." aus dem Kochbuch nehmen muss.

### Schritt 3: Der "Kellner" nimmt die Arbeit auf (JavaScript)

Das ist das Gehirn der ganzen Operation. Wenn die Webseite lädt, passiert Folgendes:

1.  **Der Kellner holt das Kochbuch:**
    Als Allererstes lädt das Skript die komplette `sprache.json`-Datei. Das ist wie der Kellner, der zu Schichtbeginn das Kochbuch aus der Küche holt. Er wartet, bis er es hat, bevor er irgendetwas anderes tut (`await fetchTranslations()`).

2.  **Der Kellner begrüßt den Gast clever:**
    Nun muss die Startsprache gewählt werden (`getInitialLanguage()`). Der Kellner ist clever und geht in drei Schritten vor:
    *   **"Waren Sie schon mal hier?"** Er schaut im `localStorage` des Browsers nach, ob der Gast bei einem früheren Besuch schon eine Sprache gewählt hatte. Wenn ja, nimmt er diese.
    *   **"Welchen Akzent haben Sie?"** Wenn nicht, lauscht er der Sprache des Browsers (`navigator.languages`). Er vergleicht sie mit allen 26 Sprachen im Kochbuch. Findet er eine Übereinstimmung, wählt er diese Sprache.
    *   **"Im Zweifel Deutsch."** Wenn alles andere fehlschlägt, bringt er als sicheren Standard einfach die deutsche "Speisekarte".

3.  **Der Kellner serviert die Gerichte:**
    Sobald die Sprache feststeht, läuft der Kellner durch das ganze Restaurant (`setLanguage()`). Er schaut sich jedes Element mit einem `data-key`-Schild an, sucht den passenden Text im Kochbuch (`translations[sprache][key]`) und setzt ihn an der richtigen Stelle ein (`elem.innerHTML = ...`).

_____

![Grillbert_der_Gemeinschmecker](https://raw.githubusercontent.com/Digid0t/DigiDot_5/main/Grillbert_Der_Gemeinschmecker.png)


_____

<img src="https://raw.githubusercontent.com/Digid0t/DigiDot_5/main/DigiDot_5_QR.png" alt="DigiDot 5 QR Code" width="300">

____
