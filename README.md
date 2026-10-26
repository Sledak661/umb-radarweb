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

A meme stat was added as well: "drinks" per player — observed uses of Clarity,
Healing Salve, Bottle, Enchanted Mango and Faerie Fire, counted from inventory
changes on the Lua side (`stats.drink`) and shown in the hero card and in the
team header. Enemy drinks are only counted while their inventory is observed.

The Lua side also sends `objectives.cycle` (server day/night timer) and the
objectives panel uses it when present.

The page is static; `radar.html` + `radar/` are enough to serve it.
