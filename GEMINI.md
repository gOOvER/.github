# Global User Rules (gOOvER)

## 1. Changelog & Versionierung (`CHANGELOG.md`)
- Aktualisiere bei **jeder** Code-Änderung, jedem Bugfix, Feature oder Refactoring automatisch und ungefragt die [`CHANGELOG.md`](CHANGELOG.md) (Format: [Keep a Changelog](https://keepachangelog.com/en/1.0.0/) mit Semantic Versioning `Added`, `Changed`, `Fixed`, `Security`, `Removed`).
- Halte dabei – falls im Projekt vorhanden – auch die Versionsnummern in Metadaten-Dateien wie `plugin.json`, `update.json`, `composer.json` oder `package.json` synchron.

## 2. Globales GitHub-Repository (`https://github.com/gOOvER/.github`)
- Alles, was **global** für alle GitHub-Projekte gelten soll (z. B. `FUNDING.yml`, `SECURITY.md`, Issue-/PR-Templates, globale Workflows, Community Health Files), wird direkt in das zentrale Repository **`https://github.com/gOOvER/.github`** (`main`-Branch) gepusht.
- Zusätzlich soll in GitHub-Projekten die Datei `.github/FUNDING.yml` (Vorlage unter `C:\Users\goove\.gemini\config\templates\FUNDING.yml`) genutzt werden:

```yaml
# 💝 Support goovers Development
# Your support helps maintain and improve these projects

# 🌟 GitHub Sponsors
#github: goover

# 🎨 Creative Platform Support
#patreon: oldnoob

# ☕ Coffee & Quick Support
ko_fi: oldnoob
buy_me_a_coffee: goover
#liberapay: goover

# 🎯 Developer Appreciation
#thanks_dev: "u/gh/goover"

# 🔗 Primary Donation Platform
custom: https://donate.goover.dev
```
