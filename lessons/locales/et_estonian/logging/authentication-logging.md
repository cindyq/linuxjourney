# Autentimise logimine

## Tunni sisu

Autentimise logimine osutub väga kasulikusk kui tekivad probleemid kasutaja sisselogimisega.

<b>/var/log/auth.log</b>

Seal asuvad süsteemi autentimise logid, näiteks kasutaja sisselogimise ja autentimise meetod.

Väike katke näiteks:

<pre>
Jan 31 10:37:50 icebox pkexec: pam_unix(polkit-1:session): session opened for user root by (uid=1000)
</pre>

## Harjutus

Tekitada mõned ebaõnnestunud sisselogimiskatsed ja ka üks edukas. Seejärel vaadata faili /var/log/auth.log ja märgata, mis juhtus.

## Küsimus

Millist logi kasutatakse kasutajate autentimist puudutava informatsiooni jaoks?

## Vastus

auth.log
