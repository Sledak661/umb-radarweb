# Cloud Radar (personal copy)

Personal copy of the Cloud Radar web page from
[4ujiuh/umbrella-scripts](https://github.com/4ujiuh/umbrella-scripts) (`site/radar.html`).

Changes: the event log panel was replaced with net worth and creep score tables,
and approximate (triangulated) wards are drawn with a dashed uncertainty circle.

Added on top: objective timers (Roshan respawn window and Aegis, first Tormentor,
day/night countdown), alerts (enemy smoke, Roshan events, all enemies missing,
enemy glyph ready) with sound and optional browser notifications, movement
trails and an enemy heatmap, a net worth chart in the economy card, a Share
button, and a compact layout on phones.

A meme stat was added as well: "drinks" for the player's own team — observed
uses of Clarity and Healing Salve (each one) plus a bottle counted only when
fully emptied. The Lua side accumulates it (`stats.drink`); the page also has a
fallback counter from item snapshots, so it works before the script is reloaded.
Drinks are shown in the hero card, as a droplet badge in the compact card, and
as a team total. Enemies are not shown.

The Lua side also sends `objectives.cycle` (server day/night timer) and the
objectives panel uses it when present.

The page is static; `radar.html` + `radar/` are enough to serve it.
