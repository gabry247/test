###############################################################
Definizione e gestione degli eventi nella politica attiva
###############################################################


La sezione denominata “ultimo evento” conterrà le informazioni relative all’ultimo evento. La sezione è obbligatoria per le politiche attive con data proposta maggiore o uguale a 04-12-2017, viene garantita in questo modo la retrocompatibilità con le politiche già acquisite.


.. figure::  ../images/moduli-evento.jpg
   :align:   center
  Figura 1-Sezione Ultimo Evento
  
  L’elemento evento può assumere uno dei valori presenti nel seguente dizionario:



.. table:: Sezione Ultimo Evento
   :name: Sezione Ultimo Evento
    
====================================== ==================
Stato		   							Descrizione
====================================== ==================
Proposta (01)							
Iniziata (02)  							 In corso di erogazione
Respinta (03)  							 Prima dell'accettazione 
Rifiuto (04)   							 Dopo l’accettazione e prima dell’avvio 
Abbandono (05) 							 Dopo l'avvio e prima della conclusione 
Annullamento (prima dell’inizio) (06)
Annullamento (dopo l’inizio) (07)        Per errore materiale 
Cancellazione (08) 					     Mancanza dei requisiti 
Sospesa (09)
Terminata (10)
Rendicontata (11)
Decaduta (12)
Esonerata (13)
Trasformata (14)
Esclusione (15)
====================================== ==================



Non viene effettuato alcun controllo sulla presenza eventi ripetuti per la stessa politica.
La gestione degli eventi comporta anche una differente modalità di impostazione delle date presenti nella politica attiva (proposta, inizio e fine – i tre campi devono essere tutti obbligatoriamente compilati) per cui la valorizzazione di tali date dovrà essere coerente con la data dell’ultimo evento ricevuto. A tale proposito viene mostrata una tabella dove sono evidenziati in:
- Giallo: gli eventi che determinano il valore della data proposta;
- Arancione: gli eventi che determinano il valore della data inizio;
- Blu: gli eventi che determinano il valore della data fine:
- Bianco: nessun vincolo di valorizzazione tra la data evento e le date della politica (proposta\inizio\fine)

Ad esempio se l’ultimo evento è proposta (in giallo nella tabella) la data proposta della politica attiva dovrà assumere il valore della data ultimo evento; se l’ultimo evento è iniziata (in arancione nella tabella) la data inizio dovrà assumere il valore della data ultimo evento; se l’ultimo evento è abbandono, annullamento dopo l’inizio, cancellazione, sospesa, terminata (in blu nella tabella) la data fine dovrà assumere il valore della data ultimo evento; per gli altri eventi (in bianco nella tabella) non è previsto alcun vincolo sulla valorizzazione delle date proposta, inizio e fine.



+------------------------+-----------------------+----------------------------------+
|  Evento                |  Descrizione          | Valorizzazione Date              |
|                        |                       |                                  |
|                        |                       +---------+-----------+------------+
|                        |                       | Proposta|   Inizio  |    Fine    |
+========================+=======================+=========+===========+============+
|Proposta                |                       |    X*   |           |            |
+------------------------+-----------------------+---------+-----------+------------+
|Iniziata                |In corso di erogazione |         |     X     |            |
+------------------------+-----------------------+---------+-----------+------------+
|Respinta                |Prima dell'accettazione|         |           |            |
+------------------------+-----------------------+---------+-----------+------------+
|Abbandono               |Dopo l'avvio e prima   |         |           |     X      |
|                        |della conclusione      |         |           |            |
+------------------------+-----------------------+---------+-----------+------------+
|Annullamento            |                       |         |           |            |
|(prima dell'inizio)     |                       |         |           |            |
+------------------------+-----------------------+---------+-----------+------------+
|Annullamento            | Per errore materiale  |         |           |     X      |
|(dopo dell'inizio)      |                       |         |           |            |
+------------------------+-----------------------+---------+-----------+------------+
|Cancellazione           |Mancanza dei requisiti |         |           |     X      |
+------------------------+-----------------------+---------+-----------+------------+
|Sospesa                 |                       |         |           |     X      |
+------------------------+-----------------------+---------+-----------+------------+
|Terminata               |                       |         |           |     X      |
+------------------------+-----------------------+---------+-----------+------------+
|Rendicontata            |                       |         |           |            |
+------------------------+-----------------------+---------+-----------+------------+
|Decaduta                |                       |         |           |     X      |
+------------------------+-----------------------+---------+-----------+------------+
|Esonerata               |                       |         |           |            |
+------------------------+-----------------------+---------+-----------+------------+
|Trasformata             |                       |         |           |     X      |
+------------------------+-----------------------+---------+-----------+------------+
|Esclusione              |                       |         |           |     X      |
+------------------------+-----------------------+---------+-----------+------------+


Ricapitolando se evento uguale ad es. a:
- Terminata (blu): la data fine deve essere uguale alla data ultimo evento;
- Iniziata (arancione): la data inizio deve essere uguale alla data ultimo evento;
- Proposta (giallo): la data proposta deve essere uguale alla data ultimo evento;
- Rifiuto (bianco): nessun vincolo di valorizzazione tra le date della politica e la data evento.





*X: Il valore della data evento deve essere uguale alla data della politica corrispondente


