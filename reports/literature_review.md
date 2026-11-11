# 甲骨文数字化与 AI 辅助释读：Sprint 1 文献综述

调查日期：2026-11-11；状态：REVIEW（桌面研究，待全文/补充材料复核和专家审阅）。

## 1. 总览

2026 年综述将甲骨文信息处理归纳为图像增强、字符检测与识别、字形分类、碎片缀合、语境理解和释读等相互依赖任务。核心困难包括材料碎片化、同字异体多、不同字形视觉相似、拓片噪声、未释读字低频长尾、闭集分类器遇到未知类强行归类，以及人类评估协议缺少统一标准。

直接启示：字符识别准确率不等于释读准确率；必须研究未知类拒识、证据可追溯、长尾泛化和专家评估。

## 2. 代表性研究

### HUST-OBC — Scientific Data, 2024
论文：https://www.nature.com/articles/s41597-024-03807-x；代码：https://github.com/Pengjie-W/HUST-OBC
报告140,053张图像：已释读1,588类、77,064张；未释读9,411类、62,989张。论文说明CC BY-NC 4.0非商业许可。
价值：视觉检索、长尾分布、开放集识别和数据质量研究。
审查：9,411是数据集类别口径，不等于学界确认的独立未释读字数；需检查原始出处、重复裁切、来源泄漏；不能作为无条件商业训练资源。

### OBIMD — Scientific Data, 2026
论文：https://www.nature.com/articles/s41597-026-06967-0；数据：https://huggingface.co/datasets/KLOBIP/OBIMD；代码：https://github.com/libang1991/OBIMD
报告10,077张图像、93,652字符标注、21,667缺字位置、21,941句子单元、4,192非句子元素，覆盖商代五个时期。Hugging Face 数据卡片标注CC BY 4.0。
价值：支持图像、字符、缺字位置和句子/释文序列联合研究。
审查：需核对补充材料、标注规范、划分、来源图像第三方权利；数据集许可不自动覆盖每张底层图像版权。

### AlphaOracle — The Innovation, 2026
论文：https://doi.org/10.1016/j.xinn.2026.101462；代码：https://github.com/Yuliang-Liu/AlphaOracle
流程包括拓片解析、部件/形态分析与历时建模、上下文检索与语义对齐、传世文献及现代学术材料中的训诂验证。论文报告定量实验和86名领域专家/博士研究人员参与的评估。
价值：已经实现“形体—语境—训诂”证据链工作流，是必须对标的直接相关系统。
审查：作者报告不等于新释读已成学界共识；需独立复核测试集、基线公平性、专家评分协议和可复现性。Apache-2.0软件许可不意味着聚合书籍、拓片和数据库图像可自由再分发或商业训练。

### 甲骨文信息处理综述 — npj Heritage Science, 2026
论文：https://www.nature.com/articles/s40494-026-02511-w
按任务梳理识别、缀合、分类和释读，强调数据极不平衡、未释读字低频、未知类拒识不足、单模态视觉缺少辞例语义及人类评估不统一。提出透明度、评分质量、评估维度、标注者资质、文献依据和实证验证等评价要素。

### 早期机器学习与计算文字学
- Han et al. (2021), Self-supervised learning of Orc-Bert augmentor for recognizing few-shot oracle characters, ACCV. DOI: https://doi.org/10.1007/978-3-030-69544-6_39
- Deciphering ancient Chinese oracle bone inscriptions using case-based reasoning (2021), ICCBR. DOI: https://doi.org/10.1007/978-3-030-86957-1_21
- 殷契文渊：2019年发布，后续建设字形、著录、文献和知识服务；2024年腾讯披露平台升级了浅刻痕可视化和AI字形映射功能。

## 3. 任务格局

| 任务 | 已有基础 | 仍需验证 |
|---|---|---|
| 图像增强/拓片解析 | AlphaOracle、平台工具 | 不同拓片、光照、骨裂和浅刻痕下的稳定性 |
| 检测/分割 | 平台数据、通用检测模型 | 跨来源泛化、边界一致性、复杂粘连 |
| 已知字识别 | HUST-OBC等 | 长尾类别、异体、开放集拒识 |
| 字形相似检索 | 视觉表示、AlphaOracle检索 | 相似度是否有文字学意义及出处可追溯 |
| 上下文补缺/辞例理解 | OBIMD、AlphaOracle | 模板造成的数据泄漏、跨组类泛化 |
| 训诂与释读 | AlphaOracle工作流 | 专家盲测、反证、可复现证据链 |
| 碎片缀合 | 既有计算研究和数据库 | 物理证据与文本证据的联合评价 |

## 4. 综合结论

不宜把项目定位为再做一个通用OCR、数据库或直接翻译未释文字。更有价值的方向是：**可独立验证的开放集疑难释读评测与证据审计**。针对罕见/未知/残损字形，系统应能识别证据不足、检索可比字形和辞例、给出候选理由与反证，并在专家盲评下校准，而不是只输出一个现代汉字。

## 5. 下一轮工作
1. 下载并阅读2026综述和AlphaOracle补充材料，建立文献矩阵。
2. 抽样审计HUST-OBC、OBIMD、AlphaOracle数据结构、重复和划分。
3. 联系殷契文渊、小學堂、傅斯年图书馆核实API/导出/授权。
4. 邀请甲骨学研究者校订问题分类。

## References
- Chen et al. (2026), npj Heritage Science. https://www.nature.com/articles/s40494-026-02511-w
- Wang et al. (2024), Scientific Data. https://www.nature.com/articles/s41597-024-03807-x
- Li et al. (2026), Scientific Data. https://www.nature.com/articles/s41597-026-06967-0
- Liu et al. (2026), The Innovation. https://doi.org/10.1016/j.xinn.2026.101462
- Tencent (2024-05-27), 殷契文渊平台介绍. https://www.tencent.com/index.php/zh-cn/articles/2201854.html
