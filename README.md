# Montserrat

A single static HTML page for learning a vocal part at home. It plays
`Montserrat.mid` with practice-friendly controls — no backend, no build step,
no install.

## Use it

The page must be served over HTTP (the MIDI file and CDN libraries won't load
from a `file://` URL). From this directory:

```bash
python3 -m http.server
```

Then open the printed address in a browser. To practise on a phone, open it on
a device on the same network using your computer's IP, e.g.
`http://192.168.1.50:8000`.

## Controls

- **Play / pause** and a running time display
- **Tempo** — slow playback to 50–100% of the original speed to practise
- **Loop** — repeat the piece while you learn it

## Files

- `index.html` — the player page
- `Montserrat.mid` — the MIDI file it plays (filename is hardcoded)

## How it works

The page uses [`html-midi-player`](https://github.com/cifkao/html-midi-player)
loaded from a CDN, so there are no dependencies to install. Everything runs in
the browser — nothing is uploaded and nothing is saved.
