# GITHUB MAPOD4D

Qui di seguito il flusso di lavoro utilizzato dalla community. Tale flusso è obbligatorio, non verranno accettate pull che non lo seguano:

## Prima di iniziare

<<<<<<< HEAD
- **Creare un'aria di sviluppo:** se non si ha già un'area di lavoro, crearne una. Questa servirà a mettere tutte cartelle che si utilizzeranno per i lavori della community (Es.: _area_sviluppo_).
=======
- **creiamo un'area di lavoro:** se non si ha già un'area di lavoro, crearne una. Questa servirà a mettere tutte cartelle che si utilizzeranno per i lavori della community (Es.: _area_lavoro_).
>>>>>>> d32a2e8d0b755952e368357626a4913df5a5ac18

- **fork del repository principale:** per effettuare il _fork_ un repository basta cliccare sul bottone **_Fork_** in alto a destra della pagina **Github** del _repository_.

- **prendiamo il link del repository forkato:** dopo aver forkato il _repository_ principale, comparirà nella lista dei _repositories_ dell'account utente il _repository_ forkato. Accedendo alla pagina potrete copiare il link dall menú a tendina che si aprirà premendo il tasto verde "**Code**".

         https://github.com/[username]/[nome_repository].git

- **cloniamo localmente e accediamo al repository:** per clonare e accedere vanno utilizzati questi due comandi da terminale (assicurarsi che il terminale sia sulla cartella di lavoro):

        git clone https://github.com/[username]/[nome_repository].git
        cd [nome_repository]

- **settiamo i riferimenti dei repository remoti nel repository locale:** per settare i remoti si usano i seguenti comandi:

        git remote add mapod4d https://github.com/mapod4d/[nome_repository].git

  questi comandi serviranno a creare una connessione al repository principale soltanto per la _pull_ dei dati. **ATTENZIONE:** se sei amministratore, settare la push su NO PUSH (vedi riferimenti alla sezione **Sei Amministratore?**)

Una volta che il nostro ambiente di lavoro è pronto, possiamo iniziare a lavorare ai nostri task.

## Giorno 1

#### ciclo di lavoro a inizio task:

1.  scarichiamo possibili nuovi aggiornamenti dal repository principale

        git pull mapod4d master

1.  inziamo creando un branch con il task di progetto

        git branch [nome_task]

1.  ci spostiamo sul branch

        git checkout [nome_branch]

    - eseguiamo il task
    - facciamo add e commit ogni qualvolta raggiungiamo degli step di lavoro

          git add [nome_file + .estensione]

          git commit -m "[inserire titolo commit]"

    - finiamo di lavorare sul task

1.  ritorniamo al master

        git checkout master

1.  uniamo il branch su cui abbiamo lavorato al master

        git merge [nome_branch]

    - risolviamo i conflitti

1.  scarichiamo possibili nuovi aggiornamenti dal repository principale

        git pull mapod4d master

    - risolviamo i conflitti

1.  portiamo le modifiche al repository forkato

        git push origin master

## Giorno n

#### ciclo giorni successivi:

1.  scarichiamo possibili nuovi aggiornamenti dal repository principale

        git pull mapod4d master

    - risolviamo i conflitti

1.  puliamo la cache del repository

        git pull --prune

1.  ci spostiamo sul branch

        git checkout [nome_branch]

1.  uniamo il master al branch

        git merge master

    - lavoriamo sul branch
    - facciamo add e commit ogni qualvolta raggiungiamo degli step di lavoro

          git add [nome_file + .estensione]

          git commit -m "[inserire_titolo_commit]"

    - finiamo di lavorare al task

1.  ritorniamo al master

        git checkout master

1.  uniamo il branch su cui ho lavorato al master

        git merge [branch]

    - risolviamo i conflitti

1.  scarichiamo possibili nuovi aggiornamenti dal repository principale

        git pull mapod4d master

    - risolviamo i conflitti

1.  portiamo le modifiche al repository forkato

        git push origin master

**N.B.**: se non hai ultimato il task, riprendere dal **Giorno n**. Se hai ultimato il task, puoi continuare a leggere.

## Cosa succede ora?

### Aprire una _Pull Request_

Bisogna accedere a GitHub ed effettuare la **_Pull Request_** cliccando su **_Contribute_** e cliccando sul tasto verde **Create Pull Request**. Nella nuova pagina, inserire il task come titolo e poi clicchiamo sul tasto **Create Pull Request**.

### Che farne del branch dove abbiamo lavorato?

Prima di eliminare il branch su cui abbiamo lavorato, dobbiamo aspettare che ci venga data la conferma dell'avvenuta accettazione della **_Pull Request_**.

### Sei Amministratore?

- **settare i remoti nel repo locale:** per settare i remoti si usano i seguenti comandi:

        git remote add mapod4d https://github.com/mapod4d/[nome_repository].git
        git remote set-url --push mapod4d NOPUSH

  questi comandi serviranno a creare una connessione al repository principale soltanto per la _pull_ dei dati.
