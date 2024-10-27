---
tags:
    - Coding
    - Python
    - VisualStudioCode
    - Windows
---

## Il problema
  
Inizializzando una qualunque funzione di python nel terminale di Visual Studio Code, nel mio caso il comando "pip" per l'installazione del pacchetto python di [Material](https://squidfunk.github.io/mkdocs-material/getting-started/ "Material for MkDocs"), si ottiene un messaggio di errore.  
  
``` title="VSC Terminal"
'pip' is not recognized as an internal or external command,  
operable program or batch file.
```  
  
## La soluzione
  
La procedura è divisa in due parti. Prima bisogna assicurarsi di avere l'estensione installata in VSC, e poi che il programma abbia il percorso di python giusto nelle impostazioni.  
  
#### L'estensione Python
Per installare l'estensione Python in VSC, basta aprire la sezione Extentions nella barra a sinistra del programma, o con la combinazione di tasti ++ctrl+shift+x++, cercare "Python" nella barra di ricerca apposita ed installare l'estensione uffciale Microsoft.  
  
#### Aggiungere l'eseguibile nelle impostazioni
In VSC, apri le Impostazioni con ++ctrl+comma++, quindi cerca "Interpreter". Se Python è installato correttamente sul PC e l'estensione è stata già installata in VSC, dovrebbe uscire la voce "Python: Default Interpreter Path". In quella voce inserisci il percorso dove si trova l'eseguibile python.exe sul tuo PC. Potresti aver bisogno di riavviare VSC dopo questi passaggi.  
  
  
Link di riferimento: [stackoverflow.com/visual-studio-code-cant-find-python](https://stackoverflow.com/questions/65999975/visual-studio-code-cant-find-python)