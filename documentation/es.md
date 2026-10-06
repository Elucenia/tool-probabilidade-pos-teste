<!-- ELUCENIA technical documentation · probabilidade-pos-teste · es · no clinical/professional/rights approval -->

# Probabilidad posterior a la prueba (teorema de Bayes)

[condiciones, fuentes y permisos](https://elucenia.org/es/herramientas/probabilidade-pos-teste)

## Cómo usar

Utilice la herramienta en el portal o abra index.html mediante un servidor HTTP local. Seleccione el idioma, complete los campos y calcule.

## Entradas y unidades

### Probabilidad preprueba (prevalencia o estimación clínica)

`pre`

% · intervalo: 0,1–99,9

### Razón de verosimilitud del resultado (RV+ si positivo, RV− si negativo)

`rv`

intervalo: 0,001–1000

## Edición del método

Odds Bayes: Fagan 1975; odds pretest×RV, conversión postest; RV Deeks–Altman 2004

## Fórmula documentada

Odds pretest = p / (1 − p) · Odds postest = Odds pretest × RV · Probabilidad postest = Odds postest / (1 + Odds postest).

Es la forma de odds del teorema de Bayes, resuelta gráficamente por el nomograma Fagan.

## Límites y población

La probabilidad preprueba debe representar la población y el contexto clínico evaluados; la razón de verosimilitud debe corresponder al test y a la categoría del resultado. Probabilidad y odds son magnitudes distintas: la actualización multiplica las odds por la razón de verosimilitud y solo después vuelve a la probabilidad. Los valores predictivos varían con la prevalencia y no se transfieren automáticamente entre estudios y servicios. El cálculo actualiza una estimación; no confirma ni descarta por sí solo una enfermedad.

## Referencias

- [Fagan TJ. Nomogram for Bayes's theorem. N Engl J Med, 1975.](https://doi.org/10.1056/NEJM197507312930513)

- [Deeks JJ, Altman DG. Diagnostic tests 4: likelihood ratios. BMJ, 2004.](https://doi.org/10.1136/bmj.329.7458.168)

- [Deeks/Altman2004,Diagnostic tests4:likelihood ratios](https://pmc.ncbi.nlm.nih.gov/articles/PMC478236/)

- [Fagan1975](https://doi.org/10.1056/NEJM197507312930513)

## Reproducir las pruebas técnicas

Ejecute node test.cjs en el directorio raíz de este repositorio para repetir los casos sintéticos registrados. Se conservan las entradas, los resultados esperados y las tolerancias originales. Las pruebas técnicas no constituyen validación clínica.

```sh
node test.cjs
```

tool.json contiene las fuentes, la edición y el alcance de la revisión. examples.json conserva las entradas y los resultados esperados de los casos sintéticos; results.json registra los resultados obtenidos.

[Ficha y referencias](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referencia](../examples.json) · [results.json](../results.json)

## Revisión y condiciones de uso

No se ha realizado una revisión clínica independiente.

Esta interfaz es una traducción de elaboración propia, no una edición oficial o certificada. No se han realizado la revisión clínica independiente, la revisión lingüística profesional ni la autorización de derechos de los instrumentos.

Resultado de la fórmula o clasificación. La interpretación, la conducta y la aplicabilidad dependen de la evaluación profesional y de la fuente seleccionada.

## Licencia y atribución

Apache-2.0 se aplica únicamente al código de ELUCENIA. Los derechos de los instrumentos, publicaciones, traducciones y datos permanecen en manos de sus respectivos titulares. Conserve LICENSE y NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Resultados documentados

La información siguiente conserva las salidas del método para ejemplos sintéticos. No constituye una validación clínica independiente.

### 1

Probabilidad posprueba de 72,7% (RV entre 5 y 10: aumento moderado)

| Detalles del resultado | |
| --- | --- |
| Odds preprueba | 0,333 |
| Odds posprueba | 2,667 |
| Variación absoluta | +47,7 puntos porcentuales |


### 2

Probabilidad posprueba de 9,1% (RV ≤ 0,1: gran reducción de la probabilidad)

| Detalles del resultado | |
| --- | --- |
| Odds preprueba | 1,000 |
| Odds posprueba | 0,100 |
| Variación absoluta | −40,9 puntos porcentuales |


### 3

Probabilidad posprueba de 10,0% (RV entre 0,5 y 2: la prueba apenas cambia la probabilidad)

| Detalles del resultado | |
| --- | --- |
| Odds preprueba | 0,111 |
| Odds posprueba | 0,111 |
| Variación absoluta | +0,0 puntos porcentuales |

