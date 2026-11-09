# DevBoard

DevBoard ist ein kleines Kanban-Board für Entwicklungsaufgaben. Das Projekt entsteht gemeinsam und dient dazu, moderne Frontend-Entwicklung mit Vue 3, TypeScript und Git praktisch zu lernen.

## Projektstatus

Das Projekt befindet sich im Aufbau. Aktuell gibt es eine statische Task-Eingabe mit Eingabefeld und Button. Der Button hat noch keine Funktion. Als Nächstes entsteht das visuelle Kanban-Board, danach folgen typisierte Task-Daten und Interaktionen.

Die vollständige Roadmap mit Aufgaben und Akzeptanzkriterien steht in [Issue #22](./issues/22).

## Geplante Funktionen

- Aufgaben in den Spalten „To Do“, „In Progress“ und „Done“ anzeigen
- Aufgaben hinzufügen, bearbeiten, löschen und zwischen Spalten verschieben
- Aufgaben lokal im Browser speichern
- Aufgaben suchen und filtern
- Responsive und barrierearme Bedienung
- Tests, CI und ein öffentliches Deployment

## Verwendete Technologien

- Vue 3 mit der Composition API
- TypeScript
- Vite
- Tailwind CSS 4
- npm
- Git und GitHub für Branches, Pull Requests und Reviews

## Lokal starten

Voraussetzung ist eine aktuelle Node.js-LTS-Version mit npm.

```bash
git clone https://github.com/Rukasu187/Projects.git
cd Projects
npm install
npm run dev
```

Vite zeigt nach dem Start die lokale URL im Terminal an.

## Verfügbare Befehle

| Befehl | Zweck |
| --- | --- |
| `npm run dev` | Lokalen Entwicklungsserver starten |
| `npm run build` | TypeScript prüfen und Produktions-Build erstellen |
| `npm run preview` | Produktions-Build lokal ansehen |

## Zusammenarbeit

Jede Aufgabe wird auf einem eigenen Branch umgesetzt. Arbeitet nicht direkt auf `main`.

```bash
git switch main
git pull
git switch -c feat/kurzer-aufgabenname
```

Änderungen committen und den Branch zu GitHub pushen:

```bash
git add .
git commit -m "feat: beschreibe die Änderung"
git push -u origin feat/kurzer-aufgabenname
```

Danach einen Pull Request gegen `main` öffnen. Im PR die zugehörige Issue verlinken, zum Beispiel mit `Closes #3`. Der andere Entwickler reviewt den Code, stellt Fragen und bestätigt, dass die Änderung lokal funktioniert. Erst nach dem Review und grünen Checks wird gemergt.

### Branch mit aktuellem `main` abgleichen

Wenn `main` während der Arbeit weiterentwickelt wurde:

```bash
git fetch origin
git rebase origin/main
```

Bei Konflikten die betroffenen Dateien gemeinsam prüfen und bearbeiten. Danach:

```bash
git add .
git rebase --continue
git push --force-with-lease
```

`--force-with-lease` nur auf dem eigenen Feature-Branch verwenden, nachdem der Rebase abgeschlossen ist.

## Lernprinzip

Die Aufgaben sind bewusst klein geschnitten. Der Entwickler, der den PR erstellt, sollte erklären können, was sich geändert hat und warum. Reviews sollen Verständnis aufbauen: konkrete Fragen und Hinweise sind hilfreicher als fertige Lösungen direkt vorzugeben.
