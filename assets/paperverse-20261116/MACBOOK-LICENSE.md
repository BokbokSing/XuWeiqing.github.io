# MacBook model attribution

**Macbook Pro 13 inch 2020** by **timblewee** is licensed under
[Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/).

- Author: https://sketchfab.com/timblewee
- Original model: https://sketchfab.com/3d-models/macbook-pro-13-inch-2020-efab224280fd4c3993c808107f7c0b38
- Public authorised distribution used: https://sceneview.github.io/models/platforms/macbook_pro_13.glb
- Distributor credits: https://sceneview.github.io/credits.html
- Original SHA-256: `a7a8e9aa65bf7844f399c02772f72c4bd44e8dd02da846042c73c6d227ee2fb5`

Changes for this website: moderate geometry simplification (77,065 to 52,092
triangles), unused vertices and disconnected helpers removed, fixed 110-degree
open-lid pose, removed a floating tiny wordmark, renamed screen and keyboard
nodes for integration, width normalised to 1.18 world units with base at y=0
and front facing +Z. Original JPEG textures retained at no more than 1024px.
The site's Paperverse interface may replace the original screen texture.

This model is a third-party depiction. No endorsement by Apple or the model
author is implied. Display attribution in the website's asset credits whenever
this model is distributed or used publicly. Keep this file with redistributed
copies; see the linked licence for the complete terms.

## Integration

Load `macbook.glb` as ordinary glTF 2.0; no compression extension or animation
mixer is required. All geometry is already in an open pose. Default dimensions:
width **1.18**, height **0.79853349**, depth **1.12084668**. Centre x/z=0, bottom y=0.

- Screen mesh node: `MacBookScreen` (material `Material.002`). Replace its
  material/texture directly; glTF texture orientation uses `flipY=false`.
- Keyboard group: `MacBookKeyboard`.
- Keyboard keys: `MacBookKeyboardKeys`.
- Keyboard frame: `MacBookKeyboardFrame`.
- Lid: `MacBookLid`.
- Base: `MacBookBase`.

The author supplied an animated Touch Bar generation model, not the later
notched-display generation. Retain that device's appearance consistently in
cabinet and enlarged views.

`macbook-source.json` records source, modifications, dimensions and mesh counts.
The preparation script is `scripts/prepare-paperverse-macbook.mjs` and expects
the public original at `/tmp/macbook-pro-sceneview.glb`.
