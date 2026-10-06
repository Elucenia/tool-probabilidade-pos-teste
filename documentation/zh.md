<!-- ELUCENIA technical documentation · probabilidade-pos-teste · zh · no clinical/professional/rights approval -->

# 验后概率（Bayes 定理）

[条件、来源与许可](https://elucenia.org/zh/tools/probabilidade-pos-teste)

## 使用方法

在门户中使用工具，或通过本地 HTTP 服务器打开 index.html。选择语言，填写各字段，然后计算。

## 输入与单位

### 验前概率（患病率或临床估计）

`pre`

% · 范围: 0.1–99.9

### 结果似然比（阳性用 LR+，阴性用 LR−）

`rv`

范围: 0.001–1000

## 方法版本

贝叶斯比值（odds）：Fagan 1975；验前比值×似然比及验后换算；Deeks–Altman 2004似然比

## 已记录的公式

验前比值（odds） = p / (1 − p) · 验后比值 = 验前比值 × 似然比 · 验后概率 = 验后比值 / (1 + 验后比值).

这是贝叶斯定理的比值（odds）形式，Fagan列线图以图形求解。

## 限制与适用人群

验前概率应代表所评估的人群和临床情境；似然比须与检测及结果类别相对应。概率与比值（odds）是不同的量：更新时先将 odds 乘以似然比，再转换回概率。预测值随患病率而变化，不能自动在研究或服务机构之间移用。计算只是更新估计，不能单独确诊或排除疾病。

## 参考文献

- [Fagan TJ. Nomogram for Bayes's theorem. N Engl J Med, 1975.](https://doi.org/10.1056/NEJM197507312930513)

- [Deeks JJ, Altman DG. Diagnostic tests 4: likelihood ratios. BMJ, 2004.](https://doi.org/10.1136/bmj.329.7458.168)

- [Deeks/Altman2004,Diagnostic tests4:likelihood ratios](https://pmc.ncbi.nlm.nih.gov/articles/PMC478236/)

- [Fagan1975](https://doi.org/10.1056/NEJM197507312930513)

## 复现技术测试

在此仓库的根目录中运行 node test.cjs，以重复已记录的合成案例。原始输入、预期结果和容差保持不变。技术测试不构成临床验证。

```sh
node test.cjs
```

tool.json 包含来源、版本和审查范围。examples.json 保留合成输入与预期结果；results.json 记录实际得到的结果。

[记录与参考文献](../tool.json) · [JavaScript代码](../calculator.js) · [参考案例](../examples.json) · [results.json](../results.json)

## 审查与使用条件

尚未开展独立临床审查。

此界面为自主编写的翻译，并非官方或认证版本。尚未完成独立临床审查、专业语言审查或工具权利授权。

公式或分类结果。解释、处理及适用性须结合专业评估和所选来源。

## 许可与署名

Apache-2.0 仅适用于 ELUCENIA 代码。工具、出版物、翻译和数据的权利仍归各自权利人所有。请保留 LICENSE 和 NOTICE。

ELUCENIA · Felipe Guedes · Copyright © 2026

## 已记录的结果

以下信息保留该方法对合成示例的输出，不构成独立的临床验证。

### 1

检后概率为 72.7%（LR 在 5 到 10 之间：中度增加）

| 结果详情 | |
| --- | --- |
| 检前赔率 | 0.333 |
| 检后赔率 | 2.667 |
| 绝对变化 | +47.7 个百分点 |


### 2

检后概率为 9.1%（LR ≤ 0.1：概率大幅降低）

| 结果详情 | |
| --- | --- |
| 检前赔率 | 1.000 |
| 检后赔率 | 0.100 |
| 绝对变化 | −40.9 个百分点 |


### 3

检后概率为 10.0%（LR 在 0.5 到 2 之间：该检验几乎不改变概率）

| 结果详情 | |
| --- | --- |
| 检前赔率 | 0.111 |
| 检后赔率 | 0.111 |
| 绝对变化 | +0.0 个百分点 |

