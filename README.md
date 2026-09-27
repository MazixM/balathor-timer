# Balathor Timer

Prosta, samodzielna strona do pilnowania cyklu Balathora w Metin2. Aplikacja nie wymaga frameworka ani zależności — głównym plikiem jest `index.html`.

**Wersja produkcyjna:** [https://balathor-timer.vercel.app/](https://balathor-timer.vercel.app/)

## Uruchomienie lokalne

Otwórz `index.html` w przeglądarce. Dostęp do mikrofonu może wymagać uruchomienia strony przez `localhost` albo HTTPS; bez mikrofonu działają timery, stoper i dźwięki.

## Publikowanie

Jedynym mechanizmem wdrażania jest natywna integracja repozytorium GitHub z Vercel. Produkcyjna strona działa pod adresem **https://balathor-timer.vercel.app/**. Każdy push do gałęzi `main` powoduje wdrożenie produkcyjne w tym projekcie Vercel.

Jeśli konfigurujesz projekt od zera, zaimportuj repozytorium `MazixM/balathor-timer` w Vercel i ustaw:

- **Framework Preset:** Other,
- **Root Directory:** `./`,
- **Build Command:** puste (bez kompilacji),
- **Output Directory:** `.`.

W Vercel w **Project → Settings → Git** sprawdź, że podłączone jest repozytorium `MazixM/balathor-timer`, a gałęzią produkcyjną jest `main`. Nie są potrzebne sekrety Vercel w GitHub Actions — deploy obsługuje integracja Vercel.
