###############################
sezione 2 - Dati Amministrativi
###############################

Posizione nel mercato del lavoro
--------------------------------

Stato in anagrafe
~~~~~~~~~~~~~~~~~

.. table:: In questa sezione vengono indicati i dati identificativi della comunicazione della SAP. Campi e significato
   :name: Stato in anagrafe

============================================================== =============================================================================================================
**stato occupazionale**											Si inserisce lo stato occupazionale dalla tabella di riferimento (Tabella Stato in Anagrafe)
**condizione**													Si inserisce la condizione dalla tabella di riferimento (Tabella Condizione Status) il campo è obbligatorio se lo stato occupazionale è=disoccupato/inoccupato
**categoria dlg.297**											Si inserisce la categoria dlg.297 dalla tabella di riferimento (Tabella Categorie297)
**anzianità di disoccupazione (mesi)**							Si inserisce l’anzianità di disoccupazione in mesi (oggetto di analisi)
**indice profiling**												Valore dell'indice di profiling. Popolato da NCN a partire dal 04/12/2017.
**data evento**							                        Data ultimo evento. Popolato da NCN a partire dal 04/12/2017.
**data dichiarazione di disponibilità** 							Contiene la data di dichiarazione di disponibilità del soggetto proprietario della SAP in formato aaaa-mm-gg. Popolato da NCN a partire dal 04/12/2017.
============================================================== =============================================================================================================

Periodi di disoccupazione
~~~~~~~~~~~~~~~~~~~~~~~~~

.. table:: In questa sezione vengono indicati i dati identificativi della comunicazione della SAP. Campi e significato
   :name: Periodi di disoccupazione

============================================================== =============================================================================================================
**data ingresso**											    Contiene la data di ingresso nello stato di disoccupazione del soggetto proprioetario della SAP in formato aaaa-mm-gg
**tipo ingresso**												Si inserisce il tipo di ingresso dalla tabella di riferimento (Tabella Ingresso Disoccupazione)
============================================================== =============================================================================================================
   

Periodi di disoccupazione
--------------------------------


.. table:: In questa sezione vengono indicati i dati identificativi della comunicazione della SAP. Campi e significato
   :name: Periodi di disoccupazione
============================================================== =============================================================================================================
**lista**											            Si inserisce la lista dalla tabella di riferimento (Tabella Liste Speciali) il campo è condizionato alla valorizzazione del campo
**data iscrizione lista**									    Contiene la data di iscrizione alla lista del soggetto proprioetario della SAP in formato aaaamm-gg Il campo è condizionato alla valorizzazione del campo “lista”
**data termine iscrizione**									    Contiene la data di termine iscrizione alla lista del soggetto proprioetario della SAP in formato aaaamm-gg Il campo è condizionato alla valorizzazione del campo “lista” In caso di invalidità non vi è un termine se non per rapporto di lavoro
**data massimo differimento**									Contiene la data di massimo differimento del soggetto proprioetario della SAP in formato aaaamm-gg Il campo è condizionato alla valorizzazione del campo “lista” la data del massimo differimento per la mobilità è quella determinata dal calcolo del periodo massimo di permanenza in lista considerando i rapporti di lavoro che consentono la non cancellazione.
**provincia di iscrizione alla lista**							Si inserisce la provincia di iscrizione alla lista dalla tabella di riferimento (Tabella Province) Il campo è condizionato alla valorizzazione del campo “lista”
============================================================== =============================================================================================================
  


Assolvimento diritto/dovere all'istruzione
------------------------------------------

.. table:: In questa sezione vengono indicati i dati identificativi della comunicazione della SAP. Campi e significato
   :name: Assolvimento diritto/dovere all'istruzione

============================================================== =============================================================================================================
**appartenenza a particolari categorie**							Si inserisce l’appartenenza a categorie particolari dalla tabella di riferimento (Tabella Categorie Protette)
**indice isee**												    Si inserisce l’indice isee il valore ammesso è numerico (4 (2 decimali)) In fase di analisi la valorizzazione dell’indice
============================================================== =============================================================================================================
   

