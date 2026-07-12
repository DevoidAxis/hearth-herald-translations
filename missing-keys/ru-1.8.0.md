# Russian translation handoff: new keys in Hearth & Herald 1.8.0

Hi! 1.8.0 adds the stationed-heralds feature and these new strings.
Same format as before: replace the English text and keep the
{VARIABLES} intact (restructure the sentence however Russian needs,
the variables just have to survive). Leading spaces in the ch_state_*
suffixes are intentional, please keep them.

Note: the old {?(X != 1)|s|} plural blocks turned out to be invalid
TaleWorlds syntax (they blanked the whole string), so 1.8.0 replaces
each of those keys with an explicit singular/plural pair (…1 / …n).
No plural blocks anywhere anymore; each variant is a plain sentence.

## Game text (goes in RU/std_module_strings_xml.xml), 30 keys
```xml
    <string id="ch_herald_arrived" text="{HERO} has reached {SETTLEMENT} and taken up the {OFFICE} post."/>
    <string id="ch_herald_enroute1" text="{HERO} sets out for {SETTLEMENT} to take up the {OFFICE} post, arriving in about a day."/>
    <string id="ch_herald_enrouten" text="{HERO} sets out for {SETTLEMENT} to take up the {OFFICE} post, arriving in about {DAYS} days."/>
    <string id="ch_herald_recalled" text="{HERO}'s journey to the {OFFICE} post is called off."/>
    <string id="ch_herald_restored_msg" text="Your {OFFICE} Herald, {HERO}, has resumed office."/>
    <string id="ch_herald_returns" text="{HERO} is released from the {OFFICE} office and returns to your party."/>
    <string id="ch_herald_stationed" text="{HERO} takes up residence at {SETTLEMENT} as {OFFICE} Herald."/>
    <string id="ch_herald_stays" text="{HERO} is released from the {OFFICE} office and remains at {SETTLEMENT}."/>
    <string id="ch_herald_suspended_msg" text="Your {OFFICE} Herald, {HERO}, stands down: {REASON}."/>
    <string id="ch_intrigue_refused" text="It cannot be done, my lord: {REASON}."/>
    <string id="ch_migrate_stationed" text="Your heralds have taken up residence at {SETTLEMENT}. Appointed heralds now serve from your Clan Home."/>
    <string id="ch_reason_by_order" text="suspended by your order"/>
    <string id="ch_reason_caravan" text="the holder runs a caravan"/>
    <string id="ch_reason_governor" text="the holder governs a settlement"/>
    <string id="ch_reason_home_lost" text="the clan home was lost"/>
    <string id="ch_reason_other" text="the holder has another duty"/>
    <string id="ch_reason_party" text="the holder leads their own party"/>
    <string id="ch_state_cd1" text=" (ready in 1 day)"/>
    <string id="ch_state_cdn" text=" (ready in {DAYS} days)"/>
    <string id="ch_state_off" text=" (turned off in settings)"/>
    <string id="ch_state_reason" text=" ({REASON})"/>
    <string id="ch_state_seat" text=" (return to seat, or reach Tier {TIER})"/>
    <string id="ch_state_soon" text=" (coming soon)"/>
    <string id="ch_status_active" text="Active"/>
    <string id="ch_status_captured" text="Captured"/>
    <string id="ch_status_dead" text="Dead"/>
    <string id="ch_status_enroute" text="En route to the seat"/>
    <string id="ch_status_missing" text="Missing"/>
    <string id="ch_status_suspended_fmt" text="Suspended: {REASON}"/>
    <string id="ch_status_vacant" text="Vacant"/>
```

## Mod Options (goes in RU/std_mcm_strings_xml.xml), 1 key
```xml
    <string id="hh_mcm_limit_companions_hint3" text="Add extra recruitable-companion slots to your clan (a flat bonus on top of the vanilla tier limit), and free the slot of each companion you station as a herald so they do not count against your recruit limit. If TrueLimits is installed and Limits mode is Auto, this steps aside entirely."/>
```

Context notes:
- ch_herald_stationed/enroute/arrived/recalled: on-screen messages when a herald takes a post at the Clan Home, travels to it, arrives, or is dismissed.
- ch_herald_suspended_msg/restored_msg: on-screen messages when an office pauses or resumes.
- ch_herald_returns/stays: dismissal outcomes (rejoins your party / waits at the seat).
- ch_status_*: one-word office status labels (Active/Vacant/Suspended/Captured/Missing/En route).
- ch_reason_*: short suspension reasons shown after "Suspended:".
- ch_migrate_stationed: the one-time message old saves see when their heralds move to the Clan Home.
- ch_state_*: short greyed-menu suffixes appended to an action name, e.g. "Prepare Defences (ready in 3 days)".
- hh_mcm_limit_companions_hint3: Mod Options hint for the companions limit.
- ch_intrigue_refused: shown when an intrigue action cannot proceed. Note: the {REASON} text itself is English-only in this release (short phrases like "requires an active Watch Herald"); reason localization is planned for a later pass.
- ch_state_reason: generic greyed-menu suffix wrapping a refusal reason, e.g. "Make this your clan's seat. (Relocation available in 12 days.)".
- Heads-up: four existing RU keys carried the broken plural block and were split/patched in-repo with placeholder Russian (ch_reloc_cooldown1/n, ch_dlg_cooldown1/n, ch_home_lost_count1/n, ch_action_stub). Please review those too.
