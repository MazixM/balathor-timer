# Balathor Timer

Prosta, samodzielna strona do pilnowania cyklu Balathora w Metin2. Aplikacja działa bez frameworków i zależności — głównym plikiem jest `index.html`.

## Uruchomienie lokalne

Otwórz `index.html` w przeglądarce. Dostęp do mikrofonu może wymagać uruchomienia strony przez `localhost` albo HTTPS; bez mikrofonu działają timery, stoper i dźwięki.

## Deploy na Vercel

Workflow `.github/workflows/deploy.yml` publikuje stronę na Vercel po każdym pushu do gałęzi `main` (oraz ręcznie przez **Actions → Deploy to Vercel → Run workflow**).

Przed pierwszym deployem:

1. Utwórz projekt Vercel dla tego repozytorium (root projektu: katalog repozytorium; framework: **Other** / brak frameworka).
2. W GitHubie otwórz **Settings → Secrets and variables → Actions** i dodaj repozytoryjne sekrety:
   - `VERCEL_TOKEN` — token z ustawień konta Vercel,
   - `VERCEL_ORG_ID` — identyfikator konta/zespołu Vercel,
   - `VERCEL_PROJECT_ID` — identyfikator projektu Vercel.
3. Zapisz pierwszy commit lub uruchom workflow ręcznie.

Nie wpisuj tych wartości do plików repozytorium. Workflow używa Vercel CLI do pobrania ustawień projektu, zbudowania i wdrożenia strony produkcyjnej.
