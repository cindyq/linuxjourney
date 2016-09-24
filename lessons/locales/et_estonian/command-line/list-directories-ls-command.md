# ls (List Directories)

## Tunni sisu

Nüüd, kus me oskame süsteemis ringi liikuda, kuidas saaksime teada, kuhu meil üldse on võimalik minna? Hetkel me ekleksime justkui pimeduses. Meil on võimalik kasutada imelist ls käsku, et kuvada kataloogide sisu. Ls käsk kuvab vaikimisi kõik jooksvas kataloogis asuvad kataloogid ja failid, kuid võid ka täpsustada, millise asukoha sisu sa näha soovid.

<pre>$ ls
$ ls /home/pete</pre>

ls on päris kasulik tööriist, sest see näitab sulle kuvatud failide ja kataloogide kohta detailset informatsiooni.

Pea meeles, et mitte kõik failid ja katalookig ei ole sulle nähtavad. Failid, mille nimed algavad . on peidetud, kuid neid saab näha ls käsuga kui sellele on lisatud lipp -a (inglise keeles a nagu all ehk kõik).

<pre>$ ls -a</pre>

Üks kasulik lipp on veel, -l nagu long ehk pikk. See kuvab failide detailse nimekirja pikemas formaadis. Detailne info, mida kuvatakse on alates vasakult: faili õigused, ühenduste arv, omaniku nimi, omanik-grupp, faili suurus, viimase muutmise ajatempel, ja faili/kataloogi nimi.

<pre>$ ls -l</pre>

<pre>pete@icebox:~$ ls -l
total 80
drwxr-x--- 7 pete penguingroup   4096 Nov 20 16:37 Töölaud
drwxr-x--- 2 pete penguingroup   4096 Oct 19 10:46  Dokumendid
drwxr-x--- 4 pete penguingroup   4096 Nov 20 09:30 Allalaadimised
drwxr-x--- 2 pete penguingroup   4096 Oct  7 13:13   Muusika
drwxr-x--- 2 pete penguingroup   4096 Sep 21 14:02 Pildid
drwxr-x--- 2 pete penguingroup   4096 Jul 27 12:41   Avalik
drwxr-x--- 2 pete penguingroup   4096 Jul 27 12:41   Mallid
drwxr-x--- 2 pete penguingroup   4096 Jul 27 12:41   Videod</pre>

Käskudel on funktsionaalsuse lisamiseks lipud (või argumendid või valikud, kuidas sulle parasjagu meeldib neid nimetada).  Märkasid, et lisasime -a ja -l, neid saab ka koos kasutada, lisades käsule -la. Lippude järjekorrast oleneb, mis järjekorras käksu täidetakse. Enamus ajast ei ole sellel erilist tähendust, nii et võid kirjutada ka -al ja see töötab sellegi poolest.

<pre>$ ls -la</pre>

## Harjutus

Proovi sisestada ls käsku erinevate lippudega ja vaata, mis väljundi sa saad.

## Küsimus

Millist käsku sa kasutaksid, et näha peidetud faile?

## Vastust

ls -a