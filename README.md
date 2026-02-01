# Complications of myocardial infarction 
## Descrizione del progetto

Questo progetto ha come obiettivo la predizione della mortalità post-infarto miocardico a partire da dati clinici ospedalieri.  
L’analisi è stata condotta utilizzando due modelli di classificazione lineare:la Regressione Logistica (RL) e l'Analisi Discriminante Lineare (LDA)
Particolare attenzione è stata rivolta alla classe clinicamente critica (decesso), riducendo il numero di falsi negativi, ovvero i pazienti deceduti che il modello classifica come sopravvissuti, tramite calibrazione della soglia decisionale della RL. Difatti, questo modello si è rivelato il più adeguato, in quanto consente di ridurre significativamente i FN, migliorando l'individuazione dei pazienti a rischio di decesso.

Il flusso di lavoro comprende:
- Descrizione del Dataset
- Analisi esplorativa dei dati (EDA)
- Gestione dei valori mancanti
- Preprocessing e standardizzazione
- Addestramento del primo modello: RL
- Valutazione del modello tramite, confusion matrix, metriche e curva ROC/AUC
- Addestramento del secondo modello: LDA
- Valutazione del modello tramite, confusion matrix, metriche e curva ROC/AUC
- Confronto finale dei risultati ottenuti dai due modelli

---
## Dataset utilizzato
https://figshare.le.ac.uk/articles/dataset/Myocardial_infarction_complications_Database/12045261/3

Il dataset utilizzato è il *Myocardial Infarction Complications Database*, composto da: 1700 osservazioni (pazienti) e 124 variabili cliniche.

La variabile target è stata costruita a partire da `LET_IS`. Essendo questa una variabile discreta multiclasse, è stato necessario renderla binaria dove 0 sta per sopravvivenza ed 1 per decesso. 

Inoltre, il dataset presenta uno sbilanciamento delle classi (circa 84% sopravvissuti e 16% deceduti).

---

## Librerie utilizzate

Il progetto è stato sviluppato in Python utilizzando:

- pandas per la gestione e la manipolazione dei dati
- numpy per il calcolo numerico
- matplotlib per la visualizzazione dei grafici
- seaborn per le visualizzazioni statistiche
- scikit-learn per preprocessing, modelli e metriche di valutazione; in particolare:

- LogisticRegression
- LinearDiscriminantAnalysis
- StandardScaler
- train_test_split
- confusion_matrix
- classification_report
- roc_curve, auc

---

## Requisiti

- Python 3.8 o superiore
- Jupyter Notebook oppure Google Colab

---

## Come eseguire il progetto

### 1. Avviare Jupyter Notebook:

jupyter notebook

### 2. Aprire il file notebook:

Complication_of_MI.ipynb

### 3. Dal menu selezionare:

Kernel → Restart & Run All

Oppure eseguire le celle dall’alto verso il basso.  

In alternativa il notebook può essere caricato ed eseguito su Google Colab.


