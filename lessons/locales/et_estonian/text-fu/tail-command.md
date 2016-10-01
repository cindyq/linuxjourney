# tail

## Tunni sisu

Sarnaselt head käsuga, laseb tail käsk sul vaadata vaikimis mingi faili viimast 10 rida.

<pre>$ tail /var/log/syslog</pre>

Just nagu head puhulgi, saad sa muuta, mitu rida kuvatakse.

<pre>$ tail -n 10 /var/log/syslog</pre>

Teine hea variant on kasutada -f (inglise keeles follow ehk järgi) lippu. See järgib faili, kui see peaks kasvama. Proovi ja vaata, mis juhtub.

<pre>$ tail -f /var/log/syslog</pre>

Kui sa kasutad oma süsteemi, muutub su syslog fail pidevalt. Tail -f käsu kasutamisega näed sa kõike, mida sinna faili parasjagu lisatakse.

## Harjutus

Vaata tail käsu man lehekülge ja uuri mõne käsu kohta, mida me ei tutvustanud.

<pre>$ man tail</pre>

## Küsimus

Millist lippu kasutakse faili jooksvaks jälgimiseks?

## Vastus

-f
