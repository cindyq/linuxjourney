# stderr (Standard Error)

## Tunni sisu

Proovime nüüd midagi natuke teistsugust. Proovime saada sisu loetelu mingist kataloogist, mida ei eksisteeri ja suuname selle info taaskord pähklid.txt faili.

<pre>$ ls /olematu/kataloog > pähklid.txt </pre>

Sa peaksid nägema midagi sellist:

<pre>ls: cannot access /fake/directory: No such file or directory</pre>

Ehk sa mõtled, kas see teade ei oleks pidanud saadetama hoopis faili? Tegelikult on olemas veel üks sisend-väljundvoog, standardveaväljund (stderr). Vaikimisi saadab stderr oma väljundi muuhulgas a ekraanile, see on stdout voost täiesti erinev ja selle väljundit tuleb ka suunata teisiti.

Kahjuks ei ole see ümbersuunamise operaator sama kena, kui <b>&lt;</b> või <b>&gt;</b>, kuid see on üsna sarnane. Me peake kasutama failideskriptorit.  Failideskriptor on mittenegatiivne number, mida kasutatake, et faili voole ligi pääseda. Me süübime sellesse hiljem, kuid praegu pead sa teadma, et failideskriptor stdin, stdout ja stderr jaoks on vastavalt 0, 1 ja 2.

Seega, kui me tahame suunata oma stderr ümber faili, saame me toimida järgnevalt:

<pre>$ ls /olematu/kataloog 2> pähklid.txt</pre>

Sa peaksid nägama failis pähklid.txt ainult stderr teadet.

Aga mis saab siis, kui ma tahan näha nii stderr kui ka stdout väljundit pähklid.txt failis?s Seda saab samuti teha failideskriptoriga:

<pre>$ ls /olematu/kataloog > pähklid.txt 2>&1</pre>

See käsk saadab ls /olematu/kataloog tulemuse failile pähklid.txt ja seejärel suunab stderr väljundi stdout'le kasutades operaatorit 2>&1. Siin on oluline toimingute järjekord, 2>&1 saadab stderr'i millelegi, millele stdout viitab. Hetkel viitab see failile. Seega, kui sa avad selle pähklid.txt faili, pekasid sa nägema mõlemat, stderr ja stdout väljundit. Meie näite põhjal, on ülemise käsu väljund ainult stderr.

Selline on lühem viis, kuidas suunata mõlemad, stdout ja stderr, faili:

<pre>$ ls /olematu/kataloog &> pähklid.txt</pre>

Aga mis siis, kui ma ei tahagi seda üleliia risustavat infot ja tahan stderr teadetest täielikult vabaneda? Sa võid suunata väljundi spetsiaalsesse faili /dev/null ja igasugune sisendinfo lihtsalt heidetakse kõrvale.

<pre>$ ls /olematu/kataloog 2> /dev/null</pre>

## Harjutus

Mida teeb allolev käsk?

<pre>$ ls /olematu/kataloog >> /dev/null 2>&1</pre>

## Küsimus

Millist märki kasutatakse stderr ümbersuunamiseks?

## Vastus

2>
