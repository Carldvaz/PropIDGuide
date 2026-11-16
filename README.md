# WWE 2K26 Prop ID guide (for creators)

> **A guide for creators, not a rule.** Ranges are suggestions so props from
> different mods don't cross paths. No number is locked and nobody owns a
> number.

## Why it helps

An arena asks for each prop **by its number**: the number is written in the
arena's PropsSet, inside its `.cak`. Unlike an arena's ID, a prop's number
can't be changed when someone else installs it. If two creators use the same
number, only one of their props can be installed on a PC, and the arena that
loses its prop crashes when it loads.

## How it works

- Each creator sets aside a **range** of numbers (1000 by default) and uses
  those for their props.
- **Nothing is enforced.** When you export an arena pack, ArenaLab looks your
  prop numbers up here. If one falls in a range someone else set aside, it
  suggests another number, and you can still go ahead. People who install
  your pack never see these suggestions: they can't change the number anyway.
- Numbers **0–9999** are left to the game: its own props, plus room for the
  ones updates add.
- New ranges start at **100000**.

## Set aside a range

Open a [range request](../../issues/new?template=request-range.yml). You can
also use **Request a range…** in ArenaLab's Prop ID guide window, which opens
the same form.

If you already have props out, list their numbers in the request. Your range
can be built around them.

## Good to know

- A prop that behaves like the steel steps (full stairs) also takes the next
  two numbers. The game creates those pieces when the arena loads. Keep all
  three inside your range.
- The guide lists numbers, not files. Your props stay yours.

## For apps

`prop-ids.json` is read as-is:

```json
{
  "format": "WWE 2K26 prop ID guide",
  "version": 1,
  "updated": "YYYY-MM-DD",
  "notice": "A guide for creators, not a rule. ...",
  "reserved": [{"from": 0, "to": 9999, "by": "the game", "note": "..."}],
  "ranges":   [{"from": 100000, "to": 100999, "creator": "...", "note": "..."}],
  "props":    [{"id": 100000, "creator": "...", "name": "...", "used_in": "..."}]
}
```
