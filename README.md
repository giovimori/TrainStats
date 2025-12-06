# 🚄 TrainStats - Analisi e Previsione dei Ritardi Ferroviari

## 📋 Descrizione del Progetto

Questo progetto di **Big Data Analytics** analizza le performance della rete ferroviaria italiana nel mese di **Novembre 2025**, utilizzando dati reali granulari estratti dalla piattaforma TrainStats.

L'obiettivo è duplice:
1.  **Analisi Esplorativa (EDA):** Identificare i "colli di bottiglia" della rete, le tratte più critiche e i pattern temporali dei disservizi.
2.  **Modellazione Predittiva (Machine Learning):** Sviluppare modelli per prevedere il ritardo all'arrivo e classificare la gravità del disservizio, sfidando la natura caotica e dinamica del traffico ferroviario.

## 📂 Il Dataset

Il dataset copre il traffico nazionale dal **01/11/2025** al **30/11/2025**.
* **Volume:** ~250.000 corse monitorate.
* **Granularità:** Dati per singolo treno (non aggregati).
* **Scope:** Sono stati filtrati i treni internazionali e i convogli tecnici/merci per focalizzare l'analisi sull'esperienza passeggeri domestica.

## ⚙️ Pipeline di Analisi

Il progetto segue una pipeline di Data Science strutturata:

### 1. Data Cleaning & Feature Engineering
* Rimozione outlier e treni esteri.
* Gestione valori nulli nei campi testuali (`Provvedimenti`).
* Creazione feature calcolate: `Ritardo_Tratta` (accumulo in viaggio) e `Fascia_Ritardo` (discretizzazione del target).

### 2. Key Insights (EDA)
* **Il "Paradosso dei Regionali":** L'analisi ha rivelato che, sebbene i treni Regionali siano numericamente preponderanti, mantengono un ritardo medio nettamente inferiore rispetto alle Frecce/Eurocity, che accumulano più ritardo sulle lunghe percorrenze.
* **Hotspots:** Identificate le stazioni di partenza e le fasce orarie (07:00 e 17:00) più critiche per la puntualità.

### 3. Machine Learning
Sono stati testati due approcci con `Scikit-Learn`:

* **Regressione Lineare Multipla:**
    * *Obiettivo:* Predire il minuto esatto di ritardo.
    * *Risultato ($R^2 \approx 0.15$):* Evidenzia che l'85% del ritardo è causato da fattori dinamici in itinere (guasti, traffico) non prevedibili alla partenza.

* **Classificazione (Random Forest):**
    * *Obiettivo:* Prevedere la fascia di rischio (Puntuale, Lieve, Grave, ecc.).
    * *Risultato (Accuracy $\approx 56\%$):* Performance superiore al modello casuale, con ottima capacità di identificare i treni sicuramente puntuali.

## 🚀 Come Eseguire il Progetto

1.  Clona la repository o scarica la cartella.
2.  Installa le dipendenze:
    ```bash
    pip install -r requirements.txt
    ```
3.  Apri il Jupyter Notebook:
    ```bash
    jupyter notebook train_stats.ipynb
    ```

## 🛠️ Tecnologie Utilizzate

* **Linguaggio:** Python
* **Analisi Dati:** Pandas, NumPy
* **Visualizzazione:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn

## 👨‍💻 Autore

**Giovanni Morelli**
Corso di *Laboratorio di Big Data, Data Mining e Data Analytics*
CdL Tecnologie dei Sistemi Informatici | AA 2025-2026
