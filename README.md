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
| `guide.html` | The complete guide. Prints to A4. | Staff, leadership, anyone adopting the system |
| `svg/` | 29 individual icons, 48px grid, single colour | Canva, Affinity, the website |
| `what-to-expect-sprite.svg` | All 29 as `<symbol>` elements | Website — `<use href="#what-to-expect-volume-2">` |
| `png/black-96/` | 96px, dark, transparent background | Email, Word, quick documents |
| `png/black-192/` | 192px, dark, transparent background | Print, PowerPoint, ProPresenter |
| `png/white-192/` | 192px, white, transparent background | Dark or photographic backgrounds |
| `what-to-expect-email.html` | Table-based email snippet | Weekly congregation email |

## The measures

Six core, on everything: `volume` · `crowd` · `seating` · `space` · `length` · `order`

Four optional, when they change the answer: `bass` · `light` · `join` · `quiet`

Each has three levels, suffixed `-1`, `-2`, `-3`. Quiet space is `quiet-yes` / `quiet-no`.

## Four rules

1. The glyph carries the level — never colour on its own.
2. Always pair the icon with a word. Alt text is in the guide; use it exactly.
3. No red / amber / green. Loud is not worse than quiet, only different — and deep bass is
   the reason some people come and the reason others cannot stay.
4. The strip is a promise. If it says an hour and a half, end at an hour and a half.

## Licence

Icons are original line drawings, released under
[CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) — the same terms as the
Home Office accessibility posters this system draws on. Created for St Mungo's Church, Balerno
(Scottish Charity SC018114).

## Hosting

Static files, no build step. Cloudflare Pages: framework preset **None**, build command
**blank**, output directory **/**.
