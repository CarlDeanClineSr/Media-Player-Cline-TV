# CLINE TV — SHOW SYSTEM 1

## Purpose

Cline TV is a television service, not an Internet Archive browser.

The Archive is the source warehouse. The repository's seven library files are the station inventory. The seven channels are the programming streams. The Guide is the viewer catalog.

## Source of truth

The seven files in `library/` are the editable programming source:

1. `01-tv-classics.md` — TV CLASSICS
2. `02-movies.md` — MOVIES
3. `03-family-cartoons.md` — FAMILY & CARTOONS
4. `04-documentaries.md` — DOCUMENTARIES
5. `05-radio.md` — RADIO
6. `06-sports.md` — SPORTS
7. `07-tv-series.md` — TV SERIES

`index.html` reads these files directly at runtime.

There is no hand-built show list inside `index.html`, and `CHANNEL_LIBRARY.md` is only a map to the seven files.

This keeps the system simple:

**Archive research → library files → seven channels → player**

## Why seven channels

The older Cline TV build already established a seven-channel structure covering the full collection. It is broad enough for normal channel surfing and simple enough to maintain.

The channels are not supposed to be artificial genre fragments.

A movie stays with MOVIES. Cartoons and family programs stay with FAMILY & CARTOONS. Radio stays with RADIO. Sports stays with SPORTS. The television-series collection stays with TV SERIES.

More detailed subjects can remain inside a library file without creating another channel.

## Current catalog

The seven library files contain 5,469 unique program URLs after recovering the missing Dragnet `5x04 The Big Lift` entry from the older repo. One clearly unsuitable title, `The Child Molester (1964)`, is held separately and is not broadcast.

The exact count is generated from the files, not typed into the player.

## Player behavior

The existing television controls remain the playback system:

- Program dial moves through programs in the current channel.
- End of stream advances to the next channel.
- Channel dial changes channels.
- Guide searches the complete on-air catalog.
- Favorites save channels.
- Share identifies the selected program and channel.
- Retry, resume, playback checks, fullscreen, mobile controls, audio handling, and video handling remain player functions.

The player determines audio/video mode from the actual media URL, so RADIO remains compatible with the same player.

## Review rule

A program should not be rejected just because a word in its title looks sensitive. Context matters.

Example: a science documentary titled `Murder, Rape and DNA` belongs with science material because the title describes its scientific subject.

Conversely, a clearly inappropriate program such as `The Child Molester (1964)` is placed in `CONTENT_REVIEW_HOLD.md` rather than being broadcast automatically.

## What must not happen again

Do not build a second giant catalog inside the player.

Do not scatter movies across unrelated channels because an automated classifier thinks they match a keyword.

Do not use anonymous Archive search matches as automatic programming decisions.

Do not replace the user's collected library with a smaller hand-picked sample.

Do not make the code harder to manually maintain.

## Editing

The intended maintenance operation is simple:

`- Program Title — https://archive.org/...`

Place the line in the appropriate one of the seven Markdown files.

That is the programming interface. The television code should not need to change when programs are added, removed, or corrected.
