# kill (Peatamine)

## Tunni sisu

Protsessi peatamiseks saadetakse signaal, mida nimetatakse *kill*.

<pre>$ kill 12445</pre>

12445 on peatatava protsessi tunnus (PID). Vaikimisi saadab see TERM signaali. SIGTERM saadetakse aga protsessile, et ta saaks rahulikult oma ressursid vabastada ja oleku salvestada.

*Kill* käsuga saab signaali ka täpsustada:

<pre>$ kill -9 12445</pre>

See käivitab SIGKILL signaali ja peatab jõuga protsessi töö.

<b>Erinevused SIGHUP, SIGINT, SIGTERM, SIGKILL, SIGSTOP vahel?</b>

Need signaalid kõlavad kõik üsna sarnaselt kuid on siiski erinevad.

<ul>
<li>SIGHUP (1) - saadetakse protsessile kui kontrollterminal on suletud. Näiteks kui sulgeda terminali aken, milles protsess alles töötas, siis saadetakse SIGHUP signaal.</li>
<li>SIGINT (2) - See on vahelesegamise signaal. Kui sisestad klahvikombinatsiooni Crtl-C püüab süsteem viisakalt protsessi peatada.</li>
<li>SIGTERM (15) - Peata protsess aga lase tal enne korralikult enda järelt ära koristada</li>
<li>SIGKILL (9) - Peata protsess, peata vahendeid valimata, mingist koristamisest pole juttugi</li>
<li>SIGSTOP (19) - Peatab protsessi ajutiselt </li>
</ul>

Kõigi signaale ja nende numbrilisi väärtusi näeb näiteks kui paigaldada programm *htop* ja mõne protsessi peal vajutada F9 (katkestamiseks *ESC*).

## Harjutus

Peatada protsesse erinevate signaalidega.

## Küsimus

Milline on vaikimisi peatamise signaal?

## Vastus

SIGTERM

