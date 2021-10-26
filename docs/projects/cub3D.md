---
layout: default
title: Cub3D
parent: Projects
nav_order: 1
---

# cub3d
In questo progetto viene richiesto di realizzare un gioco simile a Wolfstein 3D, di cui viene allegato nel subject un link per giocarci sul browser.

![img](../../img/wolf3d.png)

Il progetto é abbastaza complesso (rispetto ai precedenti progetti in cui veniva richiesto al massimo di ricreare funzioni di libreria), ecco che diventa fondamentale avere un'ottima visione d'insieme. Seguendo il [seguente tutorial](https://harm-smits.github.io/42docs/projects/cub3d.html) e leggendo il subject, si intuisce come deve essere strutturato il progetto:

- per prima cosa dobbiamo scrivere l'algoritmo che andrá a leggere il file .map, ne prenderá tutte le infomazioni necessarie (stabilendo se sono utilizzabili per la creazione del gioco), e infine la mappa, che anchessa dovrá essere controllata, ovvero dovrá essere circondata da muri e non avere punti di spawn di troppo o caratteri non ammessi
- successivamente dovremo creare la finestra e iniziare la visualizzazione del videogioco. L'algoritmo che ho seguito partendo dal tutorial linkato sopra é relativamente semplice: sostanzialmente, dato che abbiamo una mappa bidimensionale formata da 0, 1 e 2, l'algoritmo piú efficente e veloce é quello definito DDA (Digital Differential Analysis), che consiste nel proiettare vari raggi, necessari per creare un'ambienete tridimensionale, trovando per ognuno il muro ad essi perpendicolare e, una volta stabilita la distanza tra il giocatore ed il muro, ricavare l'altezza da disegnare del muro.
- infine gestire il movimento del giocatore all'interno del labirinto

Fondamentale per lo svolginto di questo progetto é l'utilizzo della MINILIBX, una libreria creata appositamente dalla 42 su OpenGL per permetterci di creare una finestra e andarci a lavorare sopra. Attraverso [questo link](https://harm-smits.github.io/42docs/libs/minilibx) potete accedere alla spiegazione di
alcune funzioni utili per la realizzazione di cub3d con relativi esercizi.
