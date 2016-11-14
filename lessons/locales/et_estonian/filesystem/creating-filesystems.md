# Failisüsteemide loomine

## Tunni sisu

Nüüd kui kettajagude loomine on seljataga, asume failisüsteemi looma.

<pre>$ sudo mkfs -t ext4 /dev/sdb2</pre>

Nii lihtne ongi! <b>mkfs</b> laseb kasutajal täpsustada soovitava failisüsteemi tüüpi ja asukohta. Failisüsteemi  luuakse asja loodud partitsiooni või vana partitsiooni ümberjaotamise tulemusel loodud partitsioonidele. Kui luua failisüsteem juba olemasoleva peale on tulemuseks kõigetõenäoliselt vigane failisüsteem.

## Harjutus

Teha USB pulgale ext4 failisüsteem.

## Küsimus

Millise käsuga luuakse failisüsteem?

## Vastus

mkfs
