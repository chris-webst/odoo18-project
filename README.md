# Odoo 18 — šablona pro lokální spuštění

Tento repozitář má sloužit jako **šablona/checklist pro lokální běh Odoo 18** s využitím Dockeru a Cursoru.

## Interaktivní instalační checklist

**[Otevřít interaktivní instalační checklist](community_local_installation.html#installation-checklist)** (`community_local_installation.html`)

Soubor je samostatná stránka s odděleným postupem pro **macOS** a **Windows**. Otevři ho dvojklikem v systému souborů, nebo z editoru přes náhled / Live Server.

Pokud nemáš licenční přístup k Odoo Enterprise modulům, můžeš si tímto způsobem stále zprovoznit lokální Odoo 18, ale pouze ve verzi Community.

## Co je v repozitáři (v kostce)

- **[`docker-compose.yml`](docker-compose.yml)** — Říká Dockeru, aby ti na počítači spustil Odoo (web) a k němu Postgres databázi. Řádek se složkou `src/` necháváš zakomentovaný, dokud nemáš stažený Enterprise kód.

- **[`config/odoo.conf`](config/odoo.conf)** — Základní nastavení Odoo (např. kde má hledat moduly). **Než začneš pracovat „naplno“, změň si heslo správce databází** v položce `admin_passwd`.

- **[`.gitignore`](.gitignore)** — Říká gitu, co se nemá commitovat: mimo jiné **`src/`** (Enterprise), soubory s hesly (`.env`, …) a běžný nepořádek (logy, cache).

- **`addons/`** — Složka pro tvoje vlastní custom moduly.

- **`src/` (jen ve tvém počítači, nikam neuploaduješ)** — Sem patří **Enterprise moduly** z oficiálního repozitáře Odoo ([github.com/odoo/enterprise](https://github.com/odoo/enterprise). Kód podléhá licenci Odoo SA a **nesmíš ho nahrávat do veřejného repozitáře**; proto je složka `src/` v [`.gitignore`](.gitignore). Až máš `src/` vyplněné, v `docker-compose.yml` odkomentuješ příslušný svazek, jak je to popsáno v HTML návodu.
