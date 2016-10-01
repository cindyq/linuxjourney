# env (Environment)

## Tunni sisu

Käivita käsk:

$ echo $HOME

Sa peaksid nägema oma kodukataloogi otsiteeknda, minu oma näeb selline välja /home/pete.

Aga see käsk?

$ echo $USER 

Sa peaksid nägema enda kasutajanime!

Kust see infiormatsioon pärineb? See pärineb sinu keskkonna muutujatest. Sa saad neid näha, kui trükid

$ env 

See väljund, kuvab palju infot selle kohta, millised keskkonna muutujad sul parasjagu seatud on. Nendes muutujates on palju kaslikku infot, mida kest ja teised protsessid saavad kasutada.

Siin on lühike näide:

<pre>
PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/bin
PWD=/home/user
USER=pete
</pre>

Üks eriliselt oluline muutuja on PATH muutuja.  Nendele saab ligi, kui topid $ sümboli muutujanime ette, niimoodi:

<pre>
$ echo $PATH
/usr/local/sbin:/usr/local/bin:/usr/sbin:/bin
</pre>

See tagastab nimekirja koolonitega eraldatud teekondades, milleni su süsteem ulatub, kui see käivitab käsu.  Ütleme, et sa laed Internetis käsitsi alla ja paigaldad paketi, mille sa paned mittestandardsesse kataloogi ja tahas käivitada käsku. Sa kirjutad $ lahekäsk ja käsuviip ütleb, et käsku ei leitud. See on küll tobe. Sa vaatad kaustas binaari ja tead, et see on olemas. Mis toimub on see, et  $PATH muutuja ei kontrolli selle kataloogi seda binaari ning seetõttu annab veateate.

Ütleme, et sul on tonnides binaare, mida sa tahad käivitada väljaspool seda kataloogi, sa võid lihtsalt muuta PATH muutujat, et see sisaldaks vajalikku kataloogi sinu PATH keskkonna muutujas.

## Harjutus

Mida teeb järgmine käsk? Miks?
<pre>$ echo $HOME</pre>

## Küsimus

Kuidas sa näed keskkonna muutujaid?

## Vastus

env

