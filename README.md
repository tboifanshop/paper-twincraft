# Paper Twincraft — Deltatube

A Deltarune-themed YouTube-style PWA designed for GitHub Pages.

## Pages

| Page | Description |
|------|-------------|
| `index.html` | Flash/Ruffle game overlay (mobile controls) |
| `shorts.html` | **Deltatube Shorts** — soul-controlled short-video feed |

---

## Deltatube Shorts

A vertical short-video feed you navigate using a controllable red pixel-art **soul** (heart).

### Controls

#### Desktop (keyboard)

| Key | Action |
|-----|--------|
| `W` / `↑` | Move soul up |
| `S` / `↓` | Move soul down |
| `A` / `←` | Move soul left |
| `D` / `→` | Move soul right |

#### Mobile

An on-screen **four-way D-pad** (Joy-Con style) appears on touch devices.  
Drag the stick up/down/left/right to move the soul.

---

### Soul Mechanics

#### Scrolling between shorts

Move the soul to the **bottom edge** of the screen and hold it there for **2 seconds**
→ loads the next short.

Move the soul to the **top edge** and hold for **2 seconds**
→ loads the previous short.

A progress ring fills during the hold and resets if you leave the zone.
You must leave and re-enter the zone to trigger again (debounced).

#### Liking

Move the soul over the **♥ Like** button and keep it there for **2 seconds**.  
The Like text turns **yellow** when toggled on, and returns to white when toggled off.  
You can also tap/click the button directly as a fallback.

#### Subscribing

Move the soul over the **Subscribe** button and hold for **2 seconds**.  
A **pixel explosion** effect fires on toggle.  
Direct tap/click also works as a fallback.

---

### Deployment (GitHub Pages)

No build step required. Push to `main` and enable GitHub Pages from the repository
settings (source: root of `main` branch).

The service worker (`sw.js`) caches `index.html` and `shorts.html` for offline use.
