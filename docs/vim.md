---
layout: default
title: Vim 
---
## apertura di vim
`vim -O file1 file2 ...` permette di aprire più file e "soplittare" la visualizzazione di essi sullo stesso terminale, molto utile quando si devono apportare a due file contemporaneamente o si vuole copiare ed incollare qualcosa velocemente. Di conseguenza, `:wa` e `:qa` salverà e chiuderà tutti i file aperti in quel momento.

## Impostazioni essenziali di Vim
Per digitare un'impostazione, premere ESC e in seguito alla scrittura dell'impostazione premere ENTER(invio)

| impostazione | descrizione |
|:----------|:-------|
| `:set nu` | visualizza il numero per ogni linea |
| `:set mouse=a`| abilita l'utilizzo del mouse |
| `:syntax on`| permette la visualizzazione di alcune parole chiave del codice |

Personalmente consiglio di copiare i conteuto di [questo file](https://github.com/UmbertoSavoia/vim/blob/main/vimrc), contenente queste ed altre impostazioni molto utili, ed aggiungerlo al tuo file .vimrc situato nella cartella home.

| comandi | descrizione |
|:----------|:-------|
| `:w` | salva il file |
| `:q` | uscita |
| `:x` | salva e uscita |
| `:a` | applica il comando a tutte le tab di vim aperte |
| `:E` | esplora tra i file |
| `:Ve` | apri verticalmente una tab di esplora |

## Comandi essenziali di Vim
Per eseguire un comando, premere ESC

| comando | descrizione |
|:----------|:-------|
| `h/j/k/l` | tasti per muoversi all'interno dell'editor (sono abilitate anche le frecce) |
| `b/B/w/W`| movimento per una parola |
| `<numero della linea>G`| spostamento sulla linea indicata |
| `a/A/i/I` | entrata nella modalita' di inserzione |
| `o/O` | inserisci una nuova riga (sotto o sopra) |
| `dd` | elimina la linea corrente |
| `yy` | copia la linea corrente |
| `p/P` | incolla nella linea successiva/precedente |
| `u/ctrl+R` | torna indietro/vai avanti |
| `gg/G` | muoviti all'inzio/fine del file |
| `ctrl+u/ctrl+d` | muoviti di 25 righe piu' avanti/indietro |
