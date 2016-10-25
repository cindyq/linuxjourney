# kill (Peatamine)

## Tunni sisu

Protsessi peatamiseks saadetakse signaal, mida nimetatakse *kill*.

<pre>$ kill 12445</pre>

12445 on peatatava protsessi PID. Vaikimisi saadab see TERM signaali. SIGTERM saadetakse aga protsessile, et ta saaks rahulikult oma ressursid vabastada ja staatuse salvestada.

*Kill* käsuga saab signaali ka täpsustada:

<pre>$ kill -9 12445</pre>

See käivitab SIGKILL signaali ja peatab protsessi töö.

<b>Erinevused SIGHUP, SIGINT, SIGTERM, SIGKILL, SIGSTOP vahel?</b>

Need signaalid kõlavad kõik usna sarnaselt, kuid on siiski erinevad.

<ul>
<li>SIGHUP - saadetakse protsessilke kui kontrollterminal on suletud. Näiteks, kui sulgeda terminali aken, milles protsess alles töötas, siis saadetakse SIGHUP signaal.</li>
<li>SIGINT - See on vahelesegamise signaal. Kui sisestad klahvikombinatsiooni Crtl-C püüab süsteem graatsiliselt protsessi peatada.</li>
<li>SIGTERM - Peata protsess, aga lase tal enne korralikult enda järelt ära koristada</li>
<li>SIGKILL - Peata protsess, peata vahendeid valimata, mingist koristamisest pole juttugi</li>
<li>SIGSTOP - Peatab protsessi ajutiselt </li>
</ul>

## Harjutus

Peatada protsesse erinevate signaalidega.

## Küsimus

Milline on vaikimisi peatamise signaal?

## Vastus

SIGTERM

