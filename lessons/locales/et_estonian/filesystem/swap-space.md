# Saalimine

## Tunni sisu

Eelmises näites tutvustati partitsioonitabelit. Vaatame seda uuesti, aga nüüd täpsemalt seda rida:

<pre>
Number  Start   End     Size    Type      File system     Flags
 5      6861MB  7380MB  519MB   logical   linux-swap(v1)
</pre>

Mis on see *swap* ehk saaleala? Saaleala kasutatakse virtuaalmälule süsteemis ruumi eraldamiseks. Kui mälumahtu hakkab väheks jääma, kasutab süsteem seda kettajagu, et saalida sinna tegevusetute protsesside mälu "tükid". Nõnda ei saa mälu otsa.

<b>Kettajao kasutamine saalimiseks</b>

Ütleme, et soovime seada oma /dev/sdb2 partitsiooni saalealaks.

<ol>
<li>Esiteks tuleb teha kindlaks, et kettajaol ei asu midagi</li>
<li>Käivitada: mkswap /dev/sdb2 et inistialiseerida saalealad</li>
<li>Käivitada: swapon /dev/sdb2 mis lubab saaleseadme</li>
<li>Kui on soovitud, et saalealad püsiksid käivitamisel, on vaja lisada ka kirje /etc/fstab faili. Kasutada tuleb sw failisüsteemi tüüpi.</li>
<li>Saaleala eemaldamiseks: swapoff /dev/sdb2</li>
</ol>

Tavaliselt peaks määrama kaks korda nii palju ruumi saalealale, kui on mälu, kuid tänapäeva süsteemid on juba piisavalt võimsad, et RAM'ist täitsa piisab.

# Harjutus

Luua USB pulga vabale alale saaleala.

## Küsimus

Millise käsuga lubatakse seadmel saaleala?

## Vastus

swapon
