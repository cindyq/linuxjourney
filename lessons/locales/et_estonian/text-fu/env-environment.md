# env (Environment)

## Tunni sisu

Käivita käsk:

<pre>$ echo $HOME</pre>

Sa peaksid nägema oma kodukataloogi otsiteekonda, minu oma näeb selline välja /home/pete.

Aga see käsk?

<pre>$ echo $USER</pre> 

Sa peaksid nägema enda kasutajanime!

Kust see infiormatsioon pärineb? See pärineb sinu keskkonna muutujatest. Neid saab näha, kui trükid

<pre>$ env</pre> 

See väljund kuvab palju infot parasjagu seatud keskkonna muutujate kohta. Nendes muutujates on palju kaslikku infot, mida kest ja teised protsessid saavad kasutada.

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

Kui käsk käivitada, tagastab see nimekirja koolonitega eraldatud teekondades, milleni su süsteem ulatub. Ütleme, et sa laed Internetis käsitsi alla ja paigaldad paketi, mille sa paned mittestandardsesse kataloogi ja tahas käivitada käsku. Sa kirjutad $ lahekäsk ja käsuviip ütleb, et käsku ei leitud. See on küll tobe! Sa vaatad kaustas binaari ja tead, et see on olemas. Mis toimub on see, et $PATH muutuja ei kontrolli selle kataloogi seda binaari ning seetõttu annab veateate.

Ütleme, et sul on tonnides binaare, mida sa tahad käivitada väljaspool seda kataloogi. Võib lihtsalt muuta PATH muutujat, et see sisaldaks vajalikku kataloogi sinu PATH keskkonna muutujas.

## Harjutus

Mida teeb järgmine käsk? Miks?
<pre>$ echo $HOME</pre>

## Küsimus

Kuidas näha keskkonna muutujaid?

## Vastus

env

