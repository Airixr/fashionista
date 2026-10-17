# Fashionista (public test)

A live appearance editor for AION 2: change your character's face, body, colours, hair, physics
and outfits in game, save looks as designs and share them as codes. It also adds the outfits,
mounts and wings that only the Korean client has. Everything is client side: only your screen
shows the changes.

This is a **test version**. Please report anything that breaks, looks wrong or is confusing
(see "Report a problem" below).

## Install

1. Close the game.
2. Put `fashionista.dll` in `AION 2\Aion2\Binaries\Win64\plugins\`. The plugin loader (`winmm.dll`
   in `Win64\`) and `paksigbypass.dll` (in `plugins\`) must be installed too; they come with the
   plugin pack you got Fashionista from.
3. If `outfitswapper.dll` is in the plugins folder, remove it: Fashionista contains it now (Outfits
   tab) and both cannot run together. Your swaps and presets carry over.
4. Start the game and press **Home** to show or hide the window (Settings changes the key).

## Get the KR cosmetics and the icons (once)

Outfits tab > **KR cosmetics** > **Download KR cosmetics + icons** (about 400 MB). The game can
stay open; every part is checked, and a paused or broken download continues where it stopped.
The icons appear at once; the KR cosmetics after you **restart the game**. They carry a purple
**KR** tag in the lists ("KR only" shows just them). Game patches do not break them.

## Tabs

- **Character**: face sliders, face / hair types, colours, material settings, model scale.
  One search box over everything; right-click a section header for its options.
- **Body**: the per-bone editor (body, face and hair bones). Mirror copies an edit to the other
  side; "Children follow" chooses what the bones below take over. Copy / Paste move a bone's edit;
  "Copy to the other side" works with Mirror off too.
- **Physics** (switch it on in Settings): how hair, chest, skirts, capes and accessories swing,
  plus jiggle bones for parts the game does not simulate.
- **Outfits**: what each slot shows (outfit, accessories, weapons, mount, wings), whatever you
  wear. Pick a look in a row's list (type to search; Up / Down and Enter work), "only this" limits
  a swap to the item you wear now, the "x" removes it. Changes show at once; **Save** keeps them
  (per character), **Revert** undoes them. Presets hold whole outfit sets.
- **Designs**: saved looks in folders. A design stores the parts you tick (face, body, colours,
  types, physics, outfit ...) and applies only those. "Keep on character" off = for this session.
- **Settings**: key, accent colour, size, theme, bone editor, and **Report a problem**.

## Share codes

The toolbar's copy button turns your look (the ticked parts) into an `A2LOOK1:` code; paste one to
apply it. Codes with an outfit carry its swaps too.

## Report a problem

Settings > **Create bug report** writes one text file (`plugins\fashionista\bug-reports\`) and
shows it in Explorer; its path is copied. Post the file in the Fashionista Discord / chat with a few
words about what you did and what happened (a screenshot helps).
It holds Fashionista's log of the last three game sessions, its settings and the KR cosmetics'
state; your Windows user name and character names are removed. Open it to see exactly what it
contains. Nothing is ever sent by itself.

## Files

- `plugins\fashionista\`: `fashionista.ini` (settings), `appearance.ini` (your look),
  `appearance_presets\` (designs), `thumbs\` (icons), `logs\` (`fashionista.log`, `bones.txt`),
  `bug-reports\`.
- Outfits: `%LOCALAPPDATA%\hk-settings\aion2\outfitswapper\` (the folder the standalone Outfit
  Swapper used too): `settings.json`, `<region>\swaps.json`, `presets.json`, the look list cache and
  the KR cosmetics (`WW\imports\`, about 1 GB). Settings > Outfits > "Open outfits folder".

## Remove

Delete `fashionista.dll` from the plugins folder (and `plugins\fashionista\` plus the outfits
folder above if you want your data gone too).
