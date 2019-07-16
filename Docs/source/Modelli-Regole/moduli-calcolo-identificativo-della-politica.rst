###########################################
Calcolo Identificativo della politica
###########################################


L’identificatore di una politica attiva è un codice alfanumerico composto da 11 caratteri, composto come di seguito riportato:

- (Numeric) I primi 2 caratteri rappresentano il codice del sistema di provenienza che effettua il primo invio della politica attiva nella sezione 6 della SAP generando l’identificatore della politica stessa –vedi tabella 1-; ad esempio se la politica attiva con ente promotore lombardo (quindi di competenza della regione Lombardia) viene inserita attraverso il cruscotto SAP del portale nazionale il campo sarà valorizzato con “00 - NCN”; eventuali aggiornamenti di questa politica attiva in cooperazione applicativa da parte della regione, non devono modificare l’identificatore generato.
- (Numeric) I caratteri 3 al carattere 10 (8 caratteri) rappresentano un numero sequenziale generato dal soggetto abilitato che invia l’aggiornamento della politica attiva nella sezione 6 della SAP. Il formato del numero sequenziale è esadecimale. Tale codifica garantisce la possibilità per soggetto abilitato di generare 4.294.967.296 sequenze di valori univoci;
- (Alfabetico) Il carattere 11 rappresenta il carattere di controllo che garantisce la coerenza con la tupla di 22 caratteri composta dai seguenti dati della politica attiva:
		+ Codice Ente Promotore (6.1.i): 11 caratteri;
		+ Tipo Attività Nazionale (6.1.a): 3 caratteri;
		+ Data proposta (6.1.l): 8 caratteri formato “aaaammgg”;
L’algoritmo di calcolo del carattere di controllo è lo stesso utilizzato per la generazione del sedicesimo carattere del codice fiscale. Per le regole di calcolo si rimanda alla documentazione presente sul sito `www.agenziaentrate.gov.it. <https://dichiarazioneprecompilata.agenziaentrate.gov.it/index.htm?v=20190502>`_ La modifica di uno dei dati precedentemente indicati non comporta il ricalcolo e la generazione di dell’undicesimo carattere.

Esempio di identificativo della politica:

- Soggetto abilitato: Regione Lazio (08).
- Numero sequenziale: 008B3B94 (esadecimale) ottenuto da 9124756 (decimale).
- Dati politica attiva:
		+ Codice Ente Promotore: H501X000004
		+ Tipo Attività: A02
		+ Data proposta: 20170101


Codice identificativo generato


+---------+------------------------------+--------------------+
|Soggetto |Codice protocollo sequenziale |Carattere Controllo |
+----+----+---+---+---+---+---+---+--+---+--------------------+
| 1  |  2 | 3 | 4 | 5 | 6 | 7 | 8 | 9| 10|         11         |
+====+====+===+===+===+===+===+===+==+===+====================+
| 0  |  8 | 0 | 0 | 8 | B | 3 | B | 9| 4 |         B          | 
+----+----+---+---+---+---+---+---+--+---+--------------------+


.. table:: Soggetti abilitati
   :name: Calcolo Identificativo della politica
    
============ ==================
Codice		 Descrizione
============ ==================
00		      NCN
01		      ABRUZZO
02		      BASILICATA
03		      BOLZANO
04		      CALABRIA
05		      CAMPANIA
06		      EMILIA ROMAGNA
07		      FRIULI VENEZIA GIULIA
08		      LAZIO
09		      LIGURIA
10		      LOMBARDIA
11		      MARCHE
12		      MOLISE
13		      PIEMONTE
14		      PUGLIA
15		      SARDEGNA
16		      SICILIA
17		      TOSCANA
18		      TRENTO
19		      UMBRIA
20		      VAL D’AOSTA
21		      VENETO
31		      DOL (Crescere in Digitale)
32		      SICAMERA (Crescere Imprenditori)
============ ==================