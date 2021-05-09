# EvoSkeleton - Plugin per Blender

In questo repository è presente un plugin per integrare la rete [Evoskeleton](https://github.com/Nicholasli1995/EvoSkeleton). Tale rete ha lo scopo di produrre la posa 3D di una persona a partire da una foto.

Passi per la realizzazione:

- Download della rete [Evoskeleton](https://github.com/Nicholasli1995/EvoSkeleton)
- Comprensione del funzionamento e creazione di un file python personalizzato per l'inferenza. Tale file connette le due reti utilizzate in EvoSkeleton prendendo in input il path dell'immagine e restituendo in output un vettore di (16,3,2) elementi. Tale vettore contiene i bone del personaggio.
- Implementazione di un plugin che permette la scelta di un'immagine .jpg, .jpeg e .png e che restituisce un personaggio con la posa dell'immagine scelta direttante in Blender.

[Plugin](https://drive.google.com/file/d/1Sp7usYCp_LInmfmezmDeuqxX8vdYmnQD/view?usp=sharing)
