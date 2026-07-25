# Translation handoff: new keys since 1.9.0 (targets 1.10.0)

Two features landed on the development branch after 1.9.0: backstory presets
at the ennoblement skill build (one lore-framed choice - Marshal, Castellan,
Caravan Master, or pick the skills yourself) and Consult the Ledger (the
Master Herald opens the campaign's chronicle, merged from the game's own
history and the clan's Hearth & Herald record).

English and Russian are already in this repo. The other languages fall back
to English for these keys until translated. Same rules as before: keep the
{VARIABLES} intact and restructure sentences however your language needs.

## Game text (goes in <lang>/std_module_strings_xml.xml), 21 keys

English reference:
```xml
    <string id="ch_promo_build_title2" text="Shape the Officer" />
    <string id="ch_promo_preset_intro" text="Throughout their battles, {NAME} was known as..." />
    <string id="ch_promo_preset_marshal" text="Marshal: a captain who read the field." />
    <string id="ch_promo_preset_marshal_hint" text="A proven captain who rallied troops and read the field. Trains Tactics, Leadership, and Scouting first." />
    <string id="ch_promo_preset_castellan" text="Castellan: a steward who kept order." />
    <string id="ch_promo_preset_castellan_hint" text="A steadfast steward who maintained stores, discipline, and order. Trains Steward, Engineering, and Leadership first." />
    <string id="ch_promo_preset_caravan" text="Caravan Master: a trader of the roads." />
    <string id="ch_promo_preset_caravan_hint" text="A shrewd trader who knew every road and market. Trains Trade, Riding, and Scouting first." />
    <string id="ch_promo_preset_custom" text="...something else (pick the skills)." />
    <string id="ch_promo_preset_custom_hint" text="Open the round-by-round pickers and choose every skill yourself." />
    <string id="ch_comm_their_calling" text="{ROW} - their calling" />
    <string id="ch_ledger_title" text="The Clan Ledger ({PAGE}/{PAGES})" />
    <string id="ch_ledger_desc" text="The chronicle of your clan and the realm, newest first. Hover an entry for its date and full text; select the page rows to turn the page." />
    <string id="ch_ledger_older" text="- Older entries -" />
    <string id="ch_ledger_newer" text="- Newer entries -" />
    <string id="ch_ledger_turn" text="Turn / Close" />
    <string id="ch_ledger_empty" text="The ledger holds no entries yet." />
    <string id="ch_ledger_ennobled" text="A veteran {TROOP} was ennobled - {NAME} joined the clan&#39;s companions." />
    <string id="ch_ledger_comm_taken" text="{NAME} took up the commission of {TRACK}." />
    <string id="ch_ledger_comm_laid" text="{NAME} laid down the commission of {TRACK}." />
    <string id="ch_ledger_known_as" text="{NAME} was remembered by the ranks as a {TRACK}." />
```

Notes for translators:
- The preset card labels (ch_promo_preset_*) complete the intro sentence
  "Throughout their battles, {NAME} was known as..." - keep them short, they
  sit on a narrow option card. The matching *_hint strings carry the full
  flavor and can breathe.
- ch_comm_their_calling wraps an existing row label ({ROW} is the whole
  "Track (held/cap)" text) with a marker that the hero's chosen backstory
  matches this career.
