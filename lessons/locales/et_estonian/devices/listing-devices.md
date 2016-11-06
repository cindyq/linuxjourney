# lsusb, lspci, lssci, lsblk

## Tunni sisu

Just nagu *ls* kuvab nimekirja failidest ja kataloogidest, on olemas sarnased tööriistad ka seadmete jaoks.

<b> USB seadmete kuvamine</b>

<pre>$ lsusb </pre>

<b>PCI seadmete kuvamine</b>

<pre>$ lspci </pre>

<b>SCSI seadmete kuvamine</b>

<pre>$ lsscsi </pre>

Paigaldamiseks:
<pre>sudo apt update && sudo apt install lsscsi && sudo apt clean</pre>

<b>Plokkseadmete kuvamine</b>

<pre>$ lsblk</pre>

Vormindatud failisüsteeme näeb võtmega f:
<pre>$ lsblk -f</pre>

## Harjutus

Proovida kõiki õpitud käske ja tutvuda väljundiga.

## Küsimus

Millise käsuga saab kuvada usb seadmed?

## Vastus

lsusb
