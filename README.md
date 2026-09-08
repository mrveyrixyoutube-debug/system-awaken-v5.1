# SYSTEM: AWAKEN V5.1

Diese Version behebt den V5-Fehler: Die App bleibt auch ohne Supabase vollständig offline spielbar und die Buttons funktionieren lokal.

Enthalten:
- Quests mit exakten Mengen
- XP, Level und E-S-Rank-System
- Streak und Stats
- Shop
- tägliche kostenlose Lootbox
- Achievements
- Profil
- Login/Anonymous-Account bei Supabase
- echte Online-Weltrangliste nach Supabase-Einrichtung
- PWA/offline shell

## Warum steht OFFLINE?
Das ist normal, solange du in `index.html` noch diese Platzhalter hast:
YOUR_SUPABASE_URL
YOUR_SUPABASE_PUBLISHABLE_KEY

Die App ist trotzdem spielbar. Für Login + echte Weltrangliste musst du Supabase einmal einrichten.

## GitHub
Ersetze in deinem Repository nur:
- index.html
- manifest.json
- sw.js
- icon.svg

`supabase_setup.sql` kannst du zusätzlich hochladen.

Nach einem Commit ggf. GitHub Pages neu laden. Falls dein Handy die alte PWA-Version aus dem Cache zeigt, Seite komplett neu laden bzw. die installierte PWA einmal schließen und erneut öffnen.

## Supabase
1. Supabase-Projekt erstellen.
2. SQL Editor öffnen.
3. `supabase_setup.sql` ausführen.
4. Authentication aktivieren: Email/Password; optional Anonymous.
5. In `index.html` URL und Publishable Key eintragen.
6. Änderungen committen.
7. GitHub Pages öffnen.

Niemals einen service_role/secret key in `index.html` eintragen.

## Hinweis
Die Rangliste ist nach Supabase-Einrichtung echt online. Für ein großes öffentliches Spiel wären später noch Anti-Cheat, Rate-Limits und Moderation sinnvoll.
