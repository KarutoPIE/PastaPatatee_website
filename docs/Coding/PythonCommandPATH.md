---
tags:
    - Coding
    - Python
    - Windows
---

## Il problema
  
Nel momento in cui apri una cmd e scrivi "python" il risultato è

``` title="Command Prompt"
'python' is not recognized as an internal or external command,  
operable program or batch file.
```  
  
## La soluzione
  
Bisogna aggiungere l'eseguibile di python nella variabile PATH del tuo sistema operativo Windows  
  
1. Dall'Esplora Risorse, tasto destro su Questo PC e clicca Proprietà.
2. Nella finestra Specifiche Dispositivo, clicca su Impostazioni di sistema avanzate.
3. Nella sezione Avanzate, clicca su Variabili d'ambiente.
4. Nella sezione Variabili di sistema, trova e fai un clic sulla variabile Path e clicca poi il tasto Modifica.
5. Clicca su Nuovo ed aggiungi il percorso del tuo eseguibile di python (C:\percorso\verso\cartella\python\pythonNUMEROVERSIONE).
6. Applica i cambiamenti cliccando Ok fino a chiudere tutto. Potresti dover riavviare il sistema.
7. Riavvia la cmd e riprova. Dovrebbe funzionare.  
  
  
Link di riferimento: [stackoverflow.com/python-not-recognized-as-a-command](https://stackoverflow.com/questions/7054424/python-not-recognized-as-a-command)  