---
date: 2024-10-23
authors:
    - KarutoPIE
categories:
    - Documentazione
tags:
    - MkDocs
    - GitHub
    - VisualStudioCode
    - Coding
    - YouTube
    - Python
---

# Aggiornamento 1

Qui ho iniziato la creazione del sito. <!-- more --> Ho seguito [questa guida](https://www.youtube.com/watch?v=DeZjkCtttss&ab_channel=ThomasWilde "Thomas Wilde: How to create a BEAUTIFUL documentation-blog website for FREE! | MkDocs Material") su YouTube, consigliataci dal prof. Grillo, ovviamente con non pochi intoppi.  
Inizialmente né VSC né la cmd erano in grado di riconoscere i comandi di Python, problema poi risolto aggiungendo il percorso dell'eseguibile python.exe nella variabile "Path" nelle variabili nelle impostazioni di sistema avanzate.  
Così il pc riconosceva Python, ma in VSC ancora non era attiva la possibilità di utilizzarne i comandi. La prima cosa da fare è stata installare direttamente in VSC l'estensione "Python", dopodiché andare nelle impostazioni del programma e impostare la posizione di "python.exe" nell'impostazione "Python: Default Interpreter Path".  
Il problema successivo è stato che VSC non poteva attivare l'ambiente virtuale "[...] because running script is disabled on this system". I criteri di esecuzione di PowerShell sono gestiti dal sistema di norma, quindi c'è stato bisogno di bypassare questi criteri tramite PowerShell Amministratore (i dettagli possono essere trovati nella sezione "[Coding](../../Coding/BypassPowerShellExecutionPolicy.md "Visual Studio Code Issues")").  
Da qui la creazione del sito in locale filerà liscia, fino al momento di caricare il tutto su github ed attivare il sito online. Avviato il sito, noto che tutte le schede contenute all'interno di sottocartelle non riescono a caricarsi, mostrando solo le pagine principali contenute nella cartella iniziale "docs". Decido di interrompere qui la sessione, non riuscendo a risolvere il problema in alcun modo.