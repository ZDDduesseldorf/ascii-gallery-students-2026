# ASCII Gallery Level 1 - 2026 (Exercise level 1)

Interne Git/GitHub-Übung für den Kurs **Software Engineering für Data Science**.

Dieses Repository trainiert den **gemeinsamen Branch-Workflow**: Alle Studierenden haben Schreibrechte auf dasselbe Repository, arbeiten aber in eigenen Branches.  Änderungen am `main`-Branch erfolgen dann ausschliesslich über Pull Requests. 

<img width="600" alt="image" src="https://github.com/user-attachments/assets/9e7e9a5e-92de-4ad3-9d01-430d27bf8d14" />

## Lernziele

Nach der Übung kannst du:

- ein Issue erstellen und dir selbst zuweisen,
- einen Feature-Branch erstellen,
- sinnvolle Commits erstellen und pushen,
- einen Pull Request öffnen,
- einen Pull Request einer anderen Person reviewen,
- Review-Feedback in einem bestehenden Branch umsetzen,
- einen Pull Request mergen,
- optional einen einfachen Merge-Konflikt lösen.

## Deine Aufgabe

Füge **ein Stück ASCII-Art** zur gemeinsamen Webseite hinzu. Die Webseite siehst du hier: https://zddduesseldorf.github.io/ascii-gallery-students-2026/

### 1. Issue erstellen

Erstelle zuerst ein Issue, z. B.:

> Add ASCII art by @my-user-name

Weise das Issue dir selbst zu.

### 2. Repository aktualisieren

```bash
git switch main
git pull
```

### 3. Feature-Branch erstellen

Verwende einen aussagekräftigen Namen:

```bash
git switch -c ascii/<github-username>
```

Beispiel:

```bash
git switch -c ascii/florian-huber
```

### 4. `index.html` bearbeiten

Suche in `index.html` den Abschnitt für den ersten Buchstaben deines GitHub-Namens:

- A-F
- G-L
- M-R
- S-Z

Füge direkt **oberhalb** des passenden Kommentars einen neuen Block ein und platziere darin deine ASCII-Art. Hier ein Beispiel:

```html
<article class="art-card">
    <h3>@dein-github-name — Titel</h3>
<pre>
  /\_/\\
 ( o.o )
  > ^ <
</pre>
</article>
```

**Achtung:** Zeichen wie `<`, `>` und `&` haben in HTML eine besondere Bedeutung. Falls deine ASCII-Art diese Zeichen enthält, verwende gegebenenfalls `&lt;`, `&gt;` und `&amp;`.

Es gibt im Internet auch haufenweise Ascii-Art-Generatoren, z.B. hier: https://texteditor.com/ascii-art/

Sowohl dieses Repository als auch die daraus erstellte Webseite sind aus dem Netz frei erreichbar. Für alle.
Darum bitte:

- maximal ca. 20 Zeilen,
- keine beleidigenden oder diskriminierenden Inhalte,
- keine sensiblen, personenbezogenen Daten

### 5. Lokal kontrollieren

Du kannst die Seite direkt im Browser öffnen (also `index.html`).

### 6. Commit + Push

```bash
git status
git diff
git add index.html
git commit -m "Add ASCII art by <github-username>"
git push -u origin ascii/<github-username>
```

### 7. Pull Request erstellen

Erstelle auf GitHub einen Pull Request gegen `main`.

Der PR soll:

- dein Issue referenzieren (`Closes #...`),
- kurz beschreiben, was du hinzugefügt hast,
- eine andere Person als Reviewer anfordern.

### 8. Code Review

Reviewe mindestens **einen Pull Request einer anderen Person**.

Ein Review soll mehr enthalten als nur "sieht gut aus". Prüfe z. B.:

- Ist die Änderung im richtigen Abschnitt?
- Wurde nur das verändert, was für die Aufgabe nötig war?
- Ist das HTML weiterhin gültig/lesbar?
- Wird die ASCII-Art korrekt dargestellt?

Falls sinnvoll: `Request changes` verwenden und eine konkrete kleine Verbesserung anfordern.

### 9. Feedback einarbeiten + mergen

Falls du Feedback erhalten hast, passe deinen Branch an, committe und pushe erneut. Der bestehende Pull Request aktualisiert sich automatisch.

Nach erfolgreichem Review kann der PR gemerged werden.

## Optional: Merge-Conflict-Challenge

Wenn Zeit bleibt, arbeitet paarweise mit `conflict-zone.txt`. Beide Personen erzeugen vom gleichen Ausgangsstand einen eigenen Branch und ersetzen dieselbe Zeile durch unterschiedliche Texte. Merge den ersten PR und versuche anschliessend den zweiten Branch zu aktualisieren und den Konflikt lokal zu lösen.

## GitHub Pages

Nach einem Merge nach `main` wird die Webseite automatisch per GitHub Pages deployed, sofern Pages für dieses Repository in der Organisation freigeschaltet ist.
