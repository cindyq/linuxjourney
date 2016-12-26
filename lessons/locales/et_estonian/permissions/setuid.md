# Setuid

## Tunni sisu

Päris paljudes olukordades võib tavakasutajal vaja olla kõrgendatud ligipääsu mingitele andmetele ja süsteemi administraator ei saa alati joosta kohale, et juurkasutaja salasõna sisestada. Kuid õnneks on olemas spetsiaalsed ligipääsuõiguste bitid, mis aitavad seda probleemi lahendada. *Set User ID* (SUID) ehk kasutaja ID seadmine võimaldab kasutaja asemel käivitada programmi selle omaniku õigustest.

Vaatame näidet:

Ütleme, et tahan muuta oma salasõna. Lihtne eks? Kasutan lihtsalt *passwd* käsku:

<pre>
$ passwd
</pre>

Mida see käsk teeb? See mudab mõnda faili, kuid kõige olulisem on, et see muudab /etc/shadow faili. Vaatame seda korraks:

<pre>
$ ls -l /etc/shadow


-rw-r----- 1 root shadow 1134 Dec 1 11:45 /etc/shadow

</pre>

See fail on ju aga juurkasutaja omanduses! Kuidas on mul võimalik muuta faili, mille omanik on juurkasutaja?

Vaatame veel ühte õiguste komplekti, see kord sisestatud käsu oma:

<pre>
$ ls -l /usr/bin/passwd


-rwsr-xr-x 1 root root 47032 Dec 1 11:45 /usr/bin/passwd
</pre>

Võib märgata, et õigus on seal <b>s</b>. See õiguste bit on SUID, mille olemasolul failiõigustes lubab see käivitajal võtta faili omaniku, meie näites juurkasutaja, õigused, sealhulgas käivitamise õiguse. Seega tegelikkuses, kui sisestada passwd käsk, käivitatakse see juurkasutajana.

Seetõttu ongi võimalik pääseda passwd käsuga ligi kaitstud failidele nagu /etc/shadwo. Kui see bit eemaldada on kohe selge, et vastavat faili muuta ei saa ja salasõna jääb samuti muutmata.

<b>SUID muutmine</b>

Sarnaselt teistele õigustele, saab SUID õigusi ka muuta kahte moodi.

*Sümboliline viis:*

<pre>
$ sudo chmod u+s minufail
</pre>

*Numbriline viis:*

<pre>
$ sudo chmod 4755 minufail
</pre>

Nagu näha tähistab SUID'd number 4 ja see lisatakse teiste õiguste ette. SUID võib olla märgitud ka kui suurtäht <b>S</b>, see tähistab sama asja, kuid ei hõlma endas käivitamise õigust.

## Harjutus

Vaadata /etc/passwd õigusi detailselt. Mida veel võib märgata? Failid, millele on seatud SUID on teistest kergesti eristatavad.

## Küsimus

Milline number tähistab SUID'd?

## Vastus

4
