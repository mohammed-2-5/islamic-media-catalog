# Islamic Media Catalog

CDN-hosted catalog for the Azkar app's Audio Hub scholars section.

**CDN base:** `https://cdn.jsdelivr.net/gh/mohammed-2-5/islamic-media-catalog@master`

## Structure

```
catalog.json                          ← All scholars list
scholars/{id}/playlists.json          ← Playlists + episodes per scholar
```

## Scholars

| ID | Name |
|----|------|
| yousef_al_qatt | يوسف القط |
| mohammed_al_ghaliz | محمد الغليظ |
| amjad_samir | أمجد سامر |
| abdulrahman_al_harami | عبد الرحمن الحرمي |
| ahmed_al_arabi | د. أحمد العربي |
| yasser_al_hazimi | ياسر الحزيمي |

## Adding YouTube IDs

Each episode has a `youtube_id` field. Set it to the 11-character YouTube video ID.

Example: for `https://youtube.com/watch?v=dQw4w9WgXcQ` → `"youtube_id": "dQw4w9WgXcQ"`

Also set `youtube_channel_id` in `catalog.json` for each scholar (the `UCxxxxxx` part from their channel URL).

## Adding a New Scholar

1. Add entry to `catalog.json`
2. Create `scholars/{new_id}/playlists.json`
3. Commit and push — CDN updates automatically via jsDelivr
