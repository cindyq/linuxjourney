# NFS

## Tunni sisu

Kõite standartsem failide jagamise viis Linuxis on NFS (*Network File System* ehk võrgu failisüsteem). NFS võimaldab serveril jagada katalooge ja faile üle võrgu rohkem kui ühe kasutajaga.

NFS serveri loomise üksikasjadesse sellel kursusel ei süübita kuna see võib veidi keeruliseks minna, küll aga räägime NFS kliendi üles seadmisest.

<b>NFS kliendi üles seadmine</b>

<pre>$ sudo service nfsclient start
$ sudo mount server:/kataloog /haagitav_kataloog</pre>

<b>Automaatne haakimine</b>

Ütleme, et NFS server on üsna tihti kasutuses ning kasutaja soovib, et see oleks jäädavalt külge haagitud. Tavaliselt võiks mõelda, et tuleb muuda /etv/fstab faili, kuid alati ei pruugi õnnestuda saada serveriga ühendust ja see võib tekitada alglaadimisel probleeme. Selle asemel tasuks üles seada automaatne haakimine. Seda tehakse <b>automount</b> tööriistaga, uuemates Linuxi versioonides <b>amd</b>. Kui mõnele täpsustatud kataloogile püütakse ligi pääseda otib automount üles vastava serveri ja haagib selle automaatselt külge.

## Harjutus

Lugeda NFS'i man-lehekülge, et selle kohta rohkem teada saada.

## Küsimus

Millise tööriistaga hallatakse automaatseid haakepunkte?

## Vastus

automount
