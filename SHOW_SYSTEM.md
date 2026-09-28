# CLINE TV — SHOW SYSTEM 1

## Purpose

Cline TV is a television service, not an Internet Archive browser.

The Archive is the source warehouse. The repository library is the station inventory. The channel sections in `library/CHANNEL_LIBRARY.md` are the programming streams. The Guide is the viewer catalog.

## Source of truth

`library/CHANNEL_LIBRARY.md` is the authoritative on-air catalog.

`index.html` reads that file at runtime. It no longer carries a separate hard-coded list of programs.

This keeps the parts separate:

**Archive research → repository library → channel organization → player**

## Current lineup

The organized library currently supplies 18 broadcast channels and 5,433 on-air programs.

The library also contains a 35-program REVIEW HOLD section. Those entries remain in the repository but are not put on-air automatically.

| Ch | On-air identity |
|---:|---|
| 1 | FEATURE FILMS |
| 2 | SCI-FI & SPACE FILMS |
| 3 | HORROR & MONSTERS |
| 4 | FAMILY, COMEDY & WESTERNS |
| 5 | CLASSIC TV |
| 6 | SCI-FI TV |
| 7 | CRIME & MYSTERY TV |
| 8 | FAMILY & CHILDREN TV |
| 9 | DOCUMENTARIES |
| 10 | SCIENCE & COSMOS |
| 11 | HISTORY & WAR |
| 12 | SPACE & NASA |
| 13 | SPORTS |
| 14 | OLD-TIME RADIO |
| 15 | RADIO DRAMA & MYSTERY |
| 16 | MUSIC & JAZZ |
| 17 | NEWS & PUBLIC AFFAIRS |
| 18 | EDUCATION & TECHNOLOGY |

## Player behavior

The existing television controls remain the playback system.

Program dial: moves through programs in the current channel.

Channel dial: changes channels.

End of stream: advances to the next channel.

Guide: searches the complete on-air catalog.

Favorites: save channels.

Share: identifies the selected channel and program.

Recovery, retry, resume, fullscreen, mobile controls, and playback checks remain player functions.

Media mode is determined from the individual program URL, so a channel can contain both audio and video records without forcing the whole channel into one mode.

## Organization rule

**STREAM → PROGRAM → GENRE/FORMAT**

Channel organization is for television-style viewing. More detailed classification can remain in the library without becoming a separate channel.

## Catalog rule

When new programs are collected:

1. Keep the original title.
2. Keep the actual direct media URL.
3. Place the entry in the appropriate channel section of `CHANNEL_LIBRARY.md`.
4. Review held material before putting it on-air.
5. Do not replace the full catalog with a small sample list.

The player should read the library. The library should not be reduced to fit the player.

## Stable architecture

- Archive: acquisition and public media source.
- `library/CHANNEL_LIBRARY.md`: organized on-air inventory.
- `index.html`: television interface and library reader.
- Guide: viewer navigation.
- SHOW_SYSTEM.md: organization rules.

Keep the television stable and let the library grow.
