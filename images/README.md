# images/ —— 1711 词配图

配图随仓库发布，已覆盖 **1–1410、1700–2000**，缺少 **1411–1699、2001–3878**。
每词有 512×512 的 WebP 和 JPEG 两种格式，共 3422 个图片文件。

文件按百词区间存放，名称为 `<词形小写>.webp` 或 `.jpg`。序号与词形以
`data/words-1-3878.csv` 为准，实际路径见 `data/manifest-images.csv`。

## 规格与来源

- WebP：quality 80，method 6；JPEG：quality 90，progressive、optimize。
- 既有批次采用 FLUX.1 [schnell] 生成的卡通插画。
- 1700–2000 按 v3 规格书新绘或复用已有底图；新绘使用内置 image_gen，采用暖米色纸张、水彩和彩铅质感，并沿用固定角色参考。
- 新批次的场景、提示词和处理方式见 `data/illustrations-1700-2000.json`。带 `overlay` 的条目保留底图，显示时可按 `[cx, cy, rx, ry]` 在 0–100 坐标系上叠加椭圆圈选。
- 新增条目的 CDN 字段暂留空，可直接使用清单中的本地路径。

## 许可

图片 **CC BY 4.0**，可商用，使用时请署名：

> 配图来自 Sadhguru-English（CC BY 4.0），由 学达单词 维护。

许可全文见根目录 [LICENSE](../LICENSE)；「学达单词」「Sadhguru-English」的名称与标识为商标，不在授权范围内。
图片为插画，不含真人照片。含演讲原文、金句、语录的内容不在本目录。
