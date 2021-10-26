---
layout: default
title: Cub3D
nav_order: 1
---

# cub3d
In questo progetto viene richiesto di realizzare un gioco simile a Wolfstein 3D, di cui viene allegato nel subject un link per giocarci sul browser.

![img](../../img/wolf3d.png)

Il progetto è molto articolato, ecco che diventa fondamentale avere un'ottima visione d'insieme. Seguendo il [seguente tutorial](https://harm-smits.github.io/42docs/projects/cub3d.html) e leggendo il subject, si intuisce come deve essere strutturato il progetto:

- per prima cosa dobbiamo scrivere l'algoritmo che andrá a leggere il file .map, salverà tutte le informazioni relative alle specifiche di gioco su variabili (strutture) e la mappa, per poi essere controllati e nel caso di errori, riportarli. Fai attenzione che la mappa sia circondata da muri e che non ci siano buchi, in tal caso il programma andrebbe in SEGFAULT.
- successivamente dovremo creare la finestra e iniziare la visualizzazione della mappa in 3D. L'algoritmo che ho seguito partendo dal tutorial linkato sopra è relativamente semplice: sostanzialmente, dato che abbiamo una mappa bidimensionale formata da 0, 1 e 2, l'algoritmo piú efficente e veloce é quello definito DDA (Digital Differential Analysis), che consiste nel proiettare vari raggi dal punto in cui ci troviamo per 66°, necessari per creare un'ambienete tridimensionale simile a ciò che vede l'occhio umano, calcolando per ognuno la distanza tra noi ed il muro perpendicolare, per ottenere poi l'altezza del muro.
- infine gestire il movimento del giocatore all'interno del labirinto

Fondamentale per lo svolginto di questo progetto é l'utilizzo della MINILIBX, una libreria creata appositamente dalla 42 su OpenGL per permetterci di creare una finestra e andarci a lavorare sopra. Attraverso [questo link](https://harm-smits.github.io/42docs/libs/minilibx) potete accedere alla spiegazione di
alcune funzioni utili per la realizzazione di cub3d con relativi esercizi.
