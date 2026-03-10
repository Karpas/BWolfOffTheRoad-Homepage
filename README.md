# BWolf Homepage

Statyczna strona BWolf Off The Road, przygotowana pod darmowy hosting na Cloudflare Pages.

## Struktura repo

- `site/index.html` - strona główna
- `site/dokumenty/index.html` - podstrona dokumentów (`/dokumenty`)
- `site/assets/css/styles.css` - style
- `site/assets/images/` - obrazy i logo

## Lokalny podgląd

```bash
cd site
python3 -m http.server 4173
```

Otwórz:
- [http://localhost:4173](http://localhost:4173)
- [http://localhost:4173/dokumenty/](http://localhost:4173/dokumenty/)

## Deploy na Cloudflare Pages

1. Wypchnij repo na GitHub/GitLab.
2. W Cloudflare wybierz: `Workers & Pages` -> `Create application` -> `Pages` -> `Connect to Git`.
3. Ustaw:
   - `Framework preset`: `None`
   - `Build command`: (puste)
   - `Build output directory`: `site`
4. Kliknij `Save and Deploy`.

Możesz też użyć opcji `Direct Upload` i wskazać katalog `site`.

## Licencja

MIT - zobacz plik `LICENSE`.
