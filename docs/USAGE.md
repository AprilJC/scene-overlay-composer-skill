# Usage guide

## 1. Classify every image

Use these labels in a prompt when several images are attached:

- **Main photo:** the image to edit and preserve.
- **UI source:** screenshot whose controls, structure, colours, and visible copy should be reproduced.
- **Layout reference:** reference for hierarchy, scale, overlap, and material only; do not copy its unrelated subject/content.
- **Content source:** album art, route, workout values, colour swatches, or other factual input.

Example:

```text
Image 1 is the main photo. Image 2 is a layout reference. Image 3 is the exact UI source.
Keep Image 1's person and setting unchanged; reproduce only Image 3's interface anatomy.
```

## 2. Pick a visual family

| Goal | Skill | Strong composition |
| --- | --- | --- |
| Calendar / AirDrop / Photos selection / share sheet | Native UI | One large card or sheet behind the subject. |
| macOS folders, context menu, cursor, desktop search | Native UI | Sparse desktop field, subject as wallpaper. |
| One track or player | Music | One wide or tall player card behind the subject. |
| Playlist | Music | A large, backgroundless playlist field, not an opaque card. |
| Running or fitness data | Activity | Type directly on a wall, road, sky, or ground plane. |
| One star/heart/flower | Stickers | One large rear shape fused with the subject silhouette. |
| Multiple doodles/collage pieces | Stickers | One dominant mass plus a small intentional constellation. |

## 3. Supply factual information only when it matters

Supply exact song/artist/album artwork for a player, exact schedule/event data for Calendar, and exact activity metrics for a workout edit. If a music request has no song at all, the music skill selects a random current Billboard Hot 100 entry using the official chart, then says which one it used. If chart access is unavailable, it asks for a song rather than inventing metadata.

## 4. Ask for depth explicitly

The essential request language is: **“Put the element behind the person; make their hair/shoulder/torso/bag/legs occlude its edge. Do not cover their face, hands, phone, or held object.”**

Good prompt:

```text
Create an iOS Photos selection sheet that fills most of the width. Put it behind the person.
The photo rail should resume on either side of her shoulders, and the bottom sheet edge should run behind her skirt and legs.
```

Weak prompt:

```text
Add an iOS UI on the left.
```

The weak version leaves scale and depth unresolved, so it may produce a detached sticker.

## 5. Review and iterate

Review at normal size and thumbnail size. Ask for one targeted adjustment per iteration: enlarge the hero card, shift it behind the shoulder, replace a made-up UI with the supplied screenshot, reduce copy, or restore a protected object. Do not ask for a broad “make it better” pass when a single visible issue can be named.

## Native UI examples

```text
$scene-native-ui-composer
Main photo: attached gallery portrait.
Use an iOS Photos selection sheet. It should span 85% of the width, include a selected-photo header, Options pill, crop rail, and two blue selection checks. The person must appear in front of the sheet and interrupt the rail with her hair, shoulders, bag, skirt, and legs.
```

```text
$scene-native-ui-composer
Main photo: attached street portrait. UI source: attached AirDrop screenshot.
Preserve the UI source's title, preview placement, actions, and colours exactly. Place the alert behind the subject so their torso crosses the action row and the card continues on both sides.
```

## Boundaries

Do not use these skills to fabricate an actual account state, personal schedule, health record, live player activity, or official app integration. Generic non-factual UI content is acceptable only when it is clearly decorative and not presented as the user's data.
