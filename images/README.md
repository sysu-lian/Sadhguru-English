# images/ —— 900 张词卡配图，随仓库发布

这些图**就在仓库里**，clone 下来就有，不用跑任何下载脚本。

```
images/
├── 01-100/   100 张词（001 … 100）
├── 101-200/  100 张词（101 … 200）
├── …
├── 801-900/  100 张词（801 … 900）
└── README.md 本文件
```

每个区间目录里是**同一词的双格式**：

```
images/01-100/
├── american.webp     ← 主档
├── american.jpg      ← 兜底
├── life.webp
├── life.jpg
└── …
```

命名规则 `<词形小写>.<ext>`，例如 `american.webp`、`effort.jpg`。
排序即词频序，看 `data/words-1-3878.csv` 的 `seq` 对得上号。

## 规格

| 项      | 值                                |
| ------ | -------------------------------- |
| 尺寸     | 512 × 512                        |
| WebP   | quality 80, method 6（主档）          |
| JPEG   | quality 90, progressive, optimize（兜底） |
| 画风     | 白底 / 粗黑描边 / 扁平矢量，无文字、无字母     |
| 单张均值   | WebP ≈ 25 KB、JPEG ≈ 51 KB          |
| 合计     | 1800 个文件 ≈ 67.6 MB（900 词 × 双格式） |

## 用法

- **本地站 / Anki 导入**：直接按 `images/<区间>/<词>.webp` 引相对路径。
- **想挂 CDN 不想背 67 MB**：`data/manifest-images.csv` 里已经有线上地址，指过去即可。
- **只想给一小段做 demo**：用 `data/words-1-900.csv` 里的 `image` 字段拿到路径，再去对应区间取。

## 许可

图片 **CC BY 4.0**，可商用，署一句话就够了：

> 配图来自 Sadhguru-English（CC BY 4.0），由 学达单词 维护。

图片由 FLUX.1 [schnell] 生成（该模型权重 Apache-2.0），是本项目用原创提示词生成的
卡通角色插画，不含任何真人的照片级肖像。许可全文见仓库根目录 [`LICENSE`](../LICENSE)（CC BY 4.0）；
「学达单词」「Sadhguru-English」的名称与标识为商标，不在授权范围内。

**含演讲原文、金句、语录的内容不在本目录，也不要往里放。**
