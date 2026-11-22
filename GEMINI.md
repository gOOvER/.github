# Global User Rules (gOOvER)

## 1. Changelog, Versionierung, Contributors & README (`CHANGELOG.md`, `.github/CHANGELOG.md`, `CONTRIBUTORS.md` & `README.md`)
- Aktualisiere bei **jeder** Code-Änderung, jedem Bugfix, Feature oder Refactoring automatisch und ungefragt:
  1. [`CHANGELOG.md`](CHANGELOG.md) sowie (in GitHub-Projekten mit Release-Workflow) [`.github/CHANGELOG.md`](.github/CHANGELOG.md) im Format [Keep a Changelog](https://keepachangelog.com/en/1.0.0/) mit Semantic Versioning (`Added`, `Changed`, `Fixed`, `Security`, `Removed`).
  2. [`README.md`](README.md), sodass Features, Befehle, Optionen, unterstützte Versionen und Beschreibungen **immer** auf dem aktuellsten Stand sind.
  3. [`CONTRIBUTORS.md`](CONTRIBUTORS.md) in jedem Projekt erstellen bzw. pflegen und in der `README.md` verlinken.
- Halte dabei – falls im Projekt vorhanden – auch die Versionsnummern in Metadaten-Dateien wie `.toc`, `Cargo.toml`, `tauri.conf.json`, `plugin.json`, `update.json`, `composer.json` oder `package.json` synchron.

## 2. README-Standard (Logo, Social Preview Banner, `CONTRIBUTORS.md` & Badges)
- **Immer erstellen, wenn nicht vorhanden:** Für jedes neue oder überarbeitete GitHub-Projekt automatisch ein passendes **Logo** (`.github/assets/logo.png` & `.github/assets/logo.svg`), ein **Social Preview Banner** (`.github/assets/social-banner.png`, `1280×640`) sowie eine **[`CONTRIBUTORS.md`](CONTRIBUTORS.md)** erstellen und in der `README.md` oben zentriert samt einheitlicher Badge-Leiste einbinden.

## 3. Globales GitHub-Repository (`https://github.com/gOOvER/.github`)
- Alles, was **global** für alle GitHub-Projekte gelten soll (z. B. `FUNDING.yml`, `SECURITY.md`, `CONTRIBUTORS.md`, `CONTRIBUTING.md`, Issue-/PR-Templates, globale Workflows, Community Health Files), wird direkt in das zentrale Repository **`https://github.com/gOOvER/.github`** (`main`-Branch) gepusht.
- Zusätzlich soll in GitHub-Projekten die Datei `.github/FUNDING.yml` genutzt werden:

```yaml
# 💝 Support goovers Development
# Your support helps maintain and improve these projects

# 🌟 GitHub Sponsors
#github: goover

# 🎨 Creative Platform Support
#patreon: oldnoob

# ☕ Coffee & Quick Support
ko_fi: goover
buy_me_a_coffee: goover
#liberapay: goover

# 🎯 Developer Appreciation
#thanks_dev: "u/gh/goover"

# 🔗 Primary Donation Platform
custom: https://donate.goover.dev

# ₿ Bitcoin (BTC Mainnet)
# bc1qt6wec64n3gnrhclp4vfckyvr8h27tmqswy28gc
```
