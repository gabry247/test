###########################################
sezione - Dati Invio
###########################################



.. table:: In questa sezione vengono indicati i dati identificativi della comunicazione della SAP. Campi e significato
   :name: Dati Invio

============================================================== =============================================================================================================
**data invio (marca temporale)**									Indica la data di creazione della SAP ed es. 2007-06-21T21:33:21
**data ultimo aggiornamento**									Indica la data dell’ultimo aggiornamento della SAP in formato aaaa-mm-gg
**identificativo SAP**											Indica l’identificativo univoco della SAP è composto da un codice alfanumerico formato da 2 caratteri e 9 numeri. Se l' identificativo SAP è di tipo ZZ viene controllata l' esistenza del codice in NCN. Se esiste una SAP attiva per il codice fiscale allora il codice SAP presente nella SAP inviata deve essere uguale a quello esistente in NCN. 
**codice ente titolare**											Si inserisce il codice dell’ente titolare della SAP dalla tabella di riferimento (Tabella CPI). Il codice inserito deve essere presente nella Tabella CPI e contemporaneamente valido (la data ultimo aggiornamento deve essere compresa nel range di validità del codice CPI)
**tipo variazione**												Si inserisce il tipo di variazione della SAP dalla tabella di riferimento (Tabella Tipo Variazione)
============================================================== =============================================================================================================
