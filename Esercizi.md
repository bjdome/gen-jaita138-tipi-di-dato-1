### Database 1
**Gestione di una Biblioteca**:
Libro:

| Attributo          | Tipo mySQL | Tipo Java | Note                      |
| ------------------ | ---------- | --------- | ------------------------- |
| isbn               | int        | int       |                           |
| titolo             | varchar    | String    |                           |
| autore             | varchar    | String    |                           |
| genere             | varchar    | String    |                           |
| pagine             | int        | int       | quante pagine ha un libro |
| descrizione        | text       | String    |                           |
| casa_editrice      | varchar    | String    |                           |
| data_pubblicazione | date       | LocalDate |                           |

Membro:

| Attributo    | Tipo mySQL | Tipo Java | Note                                                        |
| ------------ | ---------- | --------- | ----------------------------------------------------------- |
| cf           | varchar    | String    |                                                             |
| nome         | varchar    | String    |                                                             |
| cognome      | varchar    | String    |                                                             |
| data_nascita | date       | LocalDate |                                                             |
| libri_letti  | int        | int       | quanti libri ha letto in tutto                              |
| libro_preso  | varchar    | String    | titolo del libro attualmente preso in prestito, se presente |


Prestito:

| Attributo  | Tipo mySQL | Tipo Java | Note                                                                                |
| ---------- | ---------- | --------- | ----------------------------------------------------------------------------------- |
| isbn       | int        | int       |                                                                                     |
| cf_membro  | varchar    | String    | chi lo ha preso attualmente, se non è in biblioteca                                 |
| preso      | bit        | boolean   | per controllare se è attualmente presente in biblioteca o è stato preso da qualcuno |
| data_preso | date       | LocalDate | quando è stato preso un libro                                                       |


### Database 2
**Catalogo di un Ristorante**:
Piatto:

| Attributo          | Tipo mySQL | Tipo Java | Note                                                                                                          |
| ------------------ | ---------- | --------- | ------------------------------------------------------------------------------------------------------------- |
| nome               | varchar    | String    |                                                                                                               |
| numero_ingredienti | int        | int       |                                                                                                               |
| ordinato           | bit        | boolean   | per sapere se il piatto è stato ordinato                                                                      |
| quanto_ordinato    | int        | int       | per sapere quante volte è stato ordinato, se è stato preso poche volte si può pensare di rimuoverlo/cambiarlo |
| prezzo             | decimal    | float     |                                                                                                               |
| sul_menu           | bit        | boolean   | per sapere se il piatto è attualmente sul menu, o è stato rimosso/da aggiungere                               |

Ingrediente:

| Attributo   | Tipo mySQL | Tipo Java | Note                                                               |
| ----------- | ---------- | --------- | ------------------------------------------------------------------ |
| nome        | varchar    | String    |                                                                    |
| provenienza | varchar    | String    |                                                                    |
| quantita    | int        | int       | per sapere quanto di un certo ingrediente è presente nel magazzino |
| richiesto   | int        | int       | in quanti piatti è richiesto                                       |
| prezzo      | decimal    | float     | quanto costa l'ingrediente                                         |


Cliente:

| Attributo   | Tipo mySQL | Tipo Java | Note                              |
| ----------- | ---------- | --------- | --------------------------------- |
| nome        | vachar     | String    |                                   |
| cognome     | varchar    | String    |                                   |
| prenotato   | bit        | boolean   | se ha prenotato prima di venire   |
| telefono    | varchar    | String    |                                   |
| ordinazione | int        | int       | quanti piatti sono stati ordinati |
| pagamento   | bit        | boolean   | pagamento in contanti o carta     |

### Database 3
**Catalogo di un Negozio di Fiori**
Fiore

| Attributo | Tipo mySQL | Tipo Java | Note                                        |
| --------- | ---------- | --------- | ------------------------------------------- |
| nome      | varchar    | String    |                                             |
| tipo      | varchar    | String    |                                             |
| quantita  | int        | int       | quanti fiori di ci sono nel negozio         |
| finto     | bit        | boolean   |                                             |
| prenotato | bit        | boolean   | se il fiore è stato richiesto da un cliente |
| prezzo    | decimal    | float     |                                             |

Fornitore

| Attributo | Tipo mySQL | Tipo Java | Note                             |
| --------- | ---------- | --------- | -------------------------------- |
| nome      | varchar    | String    |                                  |
| tipo      | varchar    | String    | che tipo di fiore fornisce       |
| quando    | date       | LocalDate | quando arriva il prossimo carico |
| prezzo    | decimal    | float     |                                  |


Cliente

| Attributo    | Tipo mySQL | Tipo Java | Note                  |
| ------------ | ---------- | --------- | --------------------- |
| nome         | varchar    | String    |                       |
| cognome      | varchar    | String    |                       |
| prenotazione | bit        | boolean   |                       |
| fiore        | varchar    | String    |                       |
| quanti       | int        | int       | quanti fiori ha preso |
