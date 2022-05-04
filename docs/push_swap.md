---
layout: default
title: push_swap
---

# push_swap

![img](../imgs/Stacks-in-C.png)

Dopo aver perso le speranze nella piena comprensione della strutturazione dell'algoritmo, ho deciso di implementare l'algoritmo in modo che rispondesse al meglio alle richieste della correzzione, senza grandi pretese, andandomi a gestire i principali casi:
- Per 3 elementi confronto in modo diretto tre numeri e poi decido le mosse per metterli nelle posizioni corrette.
- per 5 elementi, sposto i primi due elementi nello stack_b, svolgo l'ordimaneto per 3 elementi per poi reinserire nella posizione corretta i due elementi che avevo rimosso.
- per 100 numeri, vado ad ordinare lo stack per intervalli, nello specifico tre, ovvero seleziono l'intervallo di numeri più basso,
  lo metto nello stack_b e poi in base alla posizione del più grande e del più piccolo elemento che si trova in stack_b, l'algoritmo 
  sposta quello che richiede meno mose da spostare. A causa delle molte mosse di scorrimento dello stack per andare a prendere gli
  elementi di stack_a e metterli in stack_b, l'algoritmo richiede parecchie mosse, tra le 700 e le 850, non ottenendo dunque il 
  punteggio massimo.
- per 500 elementi svolgo lo stesso algoritmo per l'ordimaneto di 100 valori, andando a selezionare invece 5 intervalli. Anche in
  questo caso il numero di mosse (tra le 6500 e le 7500) non permette di prendere il punteggio massimo.

Il progetto e' stato valutato 90/100 dai tre valutatori, dato che nella pratica non ha superato i test di efficienza relativi al caso dell'ordinamento dei 100 e dei 500 numeri (per precisare, ho preso ad entrambi 4 punti su 5).

La valutazione di [Damiano](https://github.com/demian2435) è stata molto d'aiuto, perchè mi ha permesso di capire come non devessi gestire l'ordinamento con le mosse singoli, ma come il progetto fosse da impostare con le mosse doppie, perche in tal modo avrei diminuito drasticamnete il numero di mosse impiegate.

[Per seguire una pagina più approfondita e sempre in italiano, ti consiglio questa implementazione](https://github.com/sisittu99/push_swap) 
