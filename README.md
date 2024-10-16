# Testo Predittivo con N-Grammi

Questo progetto implementa un semplice modello di testo predittivo utilizzando gli n-grammi a partire dal testo del libro **"Il fantasma di Canterville"** di Oscar Wilde. Il codice legge il testo, lo pulisce, crea una mappa di n-grammi di lunghezza fissa e utilizza queste informazioni per generare nuove sequenze di testo in modo probabilistico.

## Funzionamento del Codice

### 1. Caricamento e Pulizia del Testo

Il file **"Il fantasma di Canterville"** viene letto e processato rimuovendo caratteri indesiderati come le nuove righe (`\n`) e i caratteri di sottolineatura (`_`), e convertendo il testo in minuscolo per una maggiore uniformità. Questa operazione viene eseguita dalla funzione `clean()`.

### 2. Creazione degli N-Grammi

Il codice crea un dizionario di n-grammi (sequenze di caratteri consecutive) con una lunghezza specificata (in questo caso 5). Per ogni n-gramma, il programma tiene traccia delle lettere che seguono immediatamente quell'n-gramma e calcola la loro frequenza di occorrenza, che viene poi trasformata in probabilità.

### 3. Generazione del Testo

Partendo da un n-gramma iniziale specificato (es. `"io ho"`), il programma genera una sequenza di caratteri di una lunghezza specificata (`n_iteration`, impostato su 200 caratteri), scegliendo la lettera successiva basata sulla distribuzione probabilistica delle lettere che seguono quell'n-gramma.

### Dipendenze

- **NumPy**: Utilizzato per calcolare le probabilità e gestire array di dati.
- **Collections**: Utilizzato per contare le occorrenze delle lettere successive.
- **Matplotlib**: (facoltativo, non utilizzato in questa versione del codice, ma incluso se si volesse visualizzare qualche grafico).

