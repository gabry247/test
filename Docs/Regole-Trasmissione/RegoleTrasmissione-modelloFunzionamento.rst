###############################
Modello logico di funzionamento
###############################

Il Nodo di coordinamento, attraverso il quale viaggia la Scheda Anagrafico-Professionale, è realizzato in conformità ai principi del modello architetturale a tre livelli basato su tecnologia web, i cui principali elementi funzionali sono, dal punto di vista logico:
- un componente di interfaccia utente, costituito da un web browser,
- un componente che gestisce la comunicazione e la logica applicativa, costituito da uno (o più) web server e da uno (o più) application server,
- un componente che gestisce l’accesso ai dati e la loro memorizzazione, costituito da un RDBMS.
I componenti che gestiscono la logica applicativa e l’accesso ai dati possono essere distribuiti nei domini regionali, i quali possono scambiarsi dati e servizi senza dover modificare la propria piattaforma tecnologica interna e la loro struttura organizzativa. 
Gli utenti interagiscono con il nodo di coordinamento senza doversi preoccupare della collocazione fisica, all’interno della federazione, delle informazioni e dei servizi richiesti.
Accedendo via internet, è sufficiente un web browser per interagire con il sistema.
Il Web Server costituisce il front end comunicativo tra il browser che, attraverso protocollo HTTP o HTTPS, richiede l’avvio di una transazione applicativa e l’application server delegato all’esecuzione della transazione richiesta.
L’application server dovrà garantire servizi di accesso a protocolli di network standard quali HTTP e HTTPS e a database relazionali, a directory LDAP e  web services basati su SOAP.
Il DataBase server deve consentire l’accesso alle basi di dati attraverso interfacce applicative indipendenti dal linguaggio di query del RDBMS. 
