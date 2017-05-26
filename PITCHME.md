# Processing Test


---


## Cosa sono i test di Processing

- servono per garantire la stabilità degli algoritmi |
- procedura: |
- lancio algoritmo con dati di test |
- verifica risultati |
- caricamento file di output sul repository |

---

## Come funzionano i test?

- Integrazione continua su Travis |
- esecuzione algoritmo e verifica risultati |
- se corretti, test passato e "garanzia" stabilità algoritmo |
- se risultati in background diversi non corrispondono, test fallisce: |
- controllo algoritmo se ha errori |
- eventuale fix |
- controllo del risultato |


---

## Difficoltà riscontrate (1)

- file di output consigliato è GML (diverse limitazioni) |
- difficoltà del framework, non è di immediato utilizzo |
- continuo aggiornamento del codice |
- Travis timeout durante la compilazione |
- discrepanza minima di coordinate (approssimazione decimali) |

---

## Difficoltà riscontrate (2)

- molti algoritmi non sono testabili: |
- algoritmi che non restituiscono dati (selezione) |
- algoritmi che caricano dati su PostGIS o SpatiaLite |
- a volte verifiche troppo restrittive (aggiunta campo tabella, verifica estensione layer -> problema di prima) | 
- tipo di output formato testo (es. info layer) difficili da testare (regex) |

---

## Stato dei test

- tutto è su repository https://github.com/ghtmtt/qgis_test_script: |

---

## Stato dei test GDAL

- 49 algoritmi totali |
- 35 algoritmi testati: |
- 17 algortmi corretti |
- 18 algoritmi con problemi | 
- 8 algoritmi mancanti |

---

## Stato dei test QGIS

- 154 algoritmi totali |
- 115 algoritmi testati: |
- 24 algortmi corretti |
- 29 algoritmi con problemi | 
- 39 algoritmi mancanti |

---

## Risultati ottenuti

- molti algoritmi adesso sono "blindati" |
- diversi ticket aperti e risolti: |
- GDAL 7 |
- QGIS 5 |

---

### Considerazioni finali

- framework test migliorabile (più intuitiva) |
- possibilità (non immediata) di aggiungere test per algoritmi prima non testabili (es. selezione) tramite la creazione di script ad hoc |
- refactoring di Processing in C++ |
- porting provider (SAGA), test possibili? | 
- tempo iniziale per testing sottostimato: |
- difficoltà formato file output (GML) |
- Travis timeout inficia e allunga molto i tempi |
 - continuo aggiornamento algoritmi e Processing = manutenzione continua |
