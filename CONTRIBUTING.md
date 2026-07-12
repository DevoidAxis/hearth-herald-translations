# Contributing translations

Thank you for helping translate Hearth & Herald.

## What lives here

`ModuleData/Languages/<LANG>/` holds the translation XML for each language:

- `std_module_strings_xml.xml` — the mod's in-game text.
- `std_mcm_strings_xml.xml` — the Mod Configuration Menu text.
- `language_data.xml` — registers the language's files.

English (`EN/`) is the reference. It is generated from the mod, so do not edit it here.

## Add a new language

1. Copy the `EN/` folder to a new folder named for your language (e.g. `DE`, `PL`).
2. In each XML, change `<tag language="English" />` to your language's name.
3. Translate every `text="..."` value. Leave the `id="..."` attribute untouched.
4. Open a pull request.

## Update an existing language

Edit the `text="..."` values in your language's files and open a pull request. Any keys added since the last release are listed under [`missing-keys/`](missing-keys) with their English text and context.

## Rules that keep translations from breaking

- **Keep every `{VARIABLE}` token exactly** (for example `{HERO}`, `{SETTLEMENT}`, `{DAYS}`, `{REASON}`). Rearrange the sentence however your language needs; the tokens just have to survive.
- A few short suffix strings (the `ch_state_*` keys) **begin with a leading space** — keep it.
- **Do not use plural blocks** like `{?(X != 1)|s|}`. They are invalid in this game and blank the entire string. Where singular and plural differ, translate the explicit `..._1` / `..._n` key pair instead.

## Credit

Translators are credited by their chosen name in the mod's changelog and on its Nexus page. Tell us how you would like to be credited in your pull request.

## How it ships

A maintainer syncs merged files into the mod at release time, so your translation goes live in the next Nexus release.
