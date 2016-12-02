# Tuuma paigaldamine

## Tunni sisu

Nüüd kui kogu see igav värk on selja taga, räägime parem tuuma paigaldamisest ja modifitseerimisest. Süsteemi võib paigaldada mitu tuuma. On veel meeles peatükk alglaadimisest? GRUB menüüst saab valida, millise tuumaga süsteem käivitada.

Et tuvastada süsteemi tuuma versioon, kasuta käsku:

<pre>$ uname -r
3.19.0-43-generic</pre>

*Uname* käsk kuvab süsteemi informatsiooni, -r kuvab tuuma väljalaske versiooni.

Linuxi tuuma võib paigaldada mitut moodi. Võib laadida alla lähtepaketi ja komplieerida, aga seda võib teha ka kasutades paketihaldustööriistu.

<pre>$ sudo apt install linux-generic-lts-vivid</pre>

Seejärel arvuti taaskäivitada värskelt paigaldatud tuumaga. On ju lihtne? Peaaegu, tuleb paigaldada ka teised Linuxi paketid nagu *linux-header*, *linux-image-generic* jne. Täpsustada saab ka versiooni numbrit, ülemine käsk võib välja näha ka nii: <b>sudo apt install 3.19.0-43-generic</b>.

Alternatiivina, kui huvi on uuendatud versiooni järgi, võib kasutada *dist-upgrade*'i. See teostab uuendused kõikidele pakettidele.

<pre>$ sudo apt dist-upgrade</pre>

On olemas palju erinevaid tuuma versioonie, mõnda kasutatakse LTS (*long term support* ehk pikaajalise toega), mõned on uuemad ja vingemad. Versioonide vahel võib olla väga palju erinevaid sobitumisi, nii et võib juthuda, et kasutaja tahab proovida erinvaid tuumasid.

## Harjutus

<ol>
<li> Uurida välja enda operatsioonisüsteemi tuuma versioon.</li>
<li> Uurida erinevate saadaval olevate tuumade kohta</li>
</ol>

## Küsimus

Kuidas saab teada tuuma versiooni?

## Vastus
uname -r
