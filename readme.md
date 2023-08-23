# Week19Day1
**********USARE GIT DA CONSOLE************
1) CREARE REPOSITORY SU GITHUB
2) ALL'INTERNO DI UNA CARTELLA VUOTA (LA NOSTRA WORKING STATION) APRIRE UN TERMINALE (i.e. GITBASH)
3) $ git init -> CREARE LA REPOSITORY LOCALE
4) $ touch -> CREARE FILE (i.e.  $ touch readme.md -> crea un file readme)
5) $ ls -> LISTARE I FILE NELLA WORKING STATION
6) $ git status -> STATO DELLA REPOSITORY
7) $ git add . -> AGGIUNGERE TUTTI I FILE ALLA STAGING AREA
7.1) $ git add <nome_file> -> AGGIUNGERE IL FILE SELEZIONATO ALLA STAGING AREA
8) $ git diff -> MOSTRA LE MODIFICHE APPORTATE AI FILE NELLA STAGING AREA
9) $ git commit -m "<messaggio>" -> AGGIUNGERE I FILE DALLA STAGING AREA NELLA REPOSITOY LOCALE
10) $ git log -> STORICO DEI COMMIT
11) $ git branch -M <nome> -> CAMBIARE NOME AL BRANCH (i.e. $ git branch -M <main> -> MODIFICA IL NOME DELLA BRANCH PRINCIPALE DA MASTER A MAIN)
12) $ git remote add origin <url> -> COLLEGARE LA REPOSITORY LOCALE A QUELLA REMOTA (i.e. $ git remote add origin https://github.com/WalterBarbieri/Week19Day3.git)
13) $ git push --set-upstream origin main -> PRIMO PUSH CREA UPSTREAM VERSO CORRETTO BRANCH ED EFFETTUA IL PUSH
13.1) $ git push -> DOPO PRIMO PUSH CON UPSTREAM SI USA DIRETTAMENTE PUSH 
14) $ git branch -> LISTA BRANCH
15) $ git branch <nome_branch> -> CREARE NUOVA BRANCH (i.e. $ git branch new-branch)
16) $ git checkout <nome_branch> -> PASSA ALLA BRANCH SELEZIONATA (i.e. $ git checkout new-branch)
17) $ touch index.js -> CREA NUOVO FILE JS NELLA BRANCH
17.1) $ touch index2.js -> CREA NUOVO FILE JS NELLA BRANCH
17.2) $ git add . -> AGGIUNGE NUOVI FILE NELLA STAGIN AREA
17.3) $ git commit -m "Added index & index2" -> AGGIUNGE I FILE DALLA STAGIN AREA NELLA LOCAL REPOSITORY CON MESSAGGIO
17.4) $ git push --set-upstream origin new-branch -> PUBBLICO DALLA LOCAL ALLA REMOTE REPOSITORY CON UPSTREAM PER PRIMA CONNESSIONE AL NUOVO BRANCH
18) $ git checkout main -> TORNO IN MAIN
19) $ git merge <nome_branch> -> EFFETTUA MERGE DELLA BRANCH SELEZIONATA SULLA BRANCH CORRENTE IN LOCALE, IN QUESTO CASO SU MAIN (i.e. $ git merge new-branch)
20) $ git push -> PUBBLICA LE MODIFICA NELLA REPOSITORY REMOTA 
21) $ git branch -d <nome_branch> -> ELIMINA LA BRANCH IN LOCALE
21.1) $ git push origin -d <nome-branch> ELIMINA LA BRANCH IN REMOTO
22) $ git tag v1.0.0 -> AGGIUNGE TAG LIGHTWEIGHT
23) $ git tag -a v1.0.1 -m "added tag" -> AGGIUNGE TAG ANNOTATED
24) $ git tag -> LISTA TAGS
25) $ git push --tags -> PUSH DEI TAGS IN REMOTO
26) $ git remote -v -> CONTROLLA CONNESSIONE CON LA REPOSITORY REMOTA

*********** GIT LOG **********
Può essere personalizzato per la visualizzazione dei commit con tags specifici:
) $ git log --pretty=oneline -> VISUALIZZA INFO SU UNA LINEA
) $ git log -3 -> VISUALIZZA ULTIMI 3
) $ git log --since=1week -> FILTRA ULTIMA SETTIMANA
) $ git log --after=2023-01-01 --before=2023-01-31 -> FILTRA IN ARCO TEMPORALE
) $ git log --after=2023-01-01 --before=2023-01-31 --pretty=oneline -> FILTRA PIU' PARAMETRI

*********** GIT FLOW **********
1) $ git flow init -> INIZIALLIZZA GIT FLOW -> IMPOSTARE MAIN & DEVELOP + PREFISSI
2) $ git flow <subcommand> start <nome_branch> -> CREA BRANCH NEL SUBCOMMAND SCELTO (i.e. $ git flow feature start first-feature)
3) $ touch firstFeature.js
4) $ git add .
5) $ git commit -m "Added first feature"
6) $ git push --set-upstream origin <subcommand>/<nome_branch> -> PUSH DELLE MODIFICHE SULLA REPOSITORY REMOTA
7) $ git flow <subcommand> finish <nome_branch> -> MERGE DEL BRANCH NEL SUBCOMMAND DI RIFERIMENTO CON ELIMINAZIONE CONTESTUALE DEL BRANCH TORNA SUL SUBCOMMAND (i.e. $ git flow feature finish first-feature)
8) $ git push -> PER SALVARE SUBCOMMAND BRANCH IN REMOTO
9) $ git flow release start 1.0 -> INIZIA LA RELEASE SU MAIN 
10) $ git flow release finish 1.0 -> DOPO IL CONTROLLO CONCLUDE LA RELEASE SUL MAIN E CI RIPORTA SU DEVELOP