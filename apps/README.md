# Embedded pixel tools

Both entries are real standalone production builds, freshly rebuilt from an isolated copy of the existing source. Original project files were not changed.

- `/apps/typewriter/index.html`: Bubble Typewriter, general browser edition.
- `/apps/sea/index.html`: Bubble Sea, standalone web edition.

Each application uses relative URLs (`base: ./`). Use the explicit `index.html` URLs above: Vite's public-directory routing falls back to the main portfolio page for the directory-only URL. The portfolio should open the selected tool in a foreground portrait phone (roughly 390 × 700 CSS px, responsive to viewport) with a close/home control outside the iframe. Lazy load the iframe only when opened. `title` each iframe.

Typewriter supports text, artwork, optional photos and PNG export without accounts or a backend. Sea supports the actual preset play, catching, local collection and pattern download flows. Sea login, credits and custom generation are local demo features; custom generation returns a preset sample. Do not present these as online AI generation, payment or cloud account services. Optional Sea microphone mode requires an explicit user action; long press is the default available interaction.

Font attribution and licenses are retained: Typewriter `font-licenses.json`; Sea `fonts/LICENSE.txt` and `fonts/licenses/`. User artwork and creator signature remain part of the original builds.

Main portfolio language/audio controls do not automatically translate or mute these independent applications; each tool retains its own language and audio settings. A tool's local storage is the same origin as the portfolio, using its existing keys. Avoid sandboxing away downloads/local storage; a same-origin iframe with no sandbox is appropriate for these trusted, local bundled apps.
