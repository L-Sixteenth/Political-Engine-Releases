# Skyrim topographic map — attribution and usage

Artwork: **T Cook**, *Skyrim topographic map*, Nexus Mods #36159.
Source and permissions: https://www.nexusmods.com/skyrim/mods/36159?tab=description

The user supplied `Skyrim topographic map-36159-1-0.rar` on 2026-10-10.
Its original `Skyrim.svg` is copied unchanged into the panel as
`skyrim-topographic.svg`. SHA256:
`5dbdf441e571c85ccee80e73e681ff5e784fd9e3bf75ffddd3650eb8c8c441f5`.

For runtime performance, `tools/render_panel_background.cjs` renders that
unchanged artwork into `skyrim-topographic.png` (4096x4096). This is the displayed
background; the original SVG is retained. Extreme zoom is limited by raster
resolution. Region overlays and interactive outlines remain vector geometry.
`tools/build_panel_mask.cjs` generates `map-mask.js`, a conservative 256x256
display-only land/province occupancy mask. It replaces expensive runtime SVG
hit tests when positioning labels; it does not affect native battle placement.

The author's Nexus permissions checked on 2026-10-10 allow asset use and
modification without prior permission. Redistribution requires credit to the
creator. Paid mods are forbidden; Donation Points require author permission.
These are the author's posted permissions, not an unrestricted CC0 licence.
Preserve this attribution when publishing the mod and recheck the permissions.

`tools/build_topographic_map.cjs` extracts the nine capital symbol centres,
samples the original provincial borders every 40 SVG units, and extracts the
source water footprint for an inverted land clip. The independent strategy
overlay is intersected with these borders and land: neighbouring provinces
and water receive no district colouring or pointer targets.

A thin-plate-spline projection aligns nine vanilla capital anchors. Fellburg
and custom home markers are projected from game coordinates. Strategy polygon
edges are sampled every 2,000 game units. These are campaign districts, not a
reconstruction of lore hold borders. Native ownership and battlefield selection
remain unchanged in game coordinates. No Sever Actions or Flat World Map
Framework dependency is introduced.

Both v2.41 ZIPs must be updated together because the Russian patch overrides
panel HTML. The previous private parchment background is removed from the
package; the original user attachment remains available in the workspace.
