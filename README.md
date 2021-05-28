# EvoSkeleton - Plugin per Blender

In questo repository è presente un plugin per integrare la rete [Evoskeleton](https://github.com/Nicholasli1995/EvoSkeleton). Tale rete ha lo scopo di produrre la posa 3D di una persona a partire da una foto.

Passi per la realizzazione del plugin:

- Download della rete [Evoskeleton](https://github.com/Nicholasli1995/EvoSkeleton)
- Comprensione del funzionamento e creazione di un file python personalizzato per l'inferenza. Tale file connette le due reti utilizzate in EvoSkeleton prendendo in input il path dell'immagine e restituendo in output un vettore di (16,3,2) elementi. Tale vettore contiene i bones del personaggio. Inoltre, poiché abbiamo considerato che non tutti gli utenti possiedono una scheda video nVidia recente, la rete neurale è stata adattata ad utilizzare la CPU e non la GPU. Non dovendo allenare la rete, il calo di prestazioni che si ha è assolutamente trascurabile (per avere la posa bisogna aspettare al più un paio di secondi).
- Implementazione di un plugin che permette la scelta di un'immagine .jpg, .jpeg e .png e che restituisce un personaggio con la posa dell'immagine scelta direttante in Blender.

Istruzioni per l'uso:

  - Scaricare il plugin nel link in fondo alla pagina;
  - Aprire Blender (testato sulla versione 2.92 e 2.83.13 LTS) e andare in Edit - Preferences - Add-ons e installare il plugin selezionando il file .zip scaricato in precedenza;
  - A questo punto, comparirà il plugin EvoSkeleton (nella sezione Generic);
  - Il primo avvio potrebbe impiegare del tempo aggiuntivo poiché il plugin installa automaticamente le corrette dipendenze. Dal secondo uso, l'avvio del plugin è instantaneo;
  - Aprire il pannello laterale di Blender e selezionare la voce EvoSkeleton;
  - Cliccare "Seleziona immagine e ottieni scheletro 3D". Da qui, si aprirà "Blender File View" che permetterà di selezionare una immagine a scelta;
  - Modificare eventualmente il nome dei bones seguendo le corrispondenze numeriche presente in figura ![skeleton](https://github.com/alessiogatto/progettoCG-M/blob/main/skeleton.png =100x)
  - Goditi la posa.

Poiché la rete è stata progettata per funzionare esclusivamente su Linux, il plugin non permette l'uso su altri sistemi operativi. La dipendenza dalle schede video nvidia è stata rimossa.
