# EvoSkeleton - Plugin per Blender

In questo repository è presente un plugin per integrare la rete [Evoskeleton](https://github.com/Nicholasli1995/EvoSkeleton). Tale rete ha lo scopo di produrre la posa 3D di una persona a partire da una foto.

Passi per la realizzazione del plugin:

- Download della rete [Evoskeleton](https://github.com/Nicholasli1995/EvoSkeleton)
- Comprensione del funzionamento e creazione di un file python personalizzato per l'inferenza. Tale file connette le due reti utilizzate in EvoSkeleton prendendo in input il path dell'immagine e restituendo in output un vettore di (16,3,2) elementi. Tale vettore contiene i bones del personaggio. Inoltre, poiché abbiamo considerato che non tutti gli utenti possiedono una scheda video nVidia recente, la rete neurale è stata adattata ad utilizzare la CPU e non la GPU. Non dovendo allenare la rete, il calo di prestazioni che si ha è assolutamente trascurabile (per avere la posa bisogna aspettare al più un paio di secondi).
- Implementazione di un plugin che permette la scelta di un'immagine .jpg, .jpeg e .png e che restituisce un personaggio con la posa dell'immagine scelta direttante in Blender.

Il plugin è scaricabile al seguente [link](https://drive.google.com/file/d/1ghUTW60Ok_roYIz1LvuAmMckxMhp4pzI/view?usp=sharing)

Istruzioni per l'uso:

