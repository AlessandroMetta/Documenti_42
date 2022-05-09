---
layout: default
title: Inception
---

# Inception
Questo progetto tratta la creazione di un'applicazione con container, ad ognuno dei quali viene assegnato un servizio, infine vengono costruiti tramite docker-compose.

### Docker
La teconologia su cui si basa tutto è docker, che si occupa di creare dei container. Questi si possono immaginare come macchine virtuali senza kernel, dal momento che viene usato quello del sistema operativo della macchina ospitante, nei quali vengono eseguiti i singoli processi(programmi), ecco perchè ad ogni container viene assegnato un solo servizio.
Dal momento che tutti i servizi sono indipendenti dagli altri, se un servizio crolla, o in caso di forte incremento delle richieste e di sovraccarico di uno o più servizi, ne verranno creati automaticamente aggiuntivi.
Per orchestrare più container si usa docker-compose.

Detto ciò, perchè non usare una macchina virtuale, dal momento che è molto più diffusa?
| MV | container |
| --- | --- |
| pessima gestione delle risorse: indipendentemente dal numero delle richieste, alla macchina dovremo allocare un certo numero di risorse, e quando queste non sono sufficienti, la macchina si può interrompere. | ottima gestione delle risorse: altamente scalabile, in caso di incremento di risore o di crash, automaticamente si creano nuovi containers |
| tempo di avviamento molto lento | tempo di avviamento immediato |

Si potrebbe pensare che allora la teconologia docker sia migliore come virtualizzazione, ma in quanto sicurezza non è eguagliabile alle macchine virtuali, ecco che spesso si usano uno sull'altro.

### docker images
I container vengono costruiti a partire da dei templete, chiamati images, di cui eseguiamo delle istanze che vengono integrate con implementazioni che seguono le nostre necessità.
I Dockerfile sono file in cui vengono specificate queste implementazioni. Vediamo un po di sintassi

| keyword | significato |
| --- | --- |
| `FROM <images>` | viene specificato l'immagine da cui verrà costruita l'istanza. L'immagine viene prima cercata in locale, altrimenti viene scaricata da un repository, tipo Dockerhub |
| `WORKDIR <cartella>` | specifica che tutto ciò che avverrà in seguito (comandi) sarà fatto nella cartella specificata |
| `ADD <filesystem>` | specifica quale filesystem deve unire in fase di costtruzione |
| `CP <file/cartella> <folder>` | permette la copia di file o cartelle sul container |
| `RUN <comando>` | esegue i comandi nel container in fase di costruzione |
| `EXPOSE <porta>` | per scopo illustrativo, mostra quale porta il container usa per comunicare con l'esterno |
| `CMD <comando>`  | specifica il comando che verrà eseguito dal container al momento del lancio |
  
### docker network
permette la creazione di reti per connettere i container. 

I comandi principali sono:
- `docker network create <network_name>`: crea una nuova rete 
- `docker network list`: mostra le reti attive
- `docker network inspect <network_name/network_ID>`: mostra la subnet del network specificato e i container a lui connessi.
  
Ecco alcuni comandi base di docker:
- `docker run <image_name>`: crea un container a partire dall'immagine specificata
- `docker run --net=<network_name> <image_name>`: crea un container a partire dall'immagine specificata connettendola alla rete specificata
- `docker exec -it <container_name/ID> <command>`: esegue il comando all'interno del container, indirizzando lóutput sul terminale
  
### Volumi
Grazie a loro possiamo fare in modo di salvare dei dati sulla macchina ospitante e, indipendentemente da quanti container li usino o se qualcuno di essi viene terminato, non perderli.
  
`docker run -d -v <cartella> <immagine>`: ci permette di creare un container connesso ad un volume.
  
[fonte](https://www.freecodecamp.org/news/comprehensive-introductory-guide-to-docker-vms-and-containers-4e42a13ee103/)
