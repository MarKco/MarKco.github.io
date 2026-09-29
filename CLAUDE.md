# MarKco.github.io

Sito personale di Marco Zanetti, pubblicato su GitHub Pages: `https://markco.github.io`.
Repo **pubblico** — niente segreti, credenziali, dati personali sensibili o non destinati alla condivisione. Se non sei sicura che qualcosa sia ok da pubblicare, chiedi prima.

## Chi è Marco
Android developer. Ha anche un altro sito: www.marcozanetti.it (linkato dal sito, per tutto ciò che non è progetti/codice — niente sezione musica/batteria qui, il sito resta focalizzato sui progetti).

## Stack
- **Jekyll**, build nativo di GitHub Pages (nessun GitHub Actions richiesto). Push su `main` → GH Pages builda da sola.
- Deploy: root del branch `main` (no cartella `/docs`, no branch `gh-pages` separato).
- Ruby di sistema (via Homebrew) è troppo recente per la gem `github-pages` (bug Liquid/`tainted?`). Per build/serve locali usare Ruby 3.3.12 installato via rbenv in questo progetto (`.ruby-version`), invocato con path assoluto perché `rbenv` stesso è rotto sul sistema (residuo Intel Homebrew in `/usr/local`, non toccato):
  `/Users/marco/.rbenv/versions/3.3.12/bin/ruby /Users/marco/.rbenv/versions/3.3.12/bin/jekyll serve`
- Post/blog: `_posts/YYYY-MM-DD-titolo.md` con front matter YAML. Vedi sezione "Blog" sotto.
- Progetti: collection `_projects/` (IT, permalink `/progetti/:path/`) + `_projects_en/` (EN, permalink `/en/projects/:path/`), stessi slug, layout `project`.
- Sito bilingue: contenuti IT alla root, EN sotto `/en/`. Ogni pagina ha `alt_url` in front matter che punta alla sua controparte nell'altra lingua — usato dallo switcher IT/EN in alto a destra nell'header (vedi `_includes/header.html`) e dai tag `hreflang` in `_includes/head.html`. Stringhe UI condivise (nav, bottoni progetto) in `_data/strings.yml`, chiavi per `lang`.
- Licenza: codice sotto GPL-3.0 (`LICENSE`), contenuti (testi, screenshot) sotto CC BY-NC-SA 4.0 (`CONTENT-LICENSE.md`). Pagina `/licenza/` (IT) e `/en/license/` (EN) la spiegano ai visitatori, linkata dal footer. Slug diverso apposta: su filesystem case-insensitive (macOS) `/license/` collide con il file `LICENSE` alla radice del sito generato — vedi `_site/LICENSE` vs `_site/license/`.

## Contenuti
- Portfolio Android developer: progetti da `_projects/` + `_projects_en/` (10 repo GitHub pubblici + ProPortion, in entrambe le lingue).
- Link al sito personale www.marcozanetti.it per tutto il resto (musica, pensieri non tecnici, ecc.).
- Niente sezione Musica sul sito — rimossa su richiesta esplicita di Marco.
- Aggiunta una nuova pagina/progetto in una lingua → serve sempre la controparte nell'altra (stesso slug nella collection giusta, `alt_url` incrociato). Il sito non è pensato per essere parzialmente tradotto.

## Blog — come funziona (attualmente nascosto)
Blog escluso dal build (`_posts` e `blog.html` in `exclude:` in `_config.yml`) su richiesta di Marco —
idea buona ma rimandata. Per riattivarlo: togliere quelle due righe da `exclude`, e rimettere il link
"Blog" in `_includes/header.html` e il link "RSS" in `_includes/footer.html`.

Se/quando riattivato: Marco scrive il contenuto in chat, Claude crea il file in
`_posts/YYYY-MM-DD-titolo.md` con il front matter (`title`, eventuale `tags`). Nessuna pubblicazione
automatica: il post diventa live solo dopo commit + push su `main` (fatto da Claude solo su richiesta
esplicita, mai in autonomia — vedi regola sotto sul confermare prima di pubblicare).

## Come lavorare insieme
- Prima di pubblicare/committare qualsiasi cosa, verificare che sia adatta a un repo pubblico.
- Preferire semplicità: niente build step extra oltre a quello nativo di Jekyll/GH Pages, a meno che Marco non chieda esplicitamente qualcosa che lo richieda (es. componenti interattivi → allora si valuta Astro o JS puro sopra Jekyll).
- Chiedere prima di aggiungere dipendenze, plugin Jekyll non whitelisted da GH Pages, o cambiare la strategia di deploy.
