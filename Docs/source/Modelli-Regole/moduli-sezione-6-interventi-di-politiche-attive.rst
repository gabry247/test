###########################################
sezione 6 - Interventi di Politiche Attive
###########################################

Dati generali politica attiva
-----------------------------


.. table:: In questa sezione vengono indicati i dati identificativi della comunicazione della SAP. Campi e significato
   :name: Dati generali politica attiva

============================================================== =============================================================================================================
**Attività**														Tabella Tipo_attività. Se la data proposta della politica attiva è >= 09/12/2015 e il TipoAttività non è abilitato alla GG il TipoProgetto può essere solo 01-Progetto di Politica Attiva Regionale\Provinciale
**Denominazione**												obbligatorio se tipo_attività = C. Se il TipoAttivita è H01,H02,H03 (politica nazionale impostata da Centro) la denominazione è valorizzata con un codice CO Incentivata
**Data Proposta**												Data Proposta della politica attiva. La data proposta dell’ attività deve essere minore o uguale della data fine validità (se valorizzata) indicata nella tabella Tipo_attività 
**Data Inizio**													Il campo deve essere obbligatoriamente valorizzato se la data proposta è >= 09/12/2015 oppure se la data fine è valorizzata.Se valorizzata, la data inizio deve essere >= della data proposta e <= della data fine (se valorizzata).
**Data fine**													Obbligatoria se data inizio è valorizzata e il tipo_attività = C, D, E oppure se la data proposta della politica attiva è >= 09/12/2015
**Durata**														Es: ore del corso di formazione, mesi del tirocinio, ecc. Il campo è obbligatorio se il campo Tipologia durata è valorizzato. Se valorizzato può assumere solo valori positivi
**Data fine**													Tabella Tipologia_Durata. Identifica la tipologia della durata della Politica Attiva erogata. Il campo è obbligatorio se il campo durata è valorizzato.
**Tipologia Durata**												Si inserisce il tipo di variazione della SAP dalla tabella di riferimento (Tabella Tipo Variazione)
**Descrizione**												    Testo libero di descrizione della politica attiva. Nel caso di politiche attive con tipo_attività D01, E01, E02, E03, H01, H02, H03 (politica nazionale impostata da Centro) deve essere valorizzata obbligatoriamente con il solo Codice Fiscale o P.Iva del datore di lavoro che eroga la politica attiva e che permetterà il futuro aggancio con la Comunicazione Obbligatoria. Per il tipo attività C06 il campo descrizione resta obbligatorio, viene eliminato il controllo di validità del codice fiscale \ P.IVA.
**Titolo Progetto**												Tabella Tipo Progetti. Il tipo progetto 04-GG POLITICHE NAZIONALI può essere utilizzato solo da enti promotori nazionali “ST - Operatori Abilitati GG” codRegione=00-NAZIONALE
**Codice Ente Promotore**										Tabella CPI / Operatori abilitati GG. Se il tipo progetto è nazionale l'ente promotore\erogatore deve essere nazionale. La data proposta della politica attiva deve essere compresa nel range di validità del codice ente per il tipo progetto. Il tipo progetto 04-GG POLITICHE NAZIONALI può essere utilizzato solo da enti promotori nazionali “ST - Operatori Abilitati GG” codRegione=00-NAZIONALE
**Data fine**													Obbligatoria se data inizio è valorizzata e il tipo attività = C, D, E oppure se la data proposta della politica attiva è >= 09/12/2015
**Identificativo Politica**										Identificativo della Politica Attiva. Obbligatorio per politiche con data proposta >= 04-12-2017.
**Indice Profiling**												Indice di Profiling associato alla Politica
**Identificativo Presa in Carico**								Valorizzato con l’identificativo della presa in carico di riferimento
============================================================== =============================================================================================================


Ultimo Evento (0..1)
-----------------------------


.. table:: In questa sezione vengono indicati i dati identificativi della comunicazione della SAP. Campi e significato
   :name: Ultimo Evento

============================================================== =============================================================================================================
**Evento**														Obbligatorio per politiche con data proposta >= 04-12-2017, per politiche con data proposta antecedenti è condizionato dall'esistenza della sezione 6.1.2 - Ultimo evento. Popolato dalla Tabella Eventi Politica Attiva.
**Data Evento**												    Obbligatorio per politiche con data proposta >= 04-12-2017, per politiche con data proposta antecedenti è condizionato dall'esistenza della sezione 6.1.2 - Ultimo evento.
**Descrizione evento**											Eventuale descrizione
============================================================== =============================================================================================================



