# TrainStats - Analisi e Previsione dei Ritardi Ferroviari

## Descrizione del Progetto

Questo progetto di **Laboratorio di Big Data, Data Mining e Data Analytics** analizza le performance della rete ferroviaria italiana nel mese di **Novembre 2025**, utilizzando dati reali granulari estratti dalla piattaforma TrainStats.

## Dataset

Il dataset copre il traffico nazionale dal 01/11/2025 al 30/11/2025.

- Volume: ~250.000 corse monitorate.
- Granularità: Dati per singolo treno (non aggregati).
- Scope: Sono stati filtrati i treni internazionali e i convogli tecnici/merci per focalizzare l'analisi sull'esperienza passeggeri.

## Come Eseguire il Progetto

1.  Clona la repository o scarica la cartella.
2.  Installa le dipendenze:
    ```bash
    pip install -r requirements.txt
    ```
3.  Apri il Jupyter Notebook:
    ```bash
    jupyter notebook train_stats.ipynb
    ```

## Tecnologie Utilizzate

* **Linguaggio:** Python
* **Analisi Dati:** Pandas, NumPy
* **Visualizzazione:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn

## Autore

**Giovanni Morelli**
Corso di *Laboratorio di Big Data, Data Mining e Data Analytics*
CdL Tecnologie dei Sistemi Informatici | AA 2025-2026

Fonte dati: [trainstats.com](https://trainstats.altervista.org/)
