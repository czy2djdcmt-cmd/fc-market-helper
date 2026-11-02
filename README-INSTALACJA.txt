# FC Market Helper 2.0 — instalacja na iPhonie

## Co zawiera
- `index.html` — aplikacja.
- `manifest.webmanifest` — metadane PWA.
- `sw.js` — pamięć podręczna aplikacji (Service Worker).
- `icon-180.png`, `icon-512.png` — ikony.

## Ważne ograniczenie
Aplikacja nie pobiera automatycznie cen z rynku EA. Wpisy cen są ręczne, a alert okazji pojawia się po ręcznej aktualizacji ceny. Nie ma integracji z kontem EA, automatycznego kupowania ani dostępu do prywatnych endpointów. Powiadomienia przeglądarki zależą od możliwości iOS; nie jest to działający w tle serwerowy system push.

## Publikacja bez Maca — GitHub Pages z iPhone’a
1. W Safari otwórz `https://github.com` i zaloguj się lub utwórz konto.
2. Utwórz nowe repozytorium, np. `fc-market-helper`.
3. Ustaw repozytorium jako Public (wymagane dla bezpłatnego GitHub Pages w typowym planie).
4. W repozytorium wybierz **Add file → Upload files** i wgraj wszystkie pliki z tego pakietu (nie sam ZIP).
5. Zapisz zmiany przyciskiem **Commit changes**.
6. Otwórz **Settings → Pages**. W sekcji Build and deployment wybierz **Deploy from a branch**, branch `main`, folder `/(root)`, następnie Save.
7. Poczekaj na publikację. Adres będzie w postaci `https://TWOJ_LOGIN.github.io/fc-market-helper/`.
8. Otwórz ten adres w Safari na iPhonie. Wybierz **Udostępnij → Do ekranu początkowego**. Jeśli pojawi się opcja otwierania jako aplikacja internetowa, pozostaw ją włączoną i wybierz Dodaj.

GitHub może zmieniać nazwy i położenie elementów interfejsu. Publikacja wymaga połączenia z internetem.

## Dane i kopie zapasowe
- Dane obserwowanych kart i historia są przechowywane w pamięci przeglądarki (`localStorage`) na tym urządzeniu i w tej instalacji/origin.
- Użyj **Start → Eksportuj dane** albo **Historia → Eksportuj JSON**, aby pobrać kopię.
- Po zmianie adresu witryny, wyczyszczeniu danych Safari lub zmianie przeglądarki dane mogą nie być dostępne. Zrób kopię JSON.
- Import JSON zastępuje dane aktualnie zapisane na urządzeniu.

## Skrót FC market
Przycisk w aplikacji otwiera dokładnie:
`shortcuts://run-shortcut?name=FC%20market`

## Funkcje
1. PWA: manifest, ikony i Service Worker.
2. FC Companion: przycisk uruchamiający skrót iOS.
3. Wyszukiwarka: otwiera wyniki wyszukiwania internetowego dla wpisanej nazwy i przeszukuje lokalną listę.
4. Obserwowane: nazwy kart, limity i aktualne ceny.
5. Monitor: oznaczanie okazji po ręcznej aktualizacji ceny; powiadomienie przeglądarki, jeśli dostępne i dozwolone.
6. Wygląd: ciemny interfejs inspirowany Ultimate Team.
7. Historia: zmiany limitów, ceny, dodania i usunięcia kart.

## Uwaga o PWA na iOS
Do instalacji potrzebny jest publiczny adres HTTPS. Sam plik HTML otwarty z aplikacji Pliki nie zapewni pełnej instalacji PWA ani działania Service Workera.
