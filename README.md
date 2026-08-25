# Sinai Evidence DB

This repo holds a synced copy of the evidence database for The Sinai Project — a multilingual (English/Hebrew/French/Spanish) evidence database on Torah/Tanach authenticity, organized into 14 thematic layers (core, archaeology, history_corrob, linguistics, literary, transmission, sociological, genetics, prophecy, philosophy, comparative, meta, cosmology, coherence).

## Purpose

This repo exists so a scheduled cloud agent can check `data.json` for existing entries before proposing new evidence, avoiding the duplicate-heavy results that come from an agent working without access to the current database.

## Canonical source

The **canonical, live-edited copy** of this data lives locally at `C:\Abba\Learntalmud.org\projects\sinai\data.json` and powers the actual Sinai Project website. This repo's `data.json` is a periodically-synced snapshot, pushed after editing sessions — it is not itself the source of truth, and may lag behind the canonical file between syncs.

## Structure

`data.json` contains:
- `layers`: metadata for the 14 thematic categories (id, name, description in all four languages)
- `proofs`: the individual evidence entries, each with a `layer`, multilingual title (`t`) and explanation (`e`), source (`s`), and URL (`u`)
