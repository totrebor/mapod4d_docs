# GITHUB MAPOD4D

Qui di seguito il flusso di lavoro utilizzato dalla community. Tale flusso è consigliato per evitare conflitti di codice con gli altri membri:

**Prima di iniziare**

- **fork del repository principale:** per effettuare il _fork_ un repository basta cliccare sul bottone **_Fork_** in alto a destra della pagina **Github** del _repository_.

- **prendere il link del repository forkato:** dopo aver forkato il _repository_ principale, comparirà nella lista dei _repositories_ dell'account utente il _repository_ forkato. Accedendo alla pagina potrete copiare il link dall menú a tendina che si aprirà premendo il tasto verde "**Code**".

         https://github.com/[username]/[nome_repository].git

- **clonare localmente e accedere al repository:** per clonare e accedere vanno utilizzati questi due comandi da terminale (assicurarsi che il terminale sia sulla cartella di lavoro):

        git clone https://github.com/[username]/[nome_repository].git
        cd [nome_repository]

- **settare i remoti nel repo locale:** per settare i remoti si usano i seguenti comandi:

        git remote add mapod4d https://github.com/mapod4d/[nome_repository].git
        git remote set-url --push NOPUSH

  questi comandi serviranno a creare una connessione al repository principale soltanto per la _pull_ dei dati.

Una volta che il nostro ambiente di lavoro è pronto, possiamo iniziare a lavorare alle nostre task.

## Giorno 1

#### ciclo di lavoro a inizio task:

1.  inzio creando un branch con il task di progetto

        git branch [nome_task]

    - lavoro sul branch
    - faccio add e commit ogni qualvolta raggiungo degli step di lavoro

      git add [nome_file + .estensione]
      git commit -m "[inserire titolo commit]"

    - finisco di lavorare sulla task

1.  ritorno al master

        git checkout master

1.  unisco il branch su cui ho lavorato al master

        git merge [branch]

    - risolvere conflitti

1.  scaricare possibili nuovi aggiornamenti dal repo principale

        git pull mapod4d master

    - risolvere conflitti

1.  portare le modifiche al repository forkato

        git push origin master

<!-- ## Giorno 2

#### ciclo di lavoro a inizio task:

ciclo di lavoro giornata con task iniziato:
(giornata)
1a git pull mapod4d master
2a risolvere conflitti
3a git pull --prune
3a git checkout [branch]
4a git merge master
1b lavoro sul branch
2b add and commit
3b add and commit
4b add and commit
5a git checkout master
6a git merge [branch] e risolvere conflitti
7a git pull mapod4d master
8a risolvere conflitti
9a git push origin master

ciclo di lavoro giornata con task finito:
1a git pull mapod4d master
2a risolvere conflitti
3a git pull --prune
3a git checkout [branch]
4a git merge master
5a git push origin [branch]
6a git checkout master

soluzione:
fetch -->
