# 文件命名规范

本规范适用于新建图件文件与代码。以下文件名仅说明命名方式，不表示文件已经存在或结果已经核验。

## 稳定图件 ID 与公共文件名

- 图件 ID：`S31-F001`、`S32-F001`、`S33-F001` 分别对应3.1、3.2、3.3的首个登记图件。
- `F001` 是章节内管理序号，不是正式论文 Figure 1。正式图号在索引 `manuscript_figure` 字段单独记录；重排论文图号时保留图件 ID。
- 同一图件跨版本保留 ID，不把旧 ID 分配给其他图件。
- 公共文件名格式：`<figure_id>_<panel>_<treatment>_<topic>_vNNN_YYYYMMDD.<ext>`。
- 新建文件名使用 ASCII 字母、数字、连字符及下划线，不使用空格。路径相对仓库根目录记录。
- `panel`：单面板用 `panel-A`；整图用 `all`。未知时用 `panel-TBD`。
- `treatment`：`TWP`、`TWP-C`、`TWP-B`；多处理组合用 `multi`，具体清单登记在索引；未知用 `TBD`。
- `topic`：简短、中性的内容标签，如 `surface`、`arg-profile`、`community`。避免用未经核验的 `increase`、`enhanced-transfer` 等结果性命名。
- `vNNN`：从 `v001` 开始的图件版本。内容、排版或导出参数变更均递增；不要使用 `final`、`final2`。
- `YYYYMMDD`：本版本归档日期，按 Asia/Shanghai 时区；不是采样日期，也不是实验日期。同日可有多个递增版本。
- 样本代码属于原始数据标识，不应从文件名推断或重写样本信息。

## 各类文件示例

| 类型 | 目录 | 命名示例 |
| --- | --- | --- |
| SVG 导出 | `svg/` | `S31-F001_all_TWP-C_surface_v001_20261020.svg` |
| PowerPoint | `ppt/` | `S31-F001_all_TWP-C_surface_v001_20261020.pptx` |
| TIFF 导出 | `tiff/` | `S31-F001_all_TWP-C_surface_v001_20261020.tif` |
| 原生 SVG 工程 | `source/` | `S31-F001_all_TWP-C_surface_v001_20261020.svg` |
| 原生 AI 工程 | `source/` | `S31-F001_all_TWP-C_surface_v001_20261020.ai` |
| 图注或制作说明 | `source/` | `S31-F001_all_TWP-C_surface_v001_20261020_notes.md` |
| R 绘图代码 | `code/` | `draw_S31-F001_all_TWP-C_surface_v001_20261020.R` |
| Python 导出代码 | `code/` | `export_S31-F001_all_TWP-C_surface_v001_20261020.py` |

代码前缀允许 `draw_`、`export_`、`assemble_`；依赖文件可沿用生态标准名称，如 `requirements.txt`、`renv.lock`，并在索引或制作说明中关联。文件版本必须对应实际生成该图的代码版本，不能仅把旧代码改名。

## 导出与编辑信息

- 同一发布批次的源文件、SVG、PPTX、TIFF使用相同 ID、版本和日期；未生成的格式在索引留空，不伪造路径。
- SVG 记录文字可编辑性、外部资源和字体要求；需要独立交付时嵌入必要资源。转曲副本在日期前加 `_outlined`，并保留可编辑主文件。
- PPTX 记录哪些元素可编辑、哪些是嵌入图片。扩展名本身不能证明可编辑。
- TIFF 默认计划使用600 dpi；最终以实际期刊要求和核验后的导出参数为准。将真实尺寸、dpi及色彩模式写入 `export_specs`。不能仅改写dpi元数据来冒充高分辨率。
- 若同版本存在不同尺寸导出，在版本号前加用途标签，如 `_print`、`_preview`，并分别登记路径与参数。
- 未修改的外部素材或原始文件保留原名，在制作说明记录原名、来源与关联图件 ID；不得覆盖原始数据。

## 版本与提交

1. 更新图件文件，递增版本号。
2. 更新 Figure index 中的路径、版本、日期和实际状态。
3. 更新该图件的 `<figure_id>_history.md`，说明变更、来源和核验情况。
4. 在一次 Git 提交中尽量包含该版本的源文件、代码、导出文件及追踪记录。
5. 建议提交信息：`docs: initialize figure tracking`、`fig(S32-F001): update layout to v002`。不在提交信息中添加未核验结论。
