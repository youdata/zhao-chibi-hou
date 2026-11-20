# 赵孟頫 · 行书后赤壁赋

赵孟頫《行书后赤壁赋》（台北故宫博物院藏） — a narrated deep-zoom reading, as a static page (in Chinese).

Zhao Mengfu's running-script Latter Ode on the Red Cliff (National Palace Museum, Taipei): its 31 columns, each with its modern reading, his inscription of 1301 and the colophons of 鲜于枢, 唐棣, 班惟志 and 赵奕.

Live: https://youdata.github.io/zhao-chibi-hou/

The image pyramid is a tile folder (`zhao-chibi-hou/`: `header.idx` + `{z}/{x}/{y}.png`), so any static host serves it.
Its fonts are in `fonts/`, trimmed to the page's characters. The narrated video is not included.

## How it is made

From `infographic-examples/zhao-chibi-hou/build.mjs` (the page) with rx (`~/rx-cli`):

```sh
node build.mjs                                                     # → zhao-chibi-hou.json
rx export zhao-chibi-hou.json --out site --app /rx-graphic-editor/web/index.html --canvas --theme dark --lock-layers --tiles dir
rx publish site --to github:youdata/zhao-chibi-hou --yes
```
