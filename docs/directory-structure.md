# 3.1–3.3 目录结构

每节具有相同的五类子目录，均已用 `.gitkeep` 占位。Git 不追踪空目录；占位文件不是图件，有实际文件后可删除。

| 路径 | 用途 |
| --- | --- |
| `figures/section-3.1/` | 3.1 颗粒表征及化学／界面特征图件 |
| `figures/section-3.2/` | 3.2 ARG 丰度、组成及风险分类相关图件 |
| `figures/section-3.3/` | 3.3 细菌群落及 ARG 关联相关图件 |
| `docs/` | 项目管理说明与规范 |
| `templates/` | 可复制的索引与版本历史模板 |
| `FIGURE_INDEX.csv` | 跨章节图件登记表 |
| `CHANGELOG.md` | 项目级变更记录 |

## 每节内部结构

下列路径中的 `section-3.x` 代表实际目录 `section-3.1`、`section-3.2` 或 `section-3.3`，不是另建的目录。

| 相对路径 | 存放内容 | 规则 |
| --- | --- | --- |
| `figures/section-3.x/svg/` | SVG 矢量导出 | 记录文字是否可编辑；转曲版本须单独标注 |
| `figures/section-3.x/ppt/` | PowerPoint 编辑版或展示版 | 默认扩展名 `.pptx`；如确有旧版 `.ppt`，登记兼容性与编辑限制 |
| `figures/section-3.x/tiff/` | TIFF 投稿导出 | 扩展名统一 `.tif`；记录实际尺寸、分辨率和色彩模式 |
| `figures/section-3.x/source/` | 原生编辑工程、素材及制作记录 | 如 AI、Inkscape SVG、PPTX；保留来源与素材授权记录 |
| `figures/section-3.x/code/` | 绘图、排版和导出代码 | 如 R、Python、JavaScript；记录依赖及输入路径 |

若原生工程就是 SVG 或 PPTX，`source/` 中保留主编辑文件，`svg/` 或 `ppt/` 中存放对应交付副本；在索引中明确主文件。不要把导出副本当作独立的新图件。

## 追踪文件位置

每个图件可在所属章节根目录新增 `<figure_id>_history.md`，由版本历史模板复制。图注及制作说明可存入同节 `source/`，并在索引 `notes` 字段注明路径。未经核验的科学内容不得填入这些记录。

本次不预设正式图号、不建立数据文件、不提供分析或绘图脚本实现。跨章节图件以主归属章节存放，在索引中备注其他章节，避免多份主文件。
