Temat: Implementacja filtrów molekularnych\
Zespół: Adrian Chrobot, Karol Jurzec
Repozytorium: [https://github.com/Ch-Adrian/UM-fingerprints](https://github.com/Ch-Adrian/UM-fingerprints)

## Filtry:

Issue z zatwierdzonymi implementacjami:\
[https://github.com/scikit-fingerprints/scikit-fingerprints/issues/197](https://github.com/scikit-fingerprints/scikit-fingerprints/issues/197)

Filtry:\
BeyondRo5Filter
BMSFilte
BrenkFilter
FAF4DruglikeFilter
FAF4LeadlikeFilter
GhoseFilter
GlaxoFilter
GSKFilter
HaoFilter
InpharmaticaFilter
LINTFilter
LipinskiFilter
MLSMRFilter
MolecularWeightFilter
NIBRFilter
NIHFilter
OpreaFilter
PAINSFilter
PfizerFilter
REOSFilter
RuleOfFourFilter
RuleOfThreeFilter
RuleOfTwoFilter
RuleOfVeberFilter
RuleOfXuFilter
SureChEMBLFilter
TiceHerbicidesFilter
TiceInsecticidesFilter
ValenceDiscoveryFilter
ZINCBasicFilter
ZINCDruglikeFilter

<br />

## Zbiory danych:

### Esol

zbiór danych opisujący rozpuszczalność wody dla różnych mieszanin.

Kategoria: Physical Chemistry\
Typ danych: SMILES
Typ zadania: Regression
Ilość mieszanin:  1128
Metryka: RMSE

Przykładowa jego część:

| Compound ID | ESOL predicted log solubility in mols per litre | Minimum Degree | Molecular Weight | Number of H-Bond Donors | Number of Rings | Number of Rotatable Bonds | Polar Surface Area | measured log solubility in mols per litre | smiles                                                |
| :---------- | :---------------------------------------------- | :------------- | :--------------- | :---------------------- | :-------------- | :------------------------ | :----------------- | :---------------------------------------- | :---------------------------------------------------- |
| Amigdalin   | -0.974                                          | 1              | 457.432          | 7                       | 3               | 7                         | 202.32             | -0.77                                     | OCC3OC(OCC2OC(OC(C#N)c1ccccc1)C(O)C(O)C2O)C(O)C(O)C3O |
| Fenfuram    | -2.885                                          | 1              | 201.225          | 1                       | 2               | 2                         | 42.24              | -3.3                                      | Cc1occc1C(=O)Nc2ccccc2                                |
| citral      | -2.579                                          | 1              | 152.237          | 0                       | 0               | 4                         | 17.07              | -2.06                                     | CC(C)=CCCC(C)=CC(=O)                                  |
| Picene      | -6.618                                          | 2              | 278.354          | 0                       | 5               | 0                         | 0                  | -7.87                                     | c1ccc2c(c1)ccc3c2ccc4c5ccccc5ccc43                    |

Labels distribution:

<Image align="left" width="500px" src="https://files.readme.io/b2284cb5babd51c8d4a55412c01d102b67d0f0c8b5249506ccf42f5624c6ee40-esol.png" />

<Image align="center" width="500px" src="https://files.readme.io/095bf9ae678d31d596890414e4433a57e0f5e5cd32bcf9a9b958c3c5c3c293b0-esol2.png" />

Label stats: min: -11.6, max: 1.58, mean: -3.0501019503546094, std: 2.0955117304559443

### Lipophilicity

zbiór danych reprezentujący wyniki eksperymentalne współczynnika dystrybucji oktanol/woda (logD przy pH 7,4).

Kategoria: Physical Chemistry\
Typ danych: SMILES
Typ zadania: Regression
Ilość mieszanin: 4200
Metryka: RMSE

Przykładowe dane zbioru:

| CMPD\_CHEMBLID | exp   | smiles                                                         |
| :------------- | :---- | :------------------------------------------------------------- |
| CHEMBL596271   | 3.54  | Cn1c(CN2CCN(CC2)c3ccc(Cl)cc3)nc4ccccc14                        |
| CHEMBL1951080  | -1.18 | COc1cc(OC)c(cc1NC(=O)CSCC(=O)O)S(=O)(=O)N2C(C)CCc3ccccc23      |
| CHEMBL1771     | 3.69  | COC(=O)[C@@H](N1CCc2sccc2C1) c3ccccc3Cl                        |
| CHEMBL234951   | 3.37  | OC[C@H](O) CN1C(=O)C(Cc2ccccc12)NC(=O)c3cc4cc(Cl)sc4\[nH]3     |
| CHEMBL565079   | 3.1   | Cc1cccc(C[C@H](NC\(=O\)c2cc\(nn2C\)C\(C\)\(C\)C) C(=O)NCC#N)c1 |

Labels distribution:

<Image align="left" width="500px" src="https://files.readme.io/6b3ce35c68b4559a980dae73865c893e026f24ae5019a30aa3a90c5861cc1bba-lip1.png" />

<Image align="center" width="500px" src="https://files.readme.io/07fc26e0169973342a98a82d5d1a2889b00bc34220d9593fb50dfa12b25d7586-lip2.png" />

Label stats: min: -1.5, max: 4.5, mean: 2.1863357142857165, std: 1.2028604901336188

<br />

### Bace

zbiór danych reprezentuje Ilościowe (IC50) i jakościowe (znakowanie binarne) wyniki wiązania dla zestawu inhibitorów ludzkiej β-sekretazy 1 (BACE-1).

Kategoria: Biophysics\
Typ danych: SMILES
Typ zadania: Classification (binarne etykiety)
Ilość mieszanin: 1513
Metryka: ROC-AUC

Posiada bardzo dużo kolumn i z tego względu nie ma podglądu jak wygląda dokładnie.

### Bbbp

zbiór zawiera binarne etykiety penetracji (przepuszczalności) bariery krew-mózg.

Kategoria: Physiology\
Typ danych: SMILES
Typ zadania: Classification (binarne etykiety)
Ilość mieszanin: 2039
Metryka: ROC-AUC

Przykładowe dane zbioru:

| name                 | p\_np | smiles                                             |
| :------------------- | :---- | :------------------------------------------------- |
| Propanolol           | 1     | \[Cl].CC(C)NCC(O)COc1cccc2ccccc12                  |
| Terbutylchlorambucil | 1     | C(=O)(OC(C)(C)C)CCCc1ccc(cc1)N(CCCl)CCCl           |
| 40730                | 1     | c12c3c(N4CCN(C)CC4)c(F)cc1c(c(C(O)=O)cn2C(C)CO3)=O |
| 24                   | 1     | C1CCN(CC1)Cc1cccc(c1)OCCCNC(=O)C                   |

### Clintox

<br />

zbiór zawiera dane jakościowe leków zatwierdzonych przez FDA i tych, które nie przeszły badań klinicznych z powodów toksycznośc.

Kategoria: Physiology\
Typ danych: SMILES
Typ zadania: Classification (binarne etykiety)
Ilość mieszanin: 1478
Metryka: ROC-AUC

Przykładowe dane zbioru:

| smiles                                                                  | FDA\_APPROVED | CT\_TOX |
| :---------------------------------------------------------------------- | :------------ | :------ |
| \*C(=O)[C@H](CCCCNC\(=O\)OCCOC) NC(=O)OCCOC                             | 1             | 0       |
| \[C@@H]1([C@@H](\[C@@H]\(\[C@H]\(\[C@@H]\(\[C@@H]1Cl\)Cl\)Cl\)Cl) Cl)Cl | 1             | 0       |
| [C@H](\[C@@H]\(\[C@@H]\(C\(=O\)\[O-]\)O\)O) ([C@H](C\(=O\)\[O-]) O)O    | 1             | 0       |

## Wykorzystane klasyfikatory:

Klasyfikatory do obliczenia regresji liniowej:

* SVM - Support Vector Machines
* MLP - Multilayer perceptron
* SGD - Stochastic Gradient Descent
* Gradient Boosting Regressor

Klasyfikatory służące do klasyfikacji:

* GradientBoostingClassifier
* LogisticRegression
* GaussianNB

## Wyniki klasyfikacji:

### Zbiór BBBP:

Dla jednego filtra:

| Model                     | Filters               | Baseline value | Predicted ROC-AUC | Ratio [%] |
|---------------------------|-----------------------|----------------|-------------------|-----------|
| GradientBoostingClassifier| BrenkFilter          | 0.828296       | 0.850765          | 102.71    |
| GradientBoostingClassifier| SureChEMBLFilter     | 0.828296       | 0.850644          | 102.70    |
| GradientBoostingClassifier| ZINCBasicFilter      | 0.828296       | 0.847853          | 102.36    |
| GradientBoostingClassifier| LipinskiFilter       | 0.828296       | 0.842091          | 101.67    |
| GradientBoostingClassifier| PAINSFilter          | 0.828296       | 0.840738          | 101.50    |

Dla dwóch filtrów:

| Model                     | Filters                                | Baseline value | Predicted ROC-AUC | Ratio [%] |
|---------------------------|----------------------------------------|----------------|-------------------|-----------|
| GradientBoostingClassifier| RuleOfVeberFilter;SureChEMBLFilter    | 0.828586       | 0.854546          | 103.13    |
| GradientBoostingClassifier| SureChEMBLFilter;ZINCBasicFilter      | 0.828586       | 0.851574          | 102.77    |
| GradientBoostingClassifier| PAINSFilter;SureChEMBLFilter          | 0.828586       | 0.851357          | 102.75    |
| GradientBoostingClassifier| MolecularWeightFilter;SureChEMBLFilter| 0.828586       | 0.849206          | 102.49    |
| GradientBoostingClassifier| PAINSFilter;ZINCBasicFilter           | 0.828586       | 0.848276          | 102.38    |

### Zbiór BACE:

Dla jednego filtra:

| Model                     | Filters                                | Baseline value | Predicted ROC-AUC | Ratio [%] |
|---------------------------|----------------------------------------|----------------|-------------------|-----------|
| LogisticRegression        | PAINSFilter                           | 0.79796        | 0.798542          | 100.07    |
| LogisticRegression        | BMSFilter                             | 0.79796        | 0.798049          | 100.01    |
| LogisticRegression        | NIHFilter                             | 0.79796        | 0.798049          | 100.01    |
| LogisticRegression        | MolecularWeightFilter                 | 0.79796        | 0.797378          | 99.93     |
| LogisticRegression        | BeyondRo5Filter                       | 0.79796        | 0.795141          | 99.65     |

Odpowiednio dla klasyfikatorów:

Dla dwóch filtrów:

| Filters                          | Model                      | Baseline [%] | Predicted ROC-AUC [%] | Relative Change [%] |
|----------------------------------|----------------------------|---------------|------------------------|----------------------|
| BMSFilter;PAINSFilter            | LogisticRegression         | 79.796        | 79.868                | +0.089              |
| NIHFilter;PAINSFilter            | LogisticRegression         | 79.796        | 79.868                | +0.089              |
| MolecularWeightFilter;PAINSFilter| LogisticRegression         | 79.796        | 79.850                | +0.067              |
| BMSFilter;NIHFilter              | LogisticRegression         | 79.796        | 79.805                | +0.011              |
| MolecularWeightFilter;NIHFilter  | LogisticRegression         | 79.796        | 79.707                | -0.112              |

### Zbiór CLINTOX:

Dla jednego filtra:

| Filters               | Model                      | Baseline [%]  | Predicted ROC-AUC [%] | Relative Change [%] |
|-----------------------|----------------------------|---------------|-----------------------|---------------------|
| InpharmaticaFilter    | GradientBoostingClassifier | 95.5          | 96.94                 | +1.53               |
| LINTFilter            | GradientBoostingClassifier | 95.5          | 95.92                 | +0.46               |
| PfizerFilter          | GradientBoostingClassifier | 95.5          | 95.37                 | -0.13               |
| NIBRFilter            | GradientBoostingClassifier | 95.5          | 95.20                 | -0.30               |
| BeyondRo5Filter       | GradientBoostingClassifier | 95.5          | 94.53                 | -1.00               |

Dla dwóch filtrów:

---

## Wyniki regresji:

### Zbiór ESOL:

Dla jednego filtra:

| Filters                  | Baseline RMSE       | Predicted RMSE       | Ratio [%] | Model Name                |
|--------------------------|---------------------|----------------------|-----------|--------------------------|
| RuleOfFourFilter         | 2.090871e+12       | 1.384141e+10        | 0.00066   | SGD                      |
| TiceInsecticidesFilter   | 3.293757           | 2.457469            | 74.61     | MLP                      |
| REOSFilter               | 3.293757           | 2.469561            | 74.98     | MLP                      |
| ValenceDiscoveryFilter   | 3.293757           | 2.480177            | 75.30     | MLP                      |
| OpreaFilter              | 3.293757           | 2.549589            | 77.41     | MLP                      |


Dla dwóch filtrów:

| Filters                                  | Baseline RMSE       | Predicted RMSE       | Ratio [%] | Model Name                |
|------------------------------------------|---------------------|----------------------|-----------|--------------------------|
| RuleOfTwoFilter, RuleOfXuFilter          | 1.527575e+09       | 1.069540e+07        | 0.07      | SGD                      |
| FAF4LeadlikeFilter, RuleOfTwoFilter      | 2.678578e+12       | 7.380681e+10        | 2.76      | SGD                      |
| MolecularWeightFilter, ZINCBasicFilter   | 4.358456e+12       | 7.053065e+11        | 16.18     | SGD                      |
| OpreaFilter, RuleOfTwoFilter             | 5.038074e+07       | 1.003934e+07        | 19.93     | SGD                      |
| REOSFilter, RuleOfThreeFilter            | 4.362675e+12       | 1.016946e+12        | 23.31     | SGD                      |



### Zbiór LIPOPHILICITY:

Dla jednego filtra:

| Filters                  | Model Name                | Baseline RMSE   | Predicted RMSE | Ratio [%] |
|--------------------------|---------------------------|-----------------|----------------|-----------|
| RuleOfXuFilter           | SGD                       | 3.4813e+11      | 2.8158e+11     | 80.88     |
| NIBRFilter               | SGD                       | 3.4813e+11      | 2.8188e+11     | 80.97     |
| BMSFilter                | SGD                       | 3.4813e+11      | 3.0181e+11     | 86.69     |
| MolecularWeightFilter    | SGD                       | 3.4813e+11      | 3.1138e+11     | 89.44     |
| BMSFilter                | MLP                       | 1.0169          | 0.9362         | 92.05     |


Dla dwóch filtrów:

| Filters                                 | Model Name                | Baseline RMSE   | Predicted RMSE | Ratio [%] |
|-----------------------------------------|---------------------------|-----------------|----------------|-----------|
| PfizerFilter, RuleOfTwoFilter           | SGD                       | 4.8207e+11      | 2.1405e+00     | 0.00      |
| NIBRFilter, ZINCBasicFilter             | SGD                       | 4.8207e+11      | 2.5246e+11     | 52.37     |
| MolecularWeightFilter, PAINSFilter      | SGD                       | 4.8207e+11      | 2.6430e+11     | 54.83     |
| GlaxoFilter, LipinskiFilter             | SGD                       | 4.8207e+11      | 2.6855e+11     | 55.71     |
| NIHFilter, ZINCBasicFilter              | SGD                       | 4.8207e+11      | 2.8961e+11     | 60.08     |


