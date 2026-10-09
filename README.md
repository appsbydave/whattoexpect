# What to Expect

A visual labelling system so anyone can tell, before they arrive, what a service or event
will actually be like. Built from the predictability model: when the conditions are known
in advance they hold a person up, rather than hold them down.

**Live at https://whattoexpect.appsbydave.com** — set the levels for your event, download the
graphic, put it on your flyer, leaflet, email or web page.

## Files

| Path | What it is | Use it for |
|---|---|---|
| `index.html` | The maker. Builds and downloads the finished graphic. | Ministry leads, every event |
| `key/index.html` | What the symbols mean. The visitor page the QR code opens. | Anyone who scans the code |
| `guide.html` | The complete guide. Prints to A4. | Staff, leadership, anyone adopting the system |
| `svg/` | 10 measure icons (48px grid) and 5 level marks, single colour | Canva, Affinity, the website |
| `what-to-expect-sprite.svg` | All 15 as `<symbol>` elements | Website — `<use href="#what-to-expect-volume">` |
| `png/black-96/` | 96px, dark, transparent background | Email, Word, quick documents |
| `png/black-192/` | 192px, dark, transparent background | Print, PowerPoint, ProPresenter |
| `png/white-192/` | 192px, white, transparent background | Dark or photographic backgrounds |
| `what-to-expect-email.html` | Table-based email snippet (images load from this site) | Weekly congregation email |

## The measures

Six core, on everything: `volume` · `crowd` (Attendance) · `seating` · `space` · `length` · `order`

Three optional, when they change the answer: `bass` · `light` · `join`

Plus `quiet` (quiet space), shown on everything.

Each measure has **one icon**, `what-to-expect-<measure>`, that never changes. The level is shown
by a mark beside the label: `level-1`, `level-2`, `level-3` (one, two or three bars), or `yes` /
`no` for quiet space.

## Four rules

1. One picture per measure. The picture says what it is about, never how much.
2. The bars carry the level, always with a word. Never colour on its own.
3. No red / amber / green. Loud is not worse than quiet, only different — and deep bass is
   the reason some people come and the reason others cannot stay.
4. The strip is a promise. If it says an hour and a half, end at an hour and a half.

## QR code

The maker can add a QR code to the graphic (on by default). Left at its standard link it opens
`https://whattoexpect.appsbydave.com/key/?s=2222210001`. The digits after `s=` are the event's
levels, one per measure in this fixed order:

`volume, crowd, seating, space, length, order, bass, light, join, quiet`

`0` means not shown; `1`–`3` is the level (for quiet, `1` = available, `2` = not available). The
key page reads them and opens with that event's levels in full. **If a measure is ever added, add it
at the end of the list** in both `index.html` and `key/index.html`, so codes already in print keep
working.

## Changes in v2.0 (October 2026)

From user testing feedback:

- One consistent icon per measure, instead of three different glyphs per measure. The word and
  the three bars already carry the level, so the changing glyph was redundant and doubled the
  number of pictures to learn.
- Kept the bars: they are what makes the strip readable for people who do not read English.
- Quiet space now shows a tick or a cross beside its label.
- Optional QR code on the graphic, linking to a new visitor page, *What the symbols mean*.
- Guide, icon files, sprite and email snippet updated to match. The old per-level files
  (`volume-1`, `volume-2` …) are gone.

## Licence

Icons are original line drawings, released under
[CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) — the same terms as the
Home Office accessibility posters this system draws on. Created for St Mungo's Church, Balerno
(Scottish Charity SC018114). QR codes are generated in the page with
[qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator) by Kazuhiko Arase (MIT).

## Hosting

Static files, no build step. Cloudflare Pages: framework preset **None**, build command
**blank**, output directory **/**. Upload the whole folder, including `key/`.
