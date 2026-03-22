# Odoo 18 — šablona pro lokální spuštění

Tento repozitář má sloužit jako **šablona/checklist pro lokální běh Odoo 18** s využitím Dockeru a Cursoru.

## Interaktivní instalační checklist

Průvodce je soubor [`community_local_installation.html`](community_local_installation.html) — samostatná stránka s postupem pro **macOS** a **Windows**, rozbalovacími kroky a zaškrtáváním.

**Běžná cesta:** po stažení nebo naklonování repozitáře soubor otevři v prohlížeči — dvojklikem ve složce, nebo náhled / Live Server v editoru.

**Volitelně z prohlížeče bez klonu:** u tohoto repa je zapnutý [GitHub Pages](https://pages.github.com/) náhled — **[otevřít průvodce online](https://chris-webst.github.io/odoo18-project/community_local_installation.html#installation-checklist)**.

Bez licenčního přístupu k Odoo Enterprise můžeš podle návodu spustit Odoo 18 ve verzi **Community**; Enterprise je v průvodci volitelný krok.

## Co je v repozitáři (v kostce)

- **[`community_local_installation.html`](community_local_installation.html)** — Interaktivní průvodce (Docker, složky, Enterprise atd.).

- **[`docker-compose.yml`](docker-compose.yml)** — Spouští Odoo (web) a PostgreSQL. Řádek se `src/` nechávej zakomentovaný, dokud nemáš stažený Enterprise kód.

- **[`config/odoo.conf`](config/odoo.conf)** — Základní nastavení Odoo. **Před ostrým použitím změň heslo** v `admin_passwd`.

- **[`.gitignore`](.gitignore)** — Co se nemá commitovat (mimo jiné obsah `src/` kromě značky složky, hesla v `.env`, logy, cache).

- **`addons/`** — Vlastní moduly (v repu je prázdná struktura přes `.gitkeep`).

- **`src/`** — Sem lokálně dáváš **Enterprise** z [github.com/odoo/enterprise](https://github.com/odoo/enterprise); do veřejného repa se kód nenahrává (licence). Po vyplnění odkomentuješ svazek v `docker-compose.yml` podle průvodce.