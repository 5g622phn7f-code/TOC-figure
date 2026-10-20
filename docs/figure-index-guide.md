# Figure index 填写说明

[FIGURE_INDEX.csv](../FIGURE_INDEX.csv) 是项目当前登记表；[templates/figure-index.csv](../templates/figure-index.csv) 是仅含表头的空白模板。

初始三条记录仅为每节预留管理 ID，状态均为 `planned` / `unverified`。它们不表示已有图件或已开展核验；尚未发生的日期、路径、负责人和正式图号均留空。

## 字段

| 字段 | 填写规则 |
| --- | --- |
| `figure_id` | 稳定管理 ID，如 S31-F001 |
| `section` | 3.1、3.2或3.3 |
| `manuscript_figure` | 已确认的正式论文图号；未定留空 |
| `panel` | 面板标识；未定留空 |
| `working_title` | 中性主题；未定留空 |
| `treatments` | 已确认涉及的处理，多项用分号分隔；未定留空 |
| `workflow_status` | planned / drafting / review / approved / archived |
| `verification_status` | unverified / in_review / verified / not_applicable |
| `version` | 已存在文件的版本，如 v001；尚无文件留空 |
| `source_paths` | 主编辑文件的仓库相对路径，多项用分号分隔 |
| `svg_paths` | 已存在 SVG 的相对路径 |
| `ppt_paths` | 已存在 PPTX／PPT 的相对路径 |
| `tiff_paths` | 已存在 TIFF 的相对路径 |
| `code_paths` | 实际使用的代码路径；手工绘图可留空并说明 |
| `evidence_refs` | 科学内容的具体来源：文件版本、工作表／范围、分析输出或文献定位；未核验时不填成“已证实” |
| `evidence_scope` | observation / association / mechanism / mixed / not_applicable；须按实际内容核验，未知留空 |
| `export_specs` | 实际导出尺寸、dpi、色彩模式与编辑限制等 |
| `owner` | 实际负责人；未知留空 |
| `reviewer` | 实际核验人；未知留空 |
| `updated_on` | 该条登记最近更新日期，YYYY-MM-DD |
| `verified_on` | 核验完成日期；未完成留空 |
| `history_path` | 已存在的图件版本历史文件相对路径 |
| `notes` | 待办、编辑限制、来源说明、缺失格式等 |

## 状态语义

- `planned`：已登记，尚未制作；`drafting`：制作中；`review`：待审；`approved`：已明确批准用于当前目标；`archived`：历史版本或不再使用。
- `unverified`：科学内容尚未核验；`in_review`：核验中；`verified`：有明确核验人、来源和日期；`not_applicable`：纯管理或无科学断言的对象，须备注原因。
- 布局认可、代码运行、文件导出、Git提交都不能自动把科学状态改为 `verified`。
- 关联分析不能仅因连线存在就登记为机制证据。机制类内容需逐项追溯到与其相符的验证来源。
- 缺少来源、文件或核验信息时如实保留空白或未核验，不填推测值。

## 更新方式

CSV 为 UTF-8、逗号分隔；字段中含逗号、换行或双引号时按标准 CSV 引用。多路径字段优先用分号分隔。建议每个图件保留一条当前记录，面板细节和历史版本放入相应历史文件，避免把多个版本误当作独立图件。
