Allegato H - Controlli di coerenza dei dati
===========================================



Controlli sulle SAP
-------------------

I controlli indicati nel presente documento hanno ripercussioni sui seguenti moduli:
- Interfacce Web delle piattaforme SAP
- Cooperazione applicativa


Controlli generici
~~~~~~~~~~~~~~~~~~
Si ricordano i controlli già presenti sul sistema, già previsti dai modelli ministeriali:
- Compilazione dei campi obbligatori: il controllo viene effettuato nella maggior parte dei casi tramite XSD; ci sono casi particolari di campi obbligatori solo in particolari situazioni che saranno trattati di seguito nel presente documento.
- La congruenza del tipo di dato inserito rispetto agli standard tecnici (es: validità di una data, controllo sul tipo di dato inserito - numerico/alfanumerico, ecc.).
- I controlli incrociati previsti negli standard tecnici (es: campi condizionati).
Tali controlli sono vincolanti per l’accettazione del dato.



Controlli aggiuntivi
~~~~~~~~~~~~~~~~~~~~
In questo documento verranno pertanto trattati i controlli non direttamente deducibili dei modelli ministeriali, fornendo per ciascuno di essi il livello di richiesta per il soddisfacimento del requisito:
- Vincolante: il controllo deve dare esito positivo per poter accettare la comunicazione. Non è possibile proseguire fino alla correzione dell’errore rilevato.
- Avviso: il controllo rileva un’anomalia, ma è compito del soggetto obbligato/abilitato decidere se procedere o meno (gestione dei casi particolari). Questo tipo di controllo non è applicable nel contesto del Nodo di Coordinamento Nazionale.


Impatto dei controlli
~~~~~~~~~~~~~~~~~~~~~
     
Tipologie di controlli
~~~~~~~~~~~~~~~~~~~~~~


Legenda della terminologia relativa ai controlli
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
