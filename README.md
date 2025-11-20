# Progetto IUM — Analisi e Pulizia dataset film (Python)

Breve descrizione
-----------------
Repository per il progetto di Interazione Uomo-Macchina: analisi, pulizia e preparazione di dataset cinematografici (movies, crew, actors, genres, ecc.) e generazione di output per visualizzazioni interattive.

Contenuto rilevante
-------------------
- Notebook di analisi e pulizia:
  - [solution/analisi.ipynb](solution/analisi.ipynb)
  - [solution/pulizia_fixed.ipynb](solution/pulizia_fixed.ipynb)
- Requisiti Python:
  - [solution/requirements.txt](solution/requirements.txt)
- Dati grezzi:
  - [data/main_data/movies.csv](data/main_data/movies.csv)
  - [data/main_data/crew.csv](data/main_data/crew.csv)
  - [data/additional_data/rotten_tomatoes_reviews.csv](data/additional_data/rotten_tomatoes_reviews.csv)
- Output prodotti:
  - [output/movies_clean.csv](output/movies_clean.csv)
  - mappe e visualizzazioni in [solution/](solution/)
- Virtual environment (opzionale): [IUM/bin/python](IUM/bin/python)

Requisiti
---------
- Python 3.10+ (o usa l'ambiente virtuale fornito in `IUM/`)
- Installare dipendenze:
```sh
pip install -r solution/requirements.txt
```

Uso
---
1. Aprire JupyterLab / Jupyter Notebook:
```sh
IUM/bin/jupyter-lab   # se si usa l'ambiente incluso
# oppure
jupyter-lab
```
2. Eseguire i notebook in ordine:
   - `solution/pulizia_fixed.ipynb` pulisce e salva i CSV in `output/` (vedi cella finale che crea `output/movies_clean.csv`).
   - `solution/analisi.ipynb` contiene esplorazioni e visualizzazioni.
3. Le mappe statiche/interattive si trovano in `solution/` (es. `top_studios_movies_by_country_map.html`).

Organizzazione del repository
----------------------------
- data/ : dati grezzi (main_data, additional_data)
- solution/ : notebook, script, mappe, requirements
- output/ : CSV risultanti dalla pulizia
- IUM/ : ambiente virtuale incluso (opzionale)

Note tecniche
------------
- Il notebook di pulizia scrive i file puliti in `output/` con:
```py
# esempio presente in pulizia_fixed.ipynb
output_dir = "output"
os.makedirs(output_dir, exist_ok=True)
df_movies_clean.to_csv(os.path.join(output_dir, "movies_clean.csv"), index=False)
```
- Controllare `solution/requirements.txt` per le versioni delle librerie utilizzate.

Autore e contatti
-----------------
- Autore: Mangini Dario (progetto IUM)
- Repository preparato per il corso/assignment di Interazione Uomo-Macchina.

Licenza
-------
Specificare qui la licenza scelta (es. MIT). Se non definita, aggiungere un file `LICENSE`.
