# wc ja nl

## Tunni sisu

wc (inglise keele word count ehk sõnade loendus) käsk kuvab faili täieliku sõnade hulga.

<pre>$ wc /etc/passwd
 96     265    5925 /etc/passwd
</pre>

Vastavalt väljundile on kuvatud ridade, sõnade ja vaitide arv.

Selleks, et ainult ühte välja kuvataks, kasuta vastavalt -l, -w või -c.

<pre>$ wc -l /etc/passwd
96</pre>

Veel üks käsk, millega saab faili ridade arvu teada, on nl (number lines ehk ridade number).

<pre>
fail1.txt
mulle
meeldivad
kilpkonnad
</pre>

<pre>$ nl file1.txt
1. mulle
2. meeldivad
3. kilpkonnad
</pre>

## Harjutus

Kuidas sa saaksid nl käsku kasutades faili lõpliku ridade arvu ilma, et peaksid kogu väljundil läbi vaatama? Vihje: Kasuta mõningaid teisi käske, mida sellel kursusel juba õppinud oled.

## Küsimus

Millist käsku kasutaksid, et saada failist ainult lõplik sõnade arv.

## Vastus

wc -w
