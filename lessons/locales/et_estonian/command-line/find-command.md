# find

## Tunni sisu

Meil on süsteemis palju faile ning nendest ühe konkreetse leidmine võib muutuda veidi keeruliseks. Saame selle jaoks kasutada käsku find!

<pre>$ find /home -name kutsikad.jpg</pre>

Kui kasutad find käsku, pead täpsustama, millisest kataloogist tuleb faili otsida. Praegusel juhul otsime faili nime (name) kutsikad.jpg järgi.

Sa võid ka täpsustada, millist tüüpi faili sa leida püüad.

<pre>$ find /home -type d -name MinuKaust</pre>

Nagu märkasid, siis ma panin faili tüüpbiks d (kataloogi jaoks) ning samal ajal ma otsin endiselt nime järgi MinuKaust.

Lahe asi, mida silmas pidada, on see, et find ei piirdu otsimisega täpsustatud kataloogist, see otsib ka kõikvõimalikest alamkataloogidest.

## Harjutus

<ol>
<li>Leia juurkataloogist fail, mille nimes on sõna net.</li>
</ol>

## Küsimus

Kuidas pean find käsku täpsustama, kui tahan otsida faili nime järgi?

## Vastus

-name
