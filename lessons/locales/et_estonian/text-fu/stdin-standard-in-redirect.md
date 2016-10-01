# stdin (Standard In)

## Tunni sisu

Eelmises tunnis õppisime, et me saame kasutada erinevaid stdout voogusid, näiteks faili või ekraani. Samamoodi on olemas ka standardsisendi (stdin) voogusid. Teame, et onolemas stdin seadmetelt nagu klaviatuur, kuid me võime kasutada ka faile, teiste protsesside väljundeid ning ka terminali. Vaatame näidet.

Kasutame selle näite jaoks eelmise tunni pähklid.txt faili. Meenuta, et seal oli sees tekst Hello World.

<pre>$ cat <b>&lt;</b> pähklid.txt <b>&gt;</b> banaan.txt </pre> 

Just nagu meil oli <b>&gt;</b> stdout ümbersuunamiseks, on meil <b>&lt;</b> stdin ümbersuunamise jaoks.

Tavaliselt saadaksid sa cat käsu puhul sellele faili ja sellest saab stdin, praegusel juhul aga suunasime me stdin'ks pähklid.txt. Sedasi suunatakse cat pähklid.txt väljund ümber faili mimega banaan.txt

## Harjutus

Proovi paari käsku:
<pre>
$ echo <b>&lt;</b> pähklid.txt <b>&gt;</b> banaan.txt
$ ls <b>&lt;</b> pähklid.txt <b>&gt;</b> banaan.txt
$ pwd <b>&lt;</b> pähklid.txt <b>&gt;</b> banaan.txt
</pre>

## Küsimus

Millise käsuga suunad sa ümber stdin?

## Vastus

<
