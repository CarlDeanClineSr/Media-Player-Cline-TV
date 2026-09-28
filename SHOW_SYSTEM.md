# CLINE TV — SHOW SYSTEM 1

## Purpose

Cline TV is treated as a television service, not an Internet Archive browser.

The Archive is the source warehouse. The Cline catalog is the station library. The channels are programming streams. The Guide is the station's program guide.

The player should feel like turning on a television and finding programming already arranged for viewing.

## The rule

**Do not create a channel merely because more files exist.**

A channel earns its place when there is a recognizable programming identity and enough verified material to make that identity interesting.

A program can belong to a broad programming stream while still carrying a more precise genre/format classification in the catalog.

## Current streams

| Ch | On-air identity | Programming role |
|---:|---|---|
| 1 | STAR TREK | Series |
| 2 | SCIENCE & COSMOS | Science |
| 3 | GODZILLA & MONSTERS | Creature Feature |
| 4 | MOVIE HOUSE · FAMILY & COMEDY | Matinee |
| 5 | MOVIE HOUSE · SCI-FI | Science Fiction |
| 6 | MOVIE HOUSE · ADVENTURE | Adventure |
| 7 | MOVIE HOUSE · ACTION | Action |
| 8 | MOVIE HOUSE · ANIMATION | Family |
| 9 | MOVIE HOUSE · MONSTERS | Creature Feature |
| 10 | MOVIE HOUSE · CLASSICS | Classic Feature |
| 11 | MOVIE HOUSE · WAR & THRILLER | Action Feature |
| 12 | MOVIE HOUSE · FEATURE PRESENTATION | Prime Feature |

These are the first show-system streams, not the final catalog.

## Programming behavior

The existing player mechanics remain intact:

- Program dial advances within a stream.
- At the end of a stream, automatic playback rolls to the next stream.
- Channel dial changes streams.
- Guide searches the complete catalog.
- Favorites operate on streams.
- Shared links identify the stream and program.
- Playback recovery, retry, resume, fullscreen, audio/video handling, and mobile controls remain player functions.

This is deliberate. The show system changes the **programming structure**, not the playback machinery.

## Broadcast logic

The model is based on the way independent television stations commonly mixed movies, syndicated reruns, cartoons, westerns, dramas, documentaries, sports, and other acquired programming rather than presenting viewers with a database taxonomy.

Cline TV therefore uses:

**STREAM → PROGRAM → GENRE/FORMAT**

not:

**GENRE → giant archive dump**

A future catalog can use the user's full Movies / TV / Radio genre and format system for classification without forcing every classification to become its own channel.

## What gets added later

When verified material is added:

1. Keep the original program title.
2. Keep the actual Archive.org media URL.
3. Put the program into the most appropriate existing stream.
4. Add a new stream only when the material supports a distinct programming identity.
5. Do not add filler simply to make a channel look full.
6. Do not treat recovered/harvested Archive link ledgers as automatically approved programming.
7. Holiday material is programming material, not an automatic permanent channel.
8. Special programming can be used as blocks or events without restructuring the entire station.

## Why this is different

Previous attempts repeatedly changed the channel taxonomy, which made the catalog itself unstable.

This system separates the stable parts:

- **Player:** stays stable.
- **Show system:** defines how the station is organized.
- **Catalog:** grows as verified programs are collected.
- **Guide:** exposes the catalog to the viewer.
- **Archive research:** supplies candidates; it does not decide what belongs on Cline TV.

That gives the catalog somewhere to grow without requiring another complete channel rebuild every time new material is found.

## Current state

Show System 1 is intentionally a framework.

It should now be left running long enough to judge the actual viewing experience before another structural rewrite is attempted.
