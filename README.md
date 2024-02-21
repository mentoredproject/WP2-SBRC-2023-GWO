Code related to the research associated to feature selection using Grey Wolf Optimizer (GWO):

- Paper published at http://dx.doi.org/10.5753/sbrc.2023.425 (SALVADOR, H. G. ; BATISTA, D. M. ; SANTOS, A. L. ; LIMA, M. N. . Detecção Eficiente de Anomalias em Redes de Data Centers Apoiada por Aprendizado de Máquina e Otimizador do Lobo Cinzento para Seleção de Atributos. In: Anais do XLI Simpósio Brasileiro de Redes de Computadores e Sistemas Distribuídos (SBRC), 2023.)

Here we present a solution to detect anomalies on Data Centers networks, using the Grey Wolf Optimizer (GWO) [1] to select features and Machine Learning (ML) algorithms to create models that use less features as possible and reach considerable accuracy. We compare results with a solution without features selection.

This code is the implementation of the solution reported at the paper "Detecção Eficiente de Anomalias em Redes de Data Centers Apoiada por Aprendizado de Máquina e Otimizador do Lobo Cinzento para Seleção de Atributos" published at SBRC 2023.

## Features

    Creates detection models using ML algorithms with less features as possible, with features selection;
    Reduces the number of features to generate models without a significant impact on model accuracy, using GWO.
    Improve the utilization of the network resources because fewer data need to be transferred to be classified
    Improve the utilization of the processing resources because fewer features need to be analyzed .

## How to run

To run this code, first you must download the following datasets:

    KDDCup99: file 'kddcup.data_10_percent.gz', following this link: 'https://kdd.ics.uci.edu/databases/kddcup99/kddcup99.html'. This file contents 10% of total flows from the entire dataset and we use that to run our experiments.
    UNSW-NB15: file 'UNSW_NB15_training-set.csv', following this link: 'https://research.unsw.edu.au/projects/unsw-nb15-dataset' . Containing 175,341 records in total.

Save then on your Google Drive, after that, you need to set it on the proper place, signalized as '#Load the data" in the functions 'load_KDD99()' and 'load_UNSW_NB15()', respectively.

After to set the dataset, this code runs an experiment without feature selection, the Gray Wolf Optimizer (GWO), as a comparing reference. Followed by an experiment using GWO to select features and the accuracy to compose the fitness function. And at the end, the experiment using GWO to select features and the F1-Score as parameter of the GWO fitness function.

## Contact

Henrique Salvador (PhD Student)

e-mail: henriquesalvador@ime.usp.br

## Reference

[1] Seyedali Mirjalili, Seyed Mohammad Mirjalili, Andrew Lewis. Grey Wolf Optimizer. Advances in Engineering Software. Volume 69, 2014, Pages 46-61, ISSN 0965-9978.(https://doi.org/10.1016/j.advengsoft.2013.12.007)
