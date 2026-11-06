# 🌌 webgl-fx

> Real-time 3D and WebGL environments — particle systems, galaxy, wave grid. Mouse-reactive. Zero config beyond Three.js.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## Scenes

| Scene | Description |
|-------|-------------|
| `particles` | 3000-point drifting particle cloud, mouse-reactive rotation |
| `galaxy` | Spiral galaxy with multi-arm structure and vertex colors |
| `waveGrid` | Animated sine-wave point grid, mouse-reactive camera |

## Install

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
<script src="https://cdn.jsdelivr.net/gh/hojullc/webgl-fx@1/src/webgl-fx.js"></script>
```

## Quick start

```js
const canvas = document.querySelector('canvas');

// Particle cloud
WebglFx.particles(canvas, { count: 3000, color: 0x7064ff, mouse: true });

// Galaxy with spiral arms
WebglFx.galaxy(canvas, { arms: 3, inner: 0xff6b9d, outer: 0x7064ff });

// Animated wave grid
WebglFx.waveGrid(canvas, { cols: 60, rows: 60, amp: 20 });
```

## Options

### particles(canvas, opts)
| Option | Default | Description |
|--------|---------|-------------|
| `count` | `3000` | Number of particles |
| `color` | `0x7064ff` | Point color |
| `size` | `1.5` | Point size |
| `spread` | `400` | Cloud volume |
| `mouse` | `true` | Mouse-reactive rotation |

### galaxy(canvas, opts)
| Option | Default | Description |
|--------|---------|-------------|
| `arms` | `3` | Number of spiral arms |
| `radius` | `180` | Galaxy radius |
| `inner` | `0xff6b9d` | Inner color |
| `outer` | `0x7064ff` | Outer color |

### waveGrid(canvas, opts)
| Option | Default | Description |
|--------|---------|-------------|
| `cols` / `rows` | `60` | Grid dimensions |
| `amp` | `20` | Wave amplitude |
| `speed` | `0.015` | Animation speed |

## License

MIT © [Hoju LLC](https://hoju.us)
