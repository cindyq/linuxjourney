# dhclient

## Tunni sisu

DHCP'd oleme juba tutvustanud. Enamasti ei ole kastuajatel tarvis IP aadresse, alamvõrgu maske ja muud käsitsi seadistada. Selleks ju ongi DHCP. dhclient käivitub alglaadimisel ning kasutab võrguliideste nimekirja saamiseks dhclient.conf faili. Selle nimekirja alusel püütakse kõiki liideseid seadistada DHCP protokolliga.

Liisitud IP aadresside kohta peab süsteemi taaskäivituste vahel järge dhclient.leases fail. Pärast dhclient.conf faili lugemist loetakse dhclient.leases faili, et tuvastada, kas mõnele liidesele on juba IP aadress liisitud.

<b>Uue IP aadressi saamine</b>

<pre>$ sudo dhclient</pre>

## Harjutus

Harjutust pole.

## Küsimus

Milline tööriist püüab määrata IP aadresse DHCP protokolliga?

## Vastus

dhclient
