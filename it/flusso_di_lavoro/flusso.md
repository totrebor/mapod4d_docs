# GITHUB MAPOD4D

Qui di seguito il flusso di lavoro utilizzato dalla community. Tale flusso è obbligatorio, non verranno accettate pull che non lo seguano:

## Prima di iniziare

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

1.  scaricare possibili nuovi aggiornamenti dal repo principale

        git pull mapod4d master

1.  inzio creando un branch con il task di progetto

        git branch [nome_task]

1.  ci spostiamo sul branch:

        git checkout [nome_branch]

    - lavoro sul branch
    - faccio add e commit ogni qualvolta raggiungo degli step di lavoro

          git add [nome_file + .estensione]

          git commit -m "[inserire titolo commit]"

    - finisco di lavorare sulla task

1.  ritorno al master

        git checkout master

1.  unisco il branch su cui ho lavorato al master

        git merge [nome_branch]

    - risolvere conflitti

1.  scaricare possibili nuovi aggiornamenti dal repo principale

        git pull mapod4d master

    - risolvere conflitti

1.  portare le modifiche al repository forkato

        git push origin master

## Giorno n

#### ciclo giorni successivi:

1.  scaricare possibili nuovi aggiornamenti dal repo principale

        git pull mapod4d master

    - risolvere conflitti

1.  pulire il lavoro

        git pull --prune

1.  ci spostiamo sul branch

        git checkout [nome_branch]

1.  unisco il master al branch

        git checkout [nome_branch]

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

## Giorno finale

#### ciclo giorni successivi:

1.  scaricare possibili nuovi aggiornamenti dal repo principale

        git pull mapod4d master

    - risolvere conflitti

1.  pulire il lavoro

        git pull --prune

1.  ci spostiamo sul branch

        git checkout [nome_branch]

1.  unisco il master al branch

        git checkout [nome_branch]

    - lavoro sul branch
    - faccio add e commit ogni qualvolta raggiungo degli step di lavoro

          git add [nome_file + .estensione]

          git commit -m "[inserire titolo commit]"

    - finisco di lavorare sulla task

1.  unisco il master al branch

        git merge master

    - risolvere conflitti

1.  scaricare possibili nuovi aggiornamenti dal repo principale

        git fetch mapod4d master

1.  unisco il master remoto di mapod4d al branch

        git merge mapod4d/master

    - risolvere conflitti

1.  portare le modifiche al repository forkato

        git push origin [nome_branch]

1.  unisco il master al branch

        git checkout master

## Cosa succede ora?

Bisogna accedere a Github ed effettuare la **_Pull Request_** cliccando sul **_Contribute_** e cliccare sul tasto verde **Create Pull Request**. Nella nuova pagina, inserire la task come titolo e poi clicchiamo sul tasto **Create Pull Request**.