# Scrittura-Tesi

Progetto di scrittura in LaTeX della mia tesi Triennale in Informatica all'Università Degli Studi di Milano.

Il progetto fa uso del package `\import` per dividere lo sviluppo in più file `.tex`. Vedere il contenuto del file `Tesi.tex` per un esempio d'uso.

## PDF/A-1b Compliance

Il PDF generato è immediatamente compliant allo standard PDF/A richiesto dall'università grazie all'uso dei pacchetti:
- `\usepackage[a-1b]{pdfx}`
- `\usepackage{hyperref}`

È importante che **pdfx venga importato prima di hyperref**.

### Specifica dei metadati con .xmpdata

Per finire è necessario creare un file `.xmpdata` con lo stesso nome del codice sorgente principale (nel mio caso quindi `Tesi.xmpdata`). Il suo scopo è definire i metadata che poi verranno inseriti nel pdf.

Un esempio è:

```
\Title        {Analisi Quantitativa e Percettiva di Video Creati con Generatori AI}

\Author       {Federico Coscia}

\Copyright    {Copyright \copyright\ 2024 "Federico Coscia"}

\Keywords     {}

\Subject      {}
```

Nel "Subject" ci sarebbe da metterci l'Abstract.

Consiglio di non mettere nulla nelle `Keywords` perché sono probabilmente non importanti, e creano problemi di validazione dello standard. (A quanto pare andrebbero ridichiarate identiche anche nel codice sorgente del .tex, codice duplicato, non è così importante alla fine)

Per una guida dettagliata su come generare direttamente file PDF/A-1b, io ho seguito [questa guida](https://www.mathstat.dal.ca/~selinger/pdfa/).

# Compilazione

Per ora non sto utilizzando strumenti come [BibTeX](https://www.bibtex.org) o [Biber](https://biblatex-biber.sourceforge.net) per la realizzazione della Bibliografia, per cui la compilazione è semplicemente fatta con `pdflatex`.

# Risorse Utili

- Per chiunque si imbatta in questo repository e vorrebbe avere un template da cui partire, lo invito a recuperare il **primo commit**.

- [Archivio dell'Università degli Studi di Milano di tutte le tesi discusse dal 01/01/2011](https://unimi.primo.exlibrisgroup.com/discovery/collectionDiscovery?vid=39UMI_INST:VU1&collectionId=81406318570006031) (da magistrale in poi)

- [Guida di LaTeX in generale](https://biccari.altervista.org/c/informatica/latex/.)

- [Download del marchio Unimi per la tesi](https://work.unimi.it/servizi/comunicare/37094.htm)

# Crediti

Il progetto è stato costruito a partire dal [template di LaTeX fornito dall'università](https://informatica.cdl.unimi.it/sites/lf1x/files/2022-04/template-tesi-informatica-corretto.zip), da cui è preso il frontespizio.