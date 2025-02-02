---
tags:
    - Coding
    - GitHub
---

## Il problema
  
A partire dal 30 Gennaio 2025, le GitHub Actions relative ai comandi ```actions/upload-artifact``` e ```actions/download-artifact``` non funzioneranno più nella loro versione v3. Per poter continuare a sfruttare queste funzioni sarà necessario aggiornare alla v4.  
Questo comporterà che il ```ci.yml``` consigliatoci nella precitata [guida](https://www.youtube.com/watch?v=DeZjkCtttss&ab_channel=ThomasWilde "Thomas Wilde: How to create a BEAUTIFUL documentation-blog website for FREE! | MkDocs Material") smetterà di funzionare, causando un'errore nel push delle modifiche verso github.
  
Link di riferimento: [github.blog/2024-04-16-deprecation-notice-v3-of-the-artifact-actions/](https://github.blog/changelog/2024-04-16-deprecation-notice-v3-of-the-artifact-actions/)  
  
## La soluzione
  
Risolvere questo problema è abbastanza semplice, basterà infatti apportare piccole modifiche manualmente al codice del ```ci.yml```.  
Innanzitutto, apriamo il file ```ci.yml``` e individuiamo queste righe di codice:  
```python title="ci.yml"
jobs:  
  build:  
    steps:  
      - name: Checkout repository  
        uses: actions/checkout@v3  
  
      - name: Setup Pages  
        uses: actions/configure-pages@v3  
  
      - name: Upload artifact  
        uses: actions/upload-pages-artifact@v1  
  
  deploy:  
    steps:  
      - name: Deploy to GitHub Pages  
        id: deployment  
        uses: actions/deploy-pages@v2
```  
  
Adesso modifichiamole in modo da farle risultare così:  
```python title="ci.yml"
jobs:  
  build:  
    steps:  
      - name: Checkout repository  
        uses: actions/checkout@v4  
  
      - name: Setup Pages  
        uses: actions/configure-pages@v4  
  
      - name: Upload artifact  
        uses: actions/upload-pages-artifact@v3  
  
  deploy:  
    steps:  
      - name: Deploy to GitHub Pages  
        id: deployment  
        uses: actions/deploy-pages@v4
```  
  
Salvando e provando adesso a fare push delle modifiche, queste andranno a buon fine senza nessun altro tipo di problema.