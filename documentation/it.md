<!-- ELUCENIA technical documentation · probabilidade-pos-teste · it · no clinical/professional/rights approval -->

# Probabilità post-test (teorema di Bayes)

[condizioni, fonti e autorizzazioni](https://elucenia.org/it/strumenti/probabilidade-pos-teste)

## Come usare

Usi lo strumento nel portale oppure apra index.html tramite un server HTTP locale. Selezioni la lingua, compili i campi ed esegua il calcolo.

## Dati di ingresso e unità

### Probabilità pretest (prevalenza o stima clinica)

`pre`

% · intervallo: 0,1–99,9

### Rapporto di verosimiglianza del risultato (LR+ se positivo, LR− se negativo)

`rv`

intervallo: 0,001–1000

## Edizione del metodo

Odds Bayes: Fagan 1975; odds pre-test×RV, conversione post-test; RV Deeks–Altman 2004

## Formula documentata

Odds pre-test = p / (1 − p) · Odds post-test = Odds pre-test × RV · Probabilità post-test = Odds post-test / (1 + Odds post-test).

È la forma in odds del teorema di Bayes, risolta graficamente dal nomogramma Fagan.

## Limiti e popolazione

La probabilità pre-test deve rappresentare la popolazione e il contesto clinico valutati; il rapporto di verosimiglianza deve corrispondere al test e alla categoria del risultato. Probabilità e odds sono grandezze diverse: l’aggiornamento moltiplica le odds per il rapporto di verosimiglianza e solo dopo ritorna alla probabilità. I valori predittivi variano con la prevalenza e non si trasferiscono automaticamente tra studi e servizi. Il calcolo aggiorna una stima; non conferma né esclude da solo una malattia.

## Riferimenti

- [Fagan TJ. Nomogram for Bayes's theorem. N Engl J Med, 1975.](https://doi.org/10.1056/NEJM197507312930513)

- [Deeks JJ, Altman DG. Diagnostic tests 4: likelihood ratios. BMJ, 2004.](https://doi.org/10.1136/bmj.329.7458.168)

- [Deeks/Altman2004,Diagnostic tests4:likelihood ratios](https://pmc.ncbi.nlm.nih.gov/articles/PMC478236/)

- [Fagan1975](https://doi.org/10.1056/NEJM197507313930513)

## Riprodurre i test tecnici

Esegua node test.cjs nella cartella principale di questo repository per ripetere i casi sintetici registrati. Gli input, i risultati attesi e le tolleranze originali sono conservati. I test tecnici non costituiscono validazione clinica.

```sh
node test.cjs
```

tool.json contiene le fonti, l’edizione e l’ambito della revisione. examples.json conserva gli input e i risultati attesi dei casi sintetici; results.json registra i risultati ottenuti.

[Scheda e riferimenti](../tool.json) · [Codice JavaScript](../calculator.js) · [Casi di riferimento](../examples.json) · [results.json](../results.json)

## Revisione e condizioni d’uso

Non è stata effettuata una revisione clinica indipendente.

Questa interfaccia è una traduzione realizzata dagli autori, non un’edizione ufficiale o certificata. Non sono state eseguite la revisione clinica indipendente, la revisione linguistica professionale né la verifica delle autorizzazioni relative ai diritti sugli strumenti.

Risultato della formula o classificazione. Interpretazione, condotta e applicabilità dipendono dalla valutazione professionale e dalla fonte selezionata.

## Licenza e attribuzione

Apache-2.0 si applica solo al codice di ELUCENIA. I diritti su strumenti, pubblicazioni, traduzioni e dati restano ai rispettivi titolari. Conservi LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Risultati documentati

Le informazioni seguenti conservano gli output del metodo per esempi sintetici. Non costituiscono una validazione clinica indipendente.

### 1

Probabilità post-test di 72,7% (LR tra 5 e 10: aumento moderato)

| Dettagli del risultato | |
| --- | --- |
| Odds pre-test | 0,333 |
| Odds post-test | 2,667 |
| Variazione assoluta | +47,7 punti percentuali |


### 2

Probabilità post-test di 9,1% (LR ≤ 0,1: grande riduzione della probabilità)

| Dettagli del risultato | |
| --- | --- |
| Odds pre-test | 1,000 |
| Odds post-test | 0,100 |
| Variazione assoluta | −40,9 punti percentuali |


### 3

Probabilità post-test di 10,0% (LR tra 0,5 e 2: il test quasi non modifica la probabilità)

| Dettagli del risultato | |
| --- | --- |
| Odds pre-test | 0,111 |
| Odds post-test | 0,111 |
| Variazione assoluta | +0,0 punti percentuali |

