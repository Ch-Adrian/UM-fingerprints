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

Odpowiednio dla klasyfikatorów:

Dla dwóch filtrów:

Odpowiednio dla klasyfikatorów:



### Zbiór BACE:

Dla jednego filtra:

Odpowiednio dla klasyfikatorów:

Dla dwóch filtrów:

Odpowiednio dla klasyfikatorów:



### Zbiór CLINTOX:

Dla jednego filtra:

Odpowiednio dla klasyfikatorów:

Dla dwóch filtrów:

Odpowiednio dla klasyfikatorów:



## Wyniki regresji:

### Zbiór ESOL:

Dla jednego filtra:

Odpowiednio dla klasyfikatorów:

Dla dwóch filtrów:

Odpowiednio dla klasyfikatorów:



### Zbiór LIPOPHILICITY:

Dla jednego filtra:

Odpowiednio dla klasyfikatorów:

Dla dwóch filtrów:

Odpowiednio dla klasyfikatorów: