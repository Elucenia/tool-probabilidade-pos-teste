<!-- ELUCENIA technical documentation · probabilidade-pos-teste · ja · no clinical/professional/rights approval -->

# 検査後確率（Bayesの定理）

[条件・出典・許諾](https://elucenia.org/ja/tools/probabilidade-pos-teste)

## 使い方

ポータルでツールを使用するか、ローカルHTTPサーバー経由でindex.htmlを開いてください。言語を選択し、項目を入力して計算してください。

## 入力項目と単位

### 検査前確率（有病率または臨床推定）

`pre`

% · 範囲: 0.1–99.9

### 結果の尤度比（陽性ならLR+、陰性ならLR−）

`rv`

範囲: 0.001–1000

## 方法の版

ベイズオッズ：Fagan 1975、検査前オッズ×LR、検査後換算、Deeks–Altman 2004 LR

## 記載された計算式

検査前オッズ = p / (1 − p) · 検査後オッズ = 検査前オッズ × 尤度比 · 検査後確率 = 検査後オッズ / (1 + 検査後オッズ).

ベイズの定理のオッズ形式であり、Faganノモグラムで図示して解きます。

## 限界・対象集団

検査前確率は評価する集団と臨床状況を反映する必要があり、尤度比は検査と結果カテゴリーに対応する必要があります。確率とオッズは異なる量です。更新ではオッズに尤度比を掛け、その後に確率へ戻します。予測値は有病率によって変わり、研究や施設の間で自動的に移用できません。計算は推定値を更新するもので、単独で疾患を確定または除外するものではありません。

## 参考文献

- [Fagan TJ. Nomogram for Bayes's theorem. N Engl J Med, 1975.](https://doi.org/10.1056/NEJM197507312930513)

- [Deeks JJ, Altman DG. Diagnostic tests 4: likelihood ratios. BMJ, 2004.](https://doi.org/10.1136/bmj.329.7458.168)

- [Deeks/Altman2004,Diagnostic tests4:likelihood ratios](https://pmc.ncbi.nlm.nih.gov/articles/PMC478236/)

- [Fagan1975](https://doi.org/10.1056/NEJM197507313930513)

## 技術テストの再現

このリポジトリのルートディレクトリでnode test.cjsを実行すると、記録された合成ケースを再実行できます。元の入力、期待結果、許容誤差は保持されています。技術テストは臨床的検証を意味しません。

```sh
node test.cjs
```

tool.jsonには出典、版、確認範囲が記録されています。examples.jsonには合成入力と期待結果が保持され、results.jsonには実際に得られた結果が記録されています。

[記録・参考文献](../tool.json) · [JavaScriptコード](../calculator.js) · [参照ケース](../examples.json) · [results.json](../results.json)

## 確認状況と使用条件

独立した臨床レビューは実施されていません。

このインターフェースは独自に作成した翻訳であり、公式版や認証済みの版ではありません。独立した臨床レビュー、専門家による言語レビュー、評価尺度等の権利許諾の確認は実施されていません。

式または分類の結果です。解釈、対応、適用可能性は専門家による評価と選択した出典に依存します。

## ライセンスと帰属表示

Apache-2.0はELUCENIAのコードにのみ適用されます。評価尺度等、出版物、翻訳、データの権利は、それぞれの権利者に帰属します。LICENSEとNOTICEを保持してください。

ELUCENIA · Felipe Guedes · Copyright © 2026
