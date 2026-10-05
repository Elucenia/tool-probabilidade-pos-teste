<!-- ELUCENIA technical documentation · probabilidade-pos-teste · fr · no clinical/professional/rights approval -->

# Probabilité post-test (théorème de Bayes)

[conditions, sources et autorisations](https://elucenia.org/fr/outils/probabilidade-pos-teste)

## Mode d’emploi

Utilisez l’outil sur le portail ou ouvrez index.html via un serveur HTTP local. Sélectionnez la langue, remplissez les champs et lancez le calcul.

## Données d’entrée et unités

### Probabilité prétest (prévalence ou estimation clinique)

`pre`

% · intervalle: 0,1–99,9

### Rapport de vraisemblance du résultat (RV+ si positif, RV− si négatif)

`rv`

intervalle: 0,001–1000

## Édition de la méthode

Cotes Bayes : Fagan 1975 ; prétest×RV, conversion post-test ; RV Deeks–Altman 2004

## Formule documentée

Cote prétest = p / (1 − p) · Cote post-test = Cote prétest × RV · Probabilité post-test = Cote post-test / (1 + Cote post-test).

C’est la forme en cotes du théorème de Bayes, résolue graphiquement par le nomogramme Fagan.

## Limites et population

La probabilité prétest doit représenter la population et le contexte clinique évalués ; le rapport de vraisemblance doit correspondre au test et à la catégorie du résultat. Probabilité et cote sont des grandeurs différentes : la mise à jour multiplie la cote par le rapport de vraisemblance, puis revient à la probabilité. Les valeurs prédictives varient avec la prévalence et ne se transposent pas automatiquement entre études et services. Le calcul actualise une estimation ; il ne confirme ni n’exclut une maladie à lui seul.

## Références

- [Fagan TJ. Nomogram for Bayes's theorem. N Engl J Med, 1975.](https://doi.org/10.1056/NEJM197507312930513)

- [Deeks JJ, Altman DG. Diagnostic tests 4: likelihood ratios. BMJ, 2004.](https://doi.org/10.1136/bmj.329.7458.168)

- [Deeks/Altman2004,Diagnostic tests4:likelihood ratios](https://pmc.ncbi.nlm.nih.gov/articles/PMC478236/)

- [Fagan1975](https://doi.org/10.1056/NEJM197507313930513)

## Reproduire les tests techniques

Exécutez node test.cjs dans le répertoire racine de ce dépôt pour reproduire les cas synthétiques enregistrés. Les données d’entrée, les résultats attendus et les tolérances d’origine sont conservés. Les tests techniques ne constituent pas une validation clinique.

```sh
node test.cjs
```

tool.json contient les sources, l’édition et le périmètre de la revue. examples.json conserve les données d’entrée et les résultats attendus des cas synthétiques ; results.json consigne les résultats obtenus.

[Fiche et références](../tool.json) · [Code JavaScript](../calculator.js) · [Cas de référence](../examples.json) · [results.json](../results.json)

## Revue et conditions d’utilisation

Aucune révision clinique indépendante n’a été effectuée.

Cette interface est une traduction réalisée par nos soins, et non une édition officielle ou certifiée. La revue clinique indépendante, la révision linguistique professionnelle et l’autorisation des droits sur les instruments n’ont pas été réalisées.

Résultat de la formule ou de la classification. L’interprétation, la conduite et l’applicabilité dépendent de l’évaluation professionnelle et de la source sélectionnée.

## Licence et attribution

Apache-2.0 s’applique uniquement au code d’ELUCENIA. Les droits sur les instruments, publications, traductions et données restent ceux de leurs titulaires respectifs. Conservez LICENSE et NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
