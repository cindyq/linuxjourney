# Systemd ülevaade

## Tunni sisu

*Systemd* on tasapisi kerkimas esile *init*'i standardina. Kui kasutajal on arvutis olemas kataloog /usr/lib/systemd, siis kasutatakse kõige tõenäolisemalt just *systemd*'d.

*Systemd* kasutab süsteemi töökorras hoidmiseks eesmärke. Põhimõtteliselt on nii, et on olemas eesmärk, mida tahetakse saavutada aga sellel eesmärgil on ka sõltuvused, mis tuleb samuti täita. *Systemd* on väga paindlik ja robustne, see ei järgi protsesside käivitamisel ranget järjekorda. Tüüpilise *systemd* alglaadimise ajal toimub tavaliselt järgnev:

<ol>
<li>Esiteks laeb *systemd* konfiguratsioonifailid, mis asuvad tüüpiliselt kataloogis /etc/systemd/system või /usr/lib/systemd/system</li>
<li>Seejärel tehakse kindlaks alglaadimise sihtpunkt, mis on tavaliselt default.target</li>
<li>Süsteem selgitab välja sõltuvused ja aktiveerib need</li>
</ol>

Sarnaselt *Sys V* töötasemetele, võib *systemd* alglaadida erineva sihiga:

<ul>
<li>poweroff.target - lülita süsteem välja</li>
<li>rescue.target - üksiku kasutaja režiim</li>
<li>multi-user.target - mitu kasutajat ja võrk</li>
<li>graphical.target - mitu kasutajat, võrk ja graafiline kasutajaliides</li>
<li>reboot.target - taaskäivitus</li>
</ul>

Vaikimisi osutab default.target sihile graphical.target.

Peamised objektid, millega *systemd* opereerib on üksused. *Systemd* mitte ainult ei peata ja käivita protsesse vaid võib ka haakida külge failisüsteeme, jälgida võrgusokleid ja muud. Sellise robustsuse pärast opereeritaksegi erinevate üksustega. Kõige tavalisemad üksused on:

<ul>
<li>Teenuse üksused  - teenused, mida käivitatakse ja peatatakse, need failid lõpevad .service</li>
<li>Haakeüksused  - failisüsteemide haakimiseks, lõppevad .mount </li>
<li>Sihtmärgi üksused  - grupeerivad kokku teisi üksusi, faili lõpp on .target</li>
</ul>

Ütleme näiteks, et me alglaeme default.target. Sinna on kokku grupeeritud networking.service, crond.service ja teised üksused. Seega kui see üksus aktiveerida aktiveeruvad ka kõik talle alluvad üksused.

## Harjutus

Selles peatükis harjutust pole.

## Küsimus

Millist üksust kasutatakse, et grupeerida kokku teised üksused?

## Vastus

sihtmärgi
