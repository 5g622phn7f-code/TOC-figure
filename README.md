# TOC-figure

用于组织、命名、追踪 TWP、TWP-C 和 TWP-B 相关论文图件的项目管理仓库。

**初始化范围：仅建立管理结构与模板。当前未收录图件、实验数据、分析结果或科学结论。** 目录名称、图件编号和模板示例均不构成结果声明，也不代表正式论文图号。

## 快速开始

1. 阅读[目录结构](docs/directory-structure.md)与[命名规范](docs/naming-conventions.md)。
2. 在 [Figure index](FIGURE_INDEX.csv) 中登记图件；新增条目可复制[空白 CSV 模板](templates/figure-index.csv)。
3. 仅将已获准归档的真实文件放入相应章节和格式目录，不创建虚假的 SVG、PPT 或 TIFF 文件。
4. 按[索引填写说明](docs/figure-index-guide.md)记录源文件、代码、证据来源及核验状态。
5. 每次更新图件版本时，填写[图件版本历史模板](templates/version-history.md)，并在 [CHANGELOG](CHANGELOG.md) 记录项目级变更。

## 章节入口

| 章节 | 管理主题（非结果结论） | 目录 |
| --- | --- | --- |
| 3.1 | 颗粒表征及化学／界面特征图件 | [section-3.1](figures/section-3.1/README.md) |
| 3.2 | ARG 丰度、组成及风险分类相关图件 | [section-3.2](figures/section-3.2/README.md) |
| 3.3 | 细菌群落及其与 ARG 关联相关图件 | [section-3.3](figures/section-3.3/README.md) |

以上主题用于归档；正式章节标题、面板和内容须与核验后的稿件逐项对应。当前范围为 TWP、TWP-C、TWP-B；其他处理需明确确认后登记。

## 管理约定

- 源文件、派生导出和绘图代码通过同一图件 ID、版本号及日期关联。
- 图件进度与证据核验状态分别记录；“已导出”不等于“结果已核验”。
- 未核验内容留空或明确标记“未核验”；不得补写实验数值、显著性、机制箭头或结论。
- 科学表述须区分观察、统计关联与机制验证，并能追溯到具体来源。
- 正式归档保留可编辑源文件；仅嵌入位图的 PPT 不得标作“完全可编辑”。
- 本次未上传任何数据。后续上传前需确认数据和第三方素材可公开；原始文件应保留原名及来源，不为符合命名规则而覆盖原件。
- Git 记录文件变更；人工版本历史记录修改原因、来源与核验信息。提交本身不代表科学审核通过。

## 文件入口

- [Figure index](FIGURE_INDEX.csv)
- [目录结构说明](docs/directory-structure.md)
- [SVG／PPT／TIFF／源文件／代码命名规范](docs/naming-conventions.md)
- [Figure index 填写说明](docs/figure-index-guide.md)
- [Figure index 空白模板](templates/figure-index.csv)
- [图件版本历史模板](templates/version-history.md)
- [项目版本历史](CHANGELOG.md)
