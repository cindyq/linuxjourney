# NetworkManager

## Tunni sisu

Kui käsitsi seadistamine ei ole kasutajale meelepärane, on olemas ka midagi selle jaoks, et võrk saaks üles ja töökorda automaatselt. Enamustes Linuxites on olemas deemon nimega NetworkManager, mis teeb just seda.

Kasutades graafilist kasutajaliidest võib NetworkManageri näha rakendusena töölaual. See haldab võrguga seotud riistvara ja ühendust puudutavat informatsiooni. Aglaadimisel kogub NetworkManager muuhulgas informatsiooni riistvara kohta, otsib juhtmega ja juhutmevabasid ühendusi ning aktiveerib ühenduse.

NetworkManageri kasutamiseks on olemas ka käsurea vahendid:

<b>nm-tool</b>

nm-tools raporteerib NetworkManageri oleku ja seadmed.

<pre>
pete@icebox:/$ nm-tool
NetworkManager Tool

State: connected (global)

- Device: eth0  [Wired connection 1] -------------------------------------------
  Type:              Wired
  Driver:            pcnet32
  State:             connected
  Default:           yes
  HW Address:        12:3D:45:56:7D:CC

  Capabilities:
    Carrier Detect:  yes

  Wired Properties
    Carrier:         on

  IPv4 Settings:
    Address:         192.168.22.1
    Prefix:          24 (255.255.255.0)
    Gateway:         192.168.22.2

    DNS:             192.168.22.2
</pre>

<b>nmcli</b>

nmcli käsk võimaldab kontrollida ja muuta NetworkManageri. Detailide kuvamiseks tasub vaadata man-lehekülgi.

## Harjutus

Harjutust pole.

## Küsimus

Millise käsuga kuvatakse NetworkManageri informatsioon?

## Vastus

nm-tool
