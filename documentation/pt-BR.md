<!-- ELUCENIA technical documentation · probabilidade-pos-teste · pt-BR · no clinical/professional/rights approval -->

# Probabilidade pós-teste (teorema de Bayes)

[condições, fontes e permissões](https://elucenia.org/pt-br/ferramentas/probabilidade-pos-teste)

## Como usar

Use a ferramenta no portal ou abra index.html em um servidor HTTP local. Selecione o idioma, preencha os campos e calcule.

## Entradas e unidades

### Probabilidade pré-teste (prevalência ou estimativa clínica)

`pre`

% · intervalo: 0,1–99,9

### Razão de verossimilhança do resultado (RV+ se positivo, RV− se negativo)

`rv`

intervalo: 0,001–1000

## Edição do método

Bayes Odds:Fagan 1975; oddspré×LR, conversãopós; Deeks Altman 2004 LR

## Fórmula documentada

Chance pré-teste = p / (1 − p) · Chance pós-teste = chance pré-teste × RV · Probabilidade pós-teste = chance pós-teste / (1 + chance pós-teste).

É a forma de razão de chances do teorema de Bayes, que o nomograma de Fagan resolve graficamente.

## Limites e população

A probabilidade pré-teste deve representar a população e o contexto clínico avaliados; a razão de verossimilhança deve corresponder ao teste e à categoria do resultado. Probabilidade e odds são grandezas diferentes: a atualização multiplica odds pela razão de verossimilhança e só depois retorna à probabilidade. Valores preditivos variam com a prevalência e não se transferem automaticamente entre estudos e serviços. O cálculo atualiza uma estimativa; não confirma nem exclui sozinho uma doença.

## Referências

- [Fagan TJ. Nomogram for Bayes's theorem. N Engl J Med, 1975.](https://doi.org/10.1056/NEJM197507312930513)

- [Deeks JJ, Altman DG. Diagnostic tests 4: likelihood ratios. BMJ, 2004.](https://doi.org/10.1136/bmj.329.7458.168)

- [Deeks/Altman2004,Diagnostic tests4:likelihood ratios](https://pmc.ncbi.nlm.nih.gov/articles/PMC478236/)

- [Fagan1975](https://doi.org/10.1056/NEJM197507312930513)

## Reproduzir os testes técnicos

Execute node test.cjs na pasta raiz deste repositório para repetir os casos sintéticos registrados. As entradas, expectativas e tolerâncias originais são preservadas. Testes técnicos não constituem validação clínica.

```sh
node test.cjs
```

tool.json contém fontes, edição e escopo de revisão. examples.json conserva as entradas e expectativas sintéticas; results.json registra os resultados obtidos.

[Ficha e referências](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referência](../examples.json) · [results.json](../results.json)

## Revisão e condições de uso

Revisão clínica independente não realizada.

Esta interface é uma tradução autoral, não uma edição oficial ou certificada. Revisão clínica independente, revisão linguística profissional e autorização de direitos de instrumentos não foram realizadas.

Resultado da fórmula ou classificação. Interpretação, conduta e aplicabilidade dependem da avaliação profissional e da fonte selecionada.

## Licença e atribuição

Apache-2.0 aplica-se somente ao código da ELUCENIA. Os instrumentos, publicações, traduções e dados mantêm os direitos dos respectivos titulares. Preserve LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Resultados documentados

As informações abaixo preservam as saídas do método para exemplos sintéticos. Não constituem validação clínica independente.

### 1

Probabilidade pós-teste de 72,7% (RV entre 5 e 10: aumento moderado)

| Detalhes do resultado | |
| --- | --- |
| Chance (odds) pré-teste | 0,333 |
| Chance (odds) pós-teste | 2,667 |
| Variação absoluta | +47,7 pontos percentuais |


### 2

Probabilidade pós-teste de 9,1% (RV ≤ 0,1: grande redução da probabilidade)

| Detalhes do resultado | |
| --- | --- |
| Chance (odds) pré-teste | 1,000 |
| Chance (odds) pós-teste | 0,100 |
| Variação absoluta | −40,9 pontos percentuais |


### 3

Probabilidade pós-teste de 10,0% (RV entre 0,5 e 2: o teste quase não muda a probabilidade)

| Detalhes do resultado | |
| --- | --- |
| Chance (odds) pré-teste | 0,111 |
| Chance (odds) pós-teste | 0,111 |
| Variação absoluta | +0,0 pontos percentuais |

