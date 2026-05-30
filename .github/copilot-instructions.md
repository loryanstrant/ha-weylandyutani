# Copilot instructions — ha-weylandyutani

> Canonical standards live in the `dev-standards` repo on SOUNDWAVE/Gitea.
> Read by Copilot chat **and** inline suggestions.

## What this repo is

A **Home Assistant theme** (not a custom component) — a Weyland-Yutani / *Alien*
aesthetic theme: theme YAML plus the Thedus font family, installable via HACS as
a theme.

## Repo shape

- `themes/weylandyutani.yaml` — the theme definition.
- `www/fonts/` — Thedus OTF family + `alien-fonts.css` resource (+ the font's
  commercial-use license PDF — keep it).
- `hacs.json` — HACS metadata (theme type).
- `screenshots/`, `preview.png` — README art.

## Conventions (theme, not component)

- This is a theme: **no `manifest.json`, no `custom_components/`, no `pytest`**.
  The component pipeline in `dev-standards` does NOT apply here.
- Preserve the font license PDF; the Thedus fonts ship under a commercial-use
  license — don't strip or relicense it.
- Keep the `www/fonts/alien-fonts.css` resource path stable (HA dashboards
  reference it).

## Never

- Don't commit secrets.
- Don't restructure this into a component — it's a theme.
