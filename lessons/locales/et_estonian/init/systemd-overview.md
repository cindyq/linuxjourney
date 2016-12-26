# Systemd ülevaade

## Tunni sisu

*Systemd* on tasapisi kerkimas esile *init*'i standardina. Kui kasutajal on arvutis olemas kataloog */usr/lib/systemd* siis kasutatakse kõige tõenäolisemalt just *systemd*'d.

*Systemd* kasutab süsteemi töökorras hoidmiseks eesmärke. Põhimõtteliselt on nii, et on olemas eesmärk, mida tahetakse saavutada aga sellel eesmärgil on ka sõltuvused, mis tuleb samuti täita. *Systemd* on väga paindlik ja robustne, see ei järgi protsesside käivitamisel ranget järjekorda. Tüüpilise *systemd* alglaadimise ajal toimub tavaliselt järgnev:

<ol>
<li>Esiteks laeb <i>systemd</i> konfiguratsioonifailid, mis asuvad tüüpiliselt kataloogis <i>/etc/systemd/system/</i> või <i>/usr/lib/systemd/system</i></li>
<li>Seejärel tehakse kindlaks alglaadimise sihtpunkt, mis on tavaliselt <i>default.target</i></li>
<li>Süsteem selgitab välja sõltuvused ja aktiveerib need</li>
</ol>

Sarnaselt *Sys V* töötasemetele, võib *systemd* alglaadida erineva sihiga:

<ul>
<li><i>poweroff.target</i> - lülita süsteem välja</li>
<li><i>rescue.target</i> - üksiku kasutaja režiim</li>
<li><i>multi-user.target</i> - mitu kasutajat ja võrk</li>
<li><i>graphical.target</i> - mitu kasutajat, võrk ja graafiline kasutajaliides</li>
<li><i>reboot.target</i> - taaskäivitus</li>
</ul>

Vaikimisi osutab default.target sihile graphical.target.

Peamised objektid, millega *systemd* opereerib on üksused. *Systemd* mitte ainult ei peata ja käivita protsesse vaid võib ka haakida külge failisüsteeme, jälgida võrgusokleid ja muud. Sellise robustsuse pärast opereeritaksegi erinevate üksustega. Kõige tavalisemad üksused on:

<ul>
<li>Teenuse üksused  - teenused, mida käivitatakse ja peatatakse, need failid lõpevad <i>.service</i></li>
<li>Haakeüksused  - failisüsteemide haakimiseks, lõppevad <i>.mount</i> </li>
<li>Sihtmärgi üksused  - grupeerivad kokku teisi üksusi, faili lõpp on <i>.target</i></li>
</ul>

Ütleme näiteks, et me alglaadime default.target. Sinna on kokku grupeeritud *networking.service*, *crond.service* ja teised üksused. Seega kui see üksus aktiveerida aktiveeruvad ka kõik talle alluvad üksused.

## Harjutus

Selles peatükis harjutust pole.

## Küsimus

Millist üksust kasutatakse, et grupeerida kokku teised üksused?

## Vastus

sihtmärgi
