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

|         | Dataset | Model                     | Filters            | Baseline value | Predicted ROC-AUC | Ratio [%]  |
|---------|---------|---------------------------|--------------------|----------------|-------------------|------------|
| 33      | bbbp    | GradientBoostingClassifier | BrenkFilter       | 82.8296        | 2.2469            | 102.7126   |
| 56      | bbbp    | GradientBoostingClassifier | SureChEMBLFilter  | 82.8296        | 2.2348            | 102.6981   |
| 60      | bbbp    | GradientBoostingClassifier | ZINCBasicFilter   | 82.8296        | 1.9557            | 102.3612   |
| 42      | bbbp    | GradientBoostingClassifier | LipinskiFilter    | 82.8296        | 1.3795            | 101.6655   |
| 48      | bbbp    | GradientBoostingClassifier | PAINSFilter       | 82.8296        | 1.2442            | 101.5022   |

Poszczególne modele:

GaussianNB:
|         | Filters               | Baseline value | Predicted ROC-AUC | Ratio [%]  |
|---------|-----------------------|----------------|-------------------|------------|
| 80      | PfizerFilter          | 53.7001        | 14.746           | 127.4598   |
| 82      | RuleOfFourFilter      | 53.7001        | 1.243            | 102.3148   |
| 75      | MolecularWeightFilter | 53.7001        | 0.0              | 100.0      |
| 62      | BeyondRo5Filter       | 53.7001        | -0.8371          | 98.4411    |
| 72      | LINTFilter            | 53.7001        | -0.9459          | 98.2386    |

GradientBoostingClassifier:
|         | Filters            | Baseline value | Predicted ROC-AUC | Ratio [%]  |
|---------|--------------------|----------------|-------------------|------------|
| 33      | BrenkFilter        | 82.8296        | 2.2469            | 102.7126   |
| 56      | SureChEMBLFilter   | 82.8296        | 2.2348            | 102.6981   |
| 60      | ZINCBasicFilter    | 82.8296        | 1.9557            | 102.3612   |
| 42      | LipinskiFilter     | 82.8296        | 1.3795            | 101.6655   |
| 48      | PAINSFilter        | 82.8296        | 1.2442            | 101.5022   |

LogisticRegression:
|         | Filters               | Baseline value | Predicted ROC-AUC | Ratio [%]  |
|---------|-----------------------|----------------|-------------------|------------|
| 25      | SureChEMBLFilter      | 83.622         | 0.3503            | 100.4189   |
| 13      | MolecularWeightFilter | 83.622         | -0.0145           | 99.9827    |
| 9       | InpharmaticaFilter    | 83.622         | -0.0459           | 99.9451    |
| 10      | LINTFilter            | 83.622         | -0.0821           | 99.9018    |
| 0       | BeyondRo5Filter       | 83.622         | -0.2899           | 99.6533    |


Dla dwóch filtrów:

|         | Dataset | Model                     | Filters                                   | Baseline value | Predicted ROC-AUC | Ratio [%]  |
|---------|---------|---------------------------|------------------------------------------|----------------|-------------------|------------|
| 877     | bbbp    | GradientBoostingClassifier | RuleOfVeberFilter;SureChEMBLFilter       | 82.8586        | 2.596             | 103.133    |
| 892     | bbbp    | GradientBoostingClassifier | SureChEMBLFilter;ZINCBasicFilter         | 82.8586        | 2.2988            | 102.7744   |
| 828     | bbbp    | GradientBoostingClassifier | PAINSFilter;SureChEMBLFilter             | 82.8586        | 2.2771            | 102.7481   |
| 771     | bbbp    | GradientBoostingClassifier | MolecularWeightFilter;SureChEMBLFilter  | 82.8586        | 2.062             | 102.4886   |
| 832     | bbbp    | GradientBoostingClassifier | PAINSFilter;ZINCBasicFilter              | 82.8586        | 1.969             | 102.3764   |

Poszczególne modele:
GaussianNB:
|         | Filters                                   | Baseline value | Predicted ROC-AUC | Ratio [%]  |
|---------|-------------------------------------------|----------------|-------------------|------------|
| 921     | BeyondRo5Filter;PfizerFilter              | 53.7001        | 15.6314           | 129.1087   |
| 1216    | MolecularWeightFilter;PfizerFilter        | 53.7001        | 15.2908           | 128.4744   |
| 1273    | PAINSFilter;PfizerFilter                  | 53.7001        | 14.6916           | 127.3586   |
| 1232    | NIBRFilter;PfizerFilter                   | 53.7001        | 12.9207           | 124.0608   |
| 1290    | PfizerFilter;SureChEMBLFilter             | 53.7001        | 12.7491           | 123.7414   |

GradientBoostingClassifier:
|         | Filters                                   | Baseline value | Predicted ROC-AUC | Ratio [%]  |
|---------|-------------------------------------------|----------------|-------------------|------------|
| 877     | RuleOfVeberFilter;SureChEMBLFilter       | 82.8586        | 2.596             | 103.133    |
| 892     | SureChEMBLFilter;ZINCBasicFilter         | 82.8586        | 2.2988            | 102.7744   |
| 828     | PAINSFilter;SureChEMBLFilter             | 82.8586        | 2.2771            | 102.7481   |
| 771     | MolecularWeightFilter;SureChEMBLFilter  | 82.8586        | 2.062             | 102.4886   |
| 832     | PAINSFilter;ZINCBasicFilter              | 82.8586        | 1.969             | 102.3764   |

Logistic regression:
|         | Filters                                   | Baseline value | Predicted ROC-AUC | Ratio [%]  |
|---------|-------------------------------------------|----------------|-------------------|------------|
| 319     | MolecularWeightFilter;SureChEMBLFilter    | 83.622         | 0.1039            | 100.1242   |
| 376     | PAINSFilter;SureChEMBLFilter              | 83.622         | 0.0435            | 100.052    |
| 253     | LINTFilter;MolecularWeightFilter          | 83.622         | -0.0797           | 99.9047    |
| 265     | LINTFilter;SureChEMBLFilter               | 83.622         | -0.1377           | 99.8353    |
| 233     | InpharmaticaFilter;MolecularWeightFilter  | 83.622         | -0.1401           | 99.8324    |


### Zbiór BACE:

Dla jednego filtra:
|         | Dataset | Model            | Filters             | Baseline value | Predicted ROC-AUC | Ratio [%]  |
|---------|---------|------------------|---------------------|----------------|-------------------|------------|
| 17      | bace    | LogisticRegression | PAINSFilter         | 79.796         | 0.0582            | 100.0729   |
| 1       | bace    | LogisticRegression | BMSFilter           | 79.796         | 0.0089            | 100.0112   |
| 15      | bace    | LogisticRegression | NIHFilter           | 79.796         | 0.0089            | 100.0112   |
| 13      | bace    | LogisticRegression | MolecularWeightFilter| 79.796         | -0.0582           | 99.9271    |
| 0       | bace    | LogisticRegression | BeyondRo5Filter     | 79.796         | -0.2819           | 99.6468    |


Odpowiednio dla klasyfikatorów:
GaussianNB:
|         | Filters              | Baseline value | Predicted ROC-AUC | Ratio [%]  |
|---------|----------------------|----------------|-------------------|------------|
| 78      | RuleOfFourFilter     | 59.4958        | 6.9502            | 111.6818   |
| 76      | PfizerFilter         | 59.4958        | 0.3982            | 100.6692   |
| 58      | BeyondRo5Filter      | 59.4958        | 0.0               | 100.0      |
| 75      | PAINSFilter          | 59.4958        | 0.0               | 100.0      |
| 71      | MolecularWeightFilter| 59.4958        | 0.0               | 100.0      |

GradientBoostingClassifier:
|         | Filters              | Baseline value | Predicted ROC-AUC | Ratio [%]  |
|---------|----------------------|----------------|-------------------|------------|
| 31      | BrenkFilter          | 78.5053        | 0.1633            | 100.208    |
| 46      | PAINSFilter          | 78.5053        | -0.17             | 99.7834    |
| 42      | MolecularWeightFilter| 78.5053        | -0.2394           | 99.6951    |
| 29      | BeyondRo5Filter      | 78.5053        | -0.4698           | 99.4016    |
| 44      | NIHFilter            | 78.5053        | -0.5637           | 99.2819    |

LogisticRegression:
|         | Filters             | Baseline value | Predicted ROC-AUC | Ratio [%]  |
|---------|---------------------|----------------|-------------------|------------|
| 17      | PAINSFilter         | 79.796         | 0.0582            | 100.0729   |
| 1       | BMSFilter           | 79.796         | 0.0089            | 100.0112   |
| 15      | NIHFilter           | 79.796         | 0.0089            | 100.0112   |
| 13      | MolecularWeightFilter| 79.796         | -0.0582           | 99.9271    |
| 0       | BeyondRo5Filter     | 79.796         | -0.2819           | 99.6468    |


Dla dwóch filtrów:
|         | Dataset | Model            | Filters                           | Baseline value | Predicted ROC-AUC | Ratio [%]  |
|---------|---------|------------------|-----------------------------------|----------------|-------------------|------------|
| 43      | bace    | LogisticRegression | BMSFilter;PAINSFilter             | 79.796         | 0.0716            | 100.0897   |
| 313     | bace    | LogisticRegression | NIHFilter;PAINSFilter             | 79.796         | 0.0716            | 100.0897   |
| 286     | bace    | LogisticRegression | MolecularWeightFilter;PAINSFilter | 79.796         | 0.0537            | 100.0673   |
| 41      | bace    | LogisticRegression | BMSFilter;NIHFilter               | 79.796         | 0.0089            | 100.0112   |
| 284     | bace    | LogisticRegression | MolecularWeightFilter;NIHFilter   | 79.796         | -0.0895           | 99.8879    |

Dla poszczególnych klasyfikatorów:
GaussianNB:
|         | Filters                            | Baseline value | Predicted ROC-AUC | Ratio [%]  |
|---------|------------------------------------|----------------|-------------------|------------|
| 1058    | LipinskiFilter;RuleOfFourFilter   | 59.4958        | 9.4846            | 115.9416   |
| 872     | BrenkFilter;RuleOfFourFilter      | 59.4958        | 7.7577            | 113.0391   |
| 846     | BMSFilter;RuleOfFourFilter        | 59.4958        | 5.5744            | 109.3695   |
| 1116    | NIHFilter;RuleOfFourFilter        | 59.4958        | 5.5744            | 109.3695   |
| 819     | BeyondRo5Filter;RuleOfFourFilter  | 59.4958        | 5.3709            | 109.0273   |

GradientBoostingClassifier:
|         | Filters                                | Baseline value | Predicted ROC-AUC | Ratio [%]  |
|---------|----------------------------------------|----------------|-------------------|------------|
| 465     | BrenkFilter;MolecularWeightFilter     | 78.4605        | 1.1811            | 101.5053   |
| 713     | NIHFilter;PAINSFilter                 | 78.4605        | 0.3154            | 100.402    |
| 443     | BMSFilter;PAINSFilter                 | 78.4605        | 0.2528            | 100.3222   |
| 686     | MolecularWeightFilter;PAINSFilter     | 78.4605        | 0.1655            | 100.211    |
| 414     | BeyondRo5Filter;NIHFilter             | 78.4605        | -0.0089           | 99.9886    |

Logistic Regression:
|         | Filters                           | Baseline value | Predicted ROC-AUC | Ratio [%]  |
|---------|-----------------------------------|----------------|-------------------|------------|
| 43      | BMSFilter;PAINSFilter             | 79.796         | 0.0716            | 100.0897   |
| 313     | NIHFilter;PAINSFilter             | 79.796         | 0.0716            | 100.0897   |
| 286     | MolecularWeightFilter;PAINSFilter | 79.796         | 0.0537            | 100.0673   |
| 41      | BMSFilter;NIHFilter               | 79.796         | 0.0089            | 100.0112   |
| 284     | MolecularWeightFilter;NIHFilter   | 79.796         | -0.0895           | 99.8879    |


### Zbiór CLINTOX:

Dla jednego filtra:

| Filters               | Model                      | Baseline [%]  | Predicted ROC-AUC [%] | Relative Change [%] |
|-----------------------|----------------------------|---------------|-----------------------|---------------------|
| InpharmaticaFilter    | GradientBoostingClassifier | 95.5          | 96.94                 | +1.53               |
| LINTFilter            | GradientBoostingClassifier | 95.5          | 95.92                 | +0.46               |
| PfizerFilter          | GradientBoostingClassifier | 95.5          | 95.37                 | -0.13               |
| NIBRFilter            | GradientBoostingClassifier | 95.5          | 95.20                 | -0.30               |
| BeyondRo5Filter       | GradientBoostingClassifier | 95.5          | 94.53                 | -1.00               |

Dla poszczególnych klasyfikatorów:
GradientBoostingClassifier:

| Filters               | Baseline Value | Predicted ROC-AUC | Ratio [%] |
|-----------------------|---------------|-------------------|-----------|
| InpharmaticaFilter   | 95.4923       | -0.0119          | 99.9876   |
| NIBRFilter          | 95.4923       | -0.1423          | 99.8509   |
| BeyondRo5Filter     | 95.4923       | -0.3084          | 99.677    |
| SureChEMBLFilter    | 95.4923       | -0.3796          | 99.6025   |
| LINTFilter         | 95.4923       | -0.5457          | 99.4286   |

LogisticRegression:

| Filters               | Baseline Value | Predicted ROC-AUC | Ratio [%]  |
|-----------------------|---------------|-------------------|------------|
| GlaxoFilter          | 91.032        | 1.3998            | 101.5377   |
| RuleOfXuFilter       | 91.032        | -0.5694           | 99.3745    |
| MolecularWeightFilter | 91.032       | -0.7592           | 99.166     |
| SureChEMBLFilter     | 91.032        | -1.1151           | 98.7751    |
| PAINSFilter         | 91.032        | -1.8743           | 97.9411    |

GaussianNB:
| Filters                 | Baseline Value | Predicted ROC-AUC | Ratio [%]  |
|-------------------------|---------------|-------------------|------------|
| BrenkFilter            | 50.0          | 10.0              | 120.0      |
| NIBRFilter             | 50.0          | 10.0              | 120.0      |
| TiceInsecticidesFilter | 50.0          | 6.6667            | 113.3333   |
| REOSFilter             | 50.0          | 6.6667            | 113.3333   |
| LINTFilter             | 50.0          | 6.6667            | 113.3333   |


Dla dwóch filtrów:
| Dataset | Model                        | Filters                                   | Baseline Value | Predicted ROC-AUC | Ratio [%]  |
|---------|-----------------------------|-------------------------------------------|----------------|-------------------|------------|
| clintox | GradientBoostingClassifier  | GlaxoFilter; RuleOfVeberFilter          | 94.5433        | 1.3286            | 101.4053   |
| clintox | GradientBoostingClassifier  | BMSFilter; RuleOfXuFilter               | 94.5433        | 1.0913            | 101.1543   |
| clintox | GradientBoostingClassifier  | BeyondRo5Filter; RuleOfVeberFilter      | 94.5433        | 0.9964            | 101.054    |
| clintox | GradientBoostingClassifier  | InpharmaticaFilter; LINTFilter          | 94.5433        | 0.9253            | 100.9787   |
| clintox | GradientBoostingClassifier  | BeyondRo5Filter; GlaxoFilter            | 94.5433        | 0.8304            | 100.8783   |

Dla poszczególnych klasyfikatorów:
GradientBoostingClassifier:
| Filters                                | Baseline Value | Predicted ROC-AUC | Ratio [%] |
|----------------------------------------|----------------|-------------------|-----------|
| GlaxoFilter; RuleOfVeberFilter        | 94.5433        | 1.3286            | 101.4053  |
| BMSFilter; RuleOfXuFilter             | 94.5433        | 1.0913            | 101.1543  |
| BeyondRo5Filter; RuleOfVeberFilter    | 94.5433        | 0.9964            | 101.054   |
| InpharmaticaFilter; LINTFilter        | 94.5433        | 0.9253            | 100.9787  |
| BeyondRo5Filter; GlaxoFilter          | 94.5433        | 0.8304            | 100.8783  |

LogisticRegression:
| Filters                                | Baseline Value | Predicted ROC-AUC | Ratio [%] |
|----------------------------------------|----------------|-------------------|-----------|
| GlaxoFilter; PAINSFilter               | 91.032         | 0.1898            | 100.2085  |
| GlaxoFilter; SureChEMBLFilter          | 91.032         | 0.1186            | 100.1303  |
| GlaxoFilter; MolecularWeightFilter     | 91.032         | -0.3321           | 99.6351   |
| RuleOfXuFilter; SureChEMBLFilter      | 91.032         | -1.2574           | 98.6187   |
| LipinskiFilter; RuleOfXuFilter        | 91.032         | -1.5184           | 98.332    |

## Wyniki regresji:

### Zbiór ESOL:

Dla jednego filtra:
|         | Dataset | Model   | Filters                    | Baseline RMSE   | Predicted RMSE | Ratio [%]     |
|---------|---------|---------|----------------------------|-----------------|----------------|---------------|
| 109     | esol    | SGD     | RuleOfFourFilter           | 2090871350297.0676 | 13841408329.8448 | 0.6619923472516942 |
| 86      | esol    | MLP     | TiceInsecticidesFilter     | 3.2938          | 2.4575         | 74.60990308517724   |
| 78      | esol    | MLP     | REOSFilter                 | 3.2938          | 2.4696         | 74.9770198420729    |
| 87      | esol    | MLP     | ValenceDiscoveryFilter     | 3.2938          | 2.4802         | 75.29935419573019   |
| 75      | esol    | MLP     | OpreaFilter                | 3.2938          | 2.5496         | 77.40670671396882   |

Poszczególne modele:
MLP:
|         | Filters                   | Baseline RMSE | Predicted RMSE | Ratio [%]     |
|---------|---------------------------|---------------|----------------|---------------|
| 86      | TiceInsecticidesFilter     | 3.2938        | 2.4575         | 74.60990308517724   |
| 78      | REOSFilter                 | 3.2938        | 2.4696         | 74.9770198420729    |
| 87      | ValenceDiscoveryFilter     | 3.2938        | 2.4802         | 75.29935419573019   |
| 75      | OpreaFilter                | 3.2938        | 2.5496         | 77.40670671396882   |
| 64      | FAF4LeadlikeFilter         | 3.2938        | 2.614          | 79.36130325184905   |

SGD:
|         | Filters                  | Baseline RMSE   | Predicted RMSE     | Ratio [%]    |
|---------|--------------------------|-----------------|--------------------|--------------|
| 109     | RuleOfFourFilter          | 2090871350297.0676 | 13841408329.8448   | 0.6619923472516942 |
| 112     | RuleOfVeberFilter         | 2090871350297.0676 | 1690997028431.8894 | 80.87523071142733   |
| 119     | ZINCDruglikeFilter        | 2090871350297.0676 | 1719328981474.0334 | 82.23026161938436   |
| 117     | ValenceDiscoveryFilter    | 2090871350297.0676 | 1838998975107.545  | 87.9537124484614    |
| 104     | NIHFilter                 | 2090871350297.0676 | 1839889172541.5369 | 87.9962878768284    |

SVM:
|         | Filters                     | Baseline RMSE | Predicted RMSE | Ratio [%]    |
|---------|-----------------------------|---------------|----------------|--------------|
| 18      | REOSFilter                  | 2.3187        | 2.0385         | 87.91614449874835   |
| 27      | ValenceDiscoveryFilter      | 2.3187        | 2.0724         | 89.38098898794338   |
| 15      | OpreaFilter                 | 2.3187        | 2.0868         | 90.00165269422912   |
| 26      | TiceInsecticidesFilter      | 2.3187        | 2.1043         | 90.7567344722589    |
| 19      | RuleOfFourFilter            | 2.3187        | 2.1152         | 91.22359727092328   |

Dla dwóch filtrów:
|         | Dataset | Model | Filters                                | Baseline RMSE      | Predicted RMSE      | Ratio [%]    |
|---------|---------|-------|----------------------------------------|--------------------|---------------------|--------------|
| 1304    | esol    | SGD   | RuleOfTwoFilter, RuleOfXuFilter       | 1527574591.6454    | 10695400.6218       | 0.7001557030508945 |
| 1020    | esol    | SGD   | FAF4LeadlikeFilter, RuleOfTwoFilter   | 2678578336139.304  | 73806809108.568     | 2.7554471009030657 |
| 1210    | esol    | SGD   | MolecularWeightFilter, ZINCBasicFilter| 4358456165511.242  | 705306523944.1158   | 16.182485200270087 |
| 1247    | esol    | SGD   | OpreaFilter, RuleOfTwoFilter          | 50380735.5623      | 10039339.289        | 19.926940678725476 |
| 1280    | esol    | SGD   | REOSFilter, RuleOfThreeFilter         | 4362675333293.6665 | 1016946370299.6536  | 23.310154724071452 |

Poszczególne modele:
MLP:
|         | Filters                                | Baseline RMSE | Predicted RMSE | Ratio [%]    |
|---------|----------------------------------------|---------------|----------------|--------------|
| 764     | MolecularWeightFilter, ZINCBasicFilter | 1.1582        | 1.016          | 87.72056901314093 |
| 629     | GlaxoFilter, ZINCBasicFilter          | 1.1519        | 1.0169         | 88.28439323406874 |
| 730     | LipinskiFilter, ZINCBasicFilter       | 1.1626        | 1.0352         | 89.03548552570231 |
| 451     | BeyondRo5Filter, GlaxoFilter          | 1.2011        | 1.0837         | 90.22734451365557 |
| 869     | RuleOfVeberFilter, ZINCBasicFilter   | 1.158         | 1.0513         | 90.78474787155632 |

SGD:
|         | Filters                                | Baseline RMSE      | Predicted RMSE      | Ratio [%]    |
|---------|----------------------------------------|---------------------|---------------------|--------------|
| 1304    | RuleOfTwoFilter, RuleOfXuFilter       | 1527574591.6454     | 10695400.6218       | 0.7001557030508945 |
| 1020    | FAF4LeadlikeFilter, RuleOfTwoFilter   | 2678578336139.304   | 73806809108.568     | 2.7554471009030657 |
| 1210    | MolecularWeightFilter, ZINCBasicFilter| 4358456165511.242   | 705306523944.1158   | 16.182485200270087 |
| 1247    | OpreaFilter, RuleOfTwoFilter          | 50380735.5623       | 10039339.289        | 19.926940678725476 |
| 1280    | REOSFilter, RuleOfThreeFilter         | 4362675333293.6665  | 1016946370299.6536  | 23.310154724071452 |

SVM:
|         | Filters                                | Baseline RMSE      | Predicted RMSE      | Ratio [%]    |
|---------|----------------------------------------|---------------------|---------------------|--------------|
| 167     | GlaxoFilter, MolecularWeightFilter     | 1.2799              | 1.02                | 79.69570757034047 |
| 171     | GlaxoFilter, PAINSFilter               | 1.2805              | 1.0213              | 79.75787952899192 |
| 306     | MolecularWeightFilter, PAINSFilter     | 1.2709              | 1.0215              | 80.37809444768097 |
| 183     | GlaxoFilter, ZINCBasicFilter           | 1.2683              | 1.1397              | 89.86234696172998 |
| 65      | BrenkFilter, InpharmaticaFilter       | 1.4886              | 1.4184              | 95.28249695920002 |

### Zbiór LIPOPHILICITY:

Dla jednego filtra:
| Dataset | Model      | Filters             | Baseline RMSE      | Predicted RMSE      | Ratio [%]    |
|---------|------------|---------------------|---------------------|---------------------|--------------|
| 86      | lipophilicity | SGD                 | RuleOfXuFilter      | 348130841015.0978    | 281581062897.8752    | 80.88368789068694 |
| 76      | lipophilicity | SGD                 | NIBRFilter          | 348130841015.0978    | 281880434402.9831    | 80.96968185325427 |
| 63      | lipophilicity | SGD                 | BMSFilter           | 348130841015.0978    | 301807893612.5406    | 86.69381107761487 |
| 75      | lipophilicity | SGD                 | MolecularWeightFilter | 348130841015.0978    | 311381299657.7815    | 89.44375590218894 |
| 32      | lipophilicity | MLP                 | BMSFilter           | 1.0169               | 0.9362              | 92.05491741228104 |

Poszczególne zbiory:
MLP:
| Filters            | Baseline RMSE | Predicted RMSE | Ratio [%] |
|--------------------|---------------|----------------|-----------|
| BMSFilter          | 1.0169        | 0.9362         | 92.05491741228104 |
| NIHFilter          | 1.0169        | 0.9362         | 92.05491741228104 |
| BrenkFilter        | 1.0169        | 0.9437         | 92.79482229043133 |
| ZINCBasicFilter    | 1.0169        | 0.9527         | 93.68278449870652 |
| BeyondRo5Filter    | 1.0169        | 0.9611         | 94.51065532222944 |

SGD:
| Filters               | Baseline RMSE     | Predicted RMSE    | Ratio [%]         |
|-----------------------|-------------------|-------------------|-------------------|
| RuleOfXuFilter        | 348130841015.0978 | 281581062897.8752 | 80.88368789068694 |
| NIBRFilter            | 348130841015.0978 | 281880434402.9831 | 80.96968185325427 |
| BMSFilter             | 348130841015.0978 | 301807893612.5406 | 86.69381107761487 |
| MolecularWeightFilter | 348130841015.0978 | 311381299657.7815 | 89.44375590218894 |
| ZINCBasicFilter       | 348130841015.0978 | 353571156216.5    | 101.56272141403477 |

SVM:
| Filters               | Baseline RMSE     | Predicted RMSE    | Ratio [%]         |
|-----------------------|-------------------|-------------------|-------------------|
| MolecularWeightFilter | 0.8209            | 0.8226            | 100.20522244227888 |
| LipinskiFilter        | 0.8209            | 0.8229            | 100.23767176070368 |
| BeyondRo5Filter       | 0.8209            | 0.8230            | 100.25648211807685 |
| PAINSFilter           | 0.8209            | 0.8234            | 100.29358381948721 |
| ZINCBasicFilter       | 0.8209            | 0.8237            | 100.34081058763374 |

Dla dwóch filtrów:
| Dataset | Model         | Filters                               | Baseline RMSE     | Predicted RMSE    | Ratio [%]           |
|---------|---------------|---------------------------------------|-------------------|-------------------|---------------------|
| 1159    | lipophilicity | SGD                                   | PfizerFilter, RuleOfTwoFilter | 482070154095.9755 | 2.1405            | 4.4402935650318243e-10 |
| 1113    | lipophilicity | SGD                                   | NIBRFilter, ZINCBasicFilter  | 482070154095.9755 | 252457382879.1599 | 52.3694281286906 |
| 1085    | lipophilicity | SGD                                   | MolecularWeightFilter, PAINSFilter | 482070154095.9755 | 264301451210.7948 | 54.826346116871385 |
| 940     | lipophilicity | SGD                                   | GlaxoFilter, LipinskiFilter | 482070154095.9755 | 268547106469.5825 | 55.70705927090383 |
| 1128    | lipophilicity | SGD                                   | NIHFilter, ZINCBasicFilter | 482070154095.9755 | 289609737358.7494 | 60.0762637757265 |

Poszczególne klasyfikatory:
MLP:
| Filters                              | Baseline RMSE | Predicted RMSE | Ratio [%]         |
|--------------------------------------|----------------|----------------|-------------------|
| BMSFilter, MolecularWeightFilter     | 1.0169         | 0.9251         | 90.96552604714513 |
| MolecularWeightFilter, NIHFilter     | 1.0169         | 0.9251         | 90.96552604714513 |
| BMSFilter, NIHFilter                 | 1.0169         | 0.9362         | 92.05491741228104 |
| BrenkFilter, ZINCDruglikeFilter      | 1.0169         | 0.9446         | 92.88675884167577 |
| BeyondRo5Filter, NIHFilter           | 1.0169         | 0.9446         | 92.88679741110418 |

SGD:
| Filters                              | Baseline RMSE         | Predicted RMSE        | Ratio [%]          |
|--------------------------------------|-----------------------|-----------------------|--------------------|
| PfizerFilter, RuleOfTwoFilter        | 482070154095.9755     | 2.1405                | 4.4402935650318243e-10 |
| NIBRFilter, ZINCBasicFilter          | 482070154095.9755     | 252457382879.1599     | 52.3694281286906   |
| MolecularWeightFilter, PAINSFilter   | 482070154095.9755     | 264301451210.7948     | 54.826346116871385 |
| GlaxoFilter, LipinskiFilter          | 482070154095.9755     | 268547106469.5825     | 55.70705927090383  |
| NIHFilter, ZINCBasicFilter           | 482070154095.9755     | 289609737358.7494     | 60.0762637757265   |

SVM:
| Filters                              | Baseline RMSE         | Predicted RMSE        | Ratio [%]          |
|--------------------------------------|-----------------------|-----------------------|--------------------|
| LipinskiFilter, MolecularWeightFilter | 0.8209                | 0.8229                | 100.23767176070368 |
| BeyondRo5Filter, MolecularWeightFilter| 0.8209                | 0.8230                | 100.25648211807685 |
| LipinskiFilter, ZINCBasicFilter      | 0.8209                | 0.8233                | 100.29205561717404 |
| BeyondRo5Filter, LipinskiFilter      | 0.8209                | 0.8234                | 100.30129382620237 |
| GlaxoFilter, MolecularWeightFilter   | 0.8209                | 0.8237                | 100.3407537884593  |

## Kod użyty do testowania:

### Filtry i fingerprinty:
```
fingerprints = [
    ECFPFingerprint(),
    MACCSFingerprint(),
    RDKitFingerprint(),
    BeyondRo5Filter(),
]

filters = [
    BeyondRo5Filter, BMSFilter, BrenkFilter, FAF4DruglikeFilter, FAF4LeadlikeFilter, GhoseFilter, GlaxoFilter, GSKFilter,
    HaoFilter, InpharmaticaFilter, LINTFilter, LipinskiFilter, MLSMRFilter, MolecularWeightFilter, NIBRFilter, NIHFilter,
    OpreaFilter, PAINSFilter, PfizerFilter, REOSFilter, RuleOfFourFilter, RuleOfThreeFilter, RuleOfTwoFilter, RuleOfVeberFilter,
    RuleOfXuFilter, SureChEMBLFilter, TiceHerbicidesFilter, TiceInsecticidesFilter, ValenceDiscoveryFilter, ZINCBasicFilter, ZINCDruglikeFilter
]
```

### Pipelines:
```
pipelines = {
    "baseline_pipeline": make_pipeline(MolFromSmilesTransformer(), make_union(ECFPFingerprint(count=True), MACCSFingerprint()), LogisticRegression(max_iter=1000)),
    "rf_pipeline": make_pipeline(MolFromSmilesTransformer(), make_union(ECFPFingerprint(count=True), MACCSFingerprint(), RDKitFingerprint()), RandomForestClassifier(random_state=41, class_weight='balanced')),
    "gb_pipeline": make_pipeline(MolFromSmilesTransformer(), make_union(ECFPFingerprint(count=True), MACCSFingerprint(), RDKitFingerprint()), GradientBoostingClassifier()),
    "knc_pipeline": make_pipeline(MolFromSmilesTransformer(), make_union(ECFPFingerprint(count=True), MACCSFingerprint(), RDKitFingerprint()), models[1]),
    "svm_pipeline": make_pipeline(MolFromSmilesTransformer(), make_union(ECFPFingerprint(count=True), MACCSFingerprint(), RDKitFingerprint()), models[7]),
    "GNB_pipeline": make_pipeline(MolFromSmilesTransformer(), make_union(ECFPFingerprint(count=True), MACCSFingerprint(), RDKitFingerprint()), models[2]),
    "mlp_pipeline": make_pipeline(MolFromSmilesTransformer(), make_union(ECFPFingerprint(count=True), MACCSFingerprint(), RDKitFingerprint()), models[6]),
}
```

### Dla klasyfikacji:
```
filter_f = filter()
filter_f.fit(smiles_bace)
filtered_mols = filter_f.transform(smiles_bace)
filtered_labels = [ bace_mols_mapper[mol] for mol in filtered_mols ]
rest_mols = [ mol for mol in smiles_bace if mol not in filtered_mols ]
rest_labels = [ bace_mols_mapper[mol] for mol in rest_mols ]

filtered_mols_bace_train, filtered_mols_bace_test, y_train_filtered, y_test_filtered = scaffold_train_test_split(
    filtered_mols, filtered_labels, test_size=0.2
)

pipelines[pipeline_name].fit(filtered_mols_bace_train, y_train_filtered)
y_pred_filtered = pipelines[pipeline_name].predict(filtered_mols_bace_test)
y_proba_filtered = pipelines[pipeline_name].predict_proba(filtered_mols_bace_test)


r2score_filtered, accuracy_filtered, roc_auc_filtered = calculate_scores(y_test_filtered, y_pred_filtered, y_proba_filtered)

pipelines[pipeline_name].fit(filtered_mols_bace_train, y_train_filtered)
y_pred_mixed = pipelines[pipeline_name].predict(smiles_bace_test)
y_proba_mixed = pipelines[pipeline_name].predict_proba(smiles_bace_test)

r2score_mixed, accuracy_mixed, roc_auc_mixed = calculate_scores(y_test, y_pred_mixed, y_proba_mixed)

pipelines[pipeline_name].fit(filtered_mols_bace_train, y_train_filtered)
y_pred_rest = pipelines[pipeline_name].predict(rest_mols)
y_proba_rest = pipelines[pipeline_name].predict_proba(rest_mols)

r2score_rest, accuracy_rest, roc_auc_rest = calculate_scores(rest_labels, y_pred_rest, y_proba_rest)
```

```
def calculate_scores(y_test, y_pred, y_proba):
    r2score = r2_score(y_test, y_pred)

    accuracy = accuracy_score(y_test, y_pred)

    roc_auc = roc_auc_score(y_test, y_proba[:, 1])
    return r2score, accuracy, roc_auc
```


### Dla regresji:
```
filter_f = filters[0]()
filter_f.fit(smiles_esol)
filtered_mols = filter_f.transform(smiles_esol)

filter_f2 = filters[1]()
filter_f2.fit(filtered_mols)
filtered_mols = filter_f2.transform(filtered_mols)

filtered_labels = [esol_mols_mapper[mol] for mol in filtered_mols]
rest_mols = [mol for mol in smiles_esol if mol not in filtered_mols]
rest_labels = [esol_mols_mapper[mol] for mol in rest_mols]

filtered_mols_train, filtered_mols_test, y_train_filtered, y_test_filtered = scaffold_train_test_split(
    filtered_mols, filtered_labels, test_size=0.2
)

pipelines[pipeline_name].fit(filtered_mols_train, y_train_filtered)
y_pred_filtered = pipelines[pipeline_name].predict(filtered_mols_test)
filtered_rmse = np.sqrt(mean_squared_error(y_test_filtered, y_pred_filtered))

pipelines[pipeline_name].fit(filtered_mols_train, y_train_filtered)
y_pred_mixed = pipelines[pipeline_name].predict(smiles_esol_test)
mixed_rmse = np.sqrt(mean_squared_error(y_test, y_pred_mixed))

pipelines[pipeline_name].fit(filtered_mols_train, y_train_filtered)
y_pred_rest = pipelines[pipeline_name].predict(rest_mols)
rest_rmse = np.sqrt(mean_squared_error(rest_labels, y_pred_rest))

improvement_percentage = (1 - (filtered_rmse / baseline_rmse)) * 100
```

```
def calculate_scores(y_test, y_pred, y_proba):
    rmse = root_mean_squared_error(y_pred=y_pred, y_true=y_test)
    return rmse #r2score, accuracy, roc_auc
```
