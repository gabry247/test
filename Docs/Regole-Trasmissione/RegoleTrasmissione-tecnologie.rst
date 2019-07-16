##########
Tecnologie
##########


Le tecnologie adottate sono: quella basata su Web Services sincroni e quella basata sullo scambio di messaggi (Publish & Subscribe) mediato da Web Services. (Non si esclude tuttavia l’impiego di tecnologie FTP nel caso in cui considerazioni di carattere dimensionale ne facciano emergere la necessità). A supporto del scambio di messaggi in modalità Publish & Subscribe, è previsto che SPCoop metta a disposizione un servizio di gateway applicativo.

Web Services
-------------------------
Gli standard utilizzati per l’utilizzo del modello Web services sono:
- uso del linguaggio XML per la rappresentazione dei dati;
- uso del protocollo SOAP per  il formato dei messaggi scambiati tra i domini; 
- uso del linguaggio WSDL per la definizione delle chiamate ai Web Services;
- uso del sistema UDDI per catalogare i servizi disponibili e le relative interfacce/contratti per la loro invocazione.
L’architettura basata su Web Services prevede l’interazione fra tre distinti ruoli: il Fornitore dei Servizi, il Registro dei Servizi e il Richiedente. Le operazioni a supporto di tali ruoli sono: “Publish”, “Find” e “Bind”.
In particolare, un dominio mette a disposizione un modulo software accessibile attraverso la rete, fornendone una descrizione e rendendolo pubblico (Publish) catalogandolo in un apposito registro (registro UDDI). Il richiedente utilizza un’operazione di ricerca (Find) per recuperare la descrizione del servizio e utilizzarla per connettersi (Bind) al fornitore del servizio stesso e invocarlo o interagire con esso. Il ruolo di Fornitore e richiedente può essere assunto, a seconda dell’esigenza, dallo stesso soggetto.
Ogni servizio può essere implementato utilizzando linguaggi e tecnologie differenti, per le quali viene poi generata un’interfaccia WSDL e altre componenti che producono il livello di disaccoppiamento necessario per renderlo accessibile attraverso la rete mediante protocollo HTTP (o HTTPS) e linguaggio XML. Tale interfaccia viene pubblicata sul catalogo dei servizi (registro UDDI) per essere accessibile dall’esterno.
Il registro dei servizi UDDI è una specifica di un registry web-based distribuito che contiene informazioni sui servizi forniti dalle diverse Porte di Dominio. Il registro fornisce una serie di servizi ed una interfaccia che definiscono un contesto semplice per la descrizione di qualunque tipo di servizio offerto delle Porte di Dominio. La specifica consiste di documenti e di un XML-Schema che definisce un protocollo di programmazione, basato su XML/SOAP, specifico per le operazioni di pubblicazione e di ricerca dei servizi.
La specifica del registro consiste in un XML-Schema per messaggi SOAP ed in una descrizione di API. L’XML-Schema di UDDI definisce tre tipologie fondamentali di informazione, necessarie dal un punto di vista tecnico per poter utilizzare un servizio esposto da un dominio. Queste tipologie sono:
- Informazioni istituzionali (business entity)
- Informazioni sul servizio (o informazioni di binding)
- Informazioni specifiche dei servizi
In particolare, tra le informazioni specifiche di ciascun servizio sono incluse le descrizioni delle interfacce applicative dei servizi stessi (tramite metalinguaggio WSDL). Il richiedente del servizio deve trovare nelle descrizioni pubblicate tutto quanto necessario per formulare richieste di servizio (tramite le buste e-government) al fornitore del servizio specifico.
La descrizione WSDL del servizio permette, inoltre, (attraverso uno specifico elemento di descrizione) di specificare i possibili profili di collaborazione disponibili per l’accesso a quel dato servizio (notifica o richiesta servizi sincrona e asincrona) tramite i profili base disponibili nel metalinguaggio WSDL.

Publish & Subscribe
-------------------------
Come precedentemente riportato, una delle tecnologie adottate questo sistema è quello del Publish & Subscribe, il quale è in grado di fornire le seguenti funzionalità:
- gestione degli Eventi: funzionalità di gestione delle code di eventi, delle relative liste di sottoscrizione/pubblicazione, degli stati di consegna e delle relative ricevute. Il sistema sarà in grado di gestire:
- tempi di scadenza delle notifiche per ogni tipologia di evento
- consegne presso caselle di posta;
- integrazione del Gestore eventi con la Porta di Dominio: sono moduli che permettono al sistema di Publish & Subscribe di utilizzare la porta di dominio per comunicare l’invio dei messaggi. Forniscono i seguenti servizi:
- Servizi di sottoscrizione: i moduli di Sottoscrizione permettono, ai soggetti interessati, di ricevere la notifica di eventi per cui sono sottoscritti
- Servizi di pubblicazione: il servizio di pubblicazione consiste nella possibilità di notificare al gestore un evento in una particolare categoria
- Servizi di ricevute: il modulo provvede a fornire le seguenti tipologie di ricevute: una ricevuta di “presa in carico” di una richiesta di notifica viene rilasciata al momento della ricezione dell’evento da parte del sistema di Publish & Subscribe, le ricevute finali di avvenuta o mancata consegna vengono inviate dallo stesso sistema all’Ente che ha richiesto il servizio di notifica (la ricevuta finale contiene anche le informazioni protocollari in entrata dei singoli destinatari ove possibile, qualora la consegna avvenga ad un altro message broker la ricevuta contiene evidenza dell’avvenuta consegna ai destinatari finali ove reso possibile dall’altro sistema di message brokering). Il modulo provvede ad ottenere dal destinatario una ricevuta di accettazione dell’evento al momento della notifica presso la porta di dominio del dominio
- Directory dei sottoscrittori/pubblicatori: questo modulo contiene la lista ei sottoscrittori al servizio di notifica, per ogni sottoscrittore sono riportate le tipologie di eventi ed i pubblicatori a cui è abilitato e l’indirizzo (porta di dominio) a cui notificare l’evento. La directory contiene anche la lista dei pubblicatori contenente per ogni pubblicatore l’indirizzo da cui la notifica è generata e la tipologia di eventi generabili.
- Filtro dei Sottoscrittori: Il sistema di P&S implementa una regola di filtro dei sottoscrittori in modo tale da inoltrare la scheda anagrafico professionale ai soli sottoscrittori effettivamente interessati a ricevere l’evento. A tal fine, il sistema di P&S identifica due modi di registrazione per i sottoscrittori:
- Registrazione statica: Il sottoscrittore si registra al P&S in modo statico quando deve ricevere sempre e comunque l’evento. 
- Registrazione dinamica: Il sottoscrittore si registra al P&S in modo dinamico quando deve ricevere l’evento su richiesta del mittente.
All’interno del body sarà ricavabile la lista dei destinatari.
