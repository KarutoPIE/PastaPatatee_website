---
tags:
    - Coding
    - Python
    - VisualStudioCode
    - Windows
---

## Il problema
  
Nel momento in cui si prova ad attivare un ambiente virtuale, nel mio caso per attivare il sito web tramite [Material](https://squidfunk.github.io/mkdocs-material/ "Material for MkDocs") con questo codice:

```python
./venv/Script/activate

```

si ottiene una stringa di errore del tipo:

```powershell
File ./venv/Script/activate cannot be loaded because running scripts  
is disabled on this system.
```  

Questo succede poiché di default nei sistemi Windows sono attivi i [Criteri di Eesecuzione di PowerShell](https://learn.microsoft.com/it-it/powershell/module/microsoft.powershell.core/about/about_execution_policies?view=powershell-7.4 "Microsoft: about_Execution_Policies"), che controllano in automatico il caricamento dei file e l'esecuzione di script nel prompt dei comandi.  
  
## La soluzione
  
Ci sono vari modi per ovviare questo problema, dal bypassarlo al cambiare determinati valori nell'Editor del Registro di sistema. Uno dei modi più rapidi è quello di disabilitare le restrizioni dell'Execution Policy per l'utente corrente direttamente dalla PowerShell. Avviando la PowerShell come amministratore, basta inserire il seguente comando e premere invio:  

```powershell
PS C:\Users> Set-Executionpolicy -Scope CurrentUser -ExecutionPolicy UnRestricted
```  
Uscirà quindi un avviso, basta cliccare "Y" per yes (o "S" per si nella versione italiana) inviando nuovamente per accettare e confermare il cambiamento.  
Riavviando VSC ora l'attivazione dell'ambiente virtuale dovrebbe avvenire senza problemi. Potrebbe essere necessario riavviare il PC.  
  
  
Link di riferimento: [netspi.com/15-ways-to-bypass-the-powershell-execution-policy](https://www.netspi.com/blog/technical-blog/network-penetration-testing/15-ways-to-bypass-the-powershell-execution-policy/) 
