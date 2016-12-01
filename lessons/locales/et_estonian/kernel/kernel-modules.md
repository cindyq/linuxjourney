# Tuuma moodulid

## Tunni sisu

Ütleme, et mul on uhke auto, ma olen sinna investeerimud palju aega ja raha. Lisan tagaspoileri, veokonksu, rattaraami ja veel igasuguseid asju. Need komponendd ei muuda tegelikult auto keskset toimimist ning ma võin neid lisada ja eemaldada väga lihtsalt. Tuum kasutab sama kontseptsiooni moodulitega.

Tuum iseenesest on üks monoliitne tükk tarkvara, kui me tahame lisada tuge uut tüüpi klaviatuurile, ei kirjuta me seda otse tuuma koodi. Jus nagu me ei keevita rattaraami auto külge (kes teab, vahest mõni inimene tahab seda teha). Tuuma mooduliud on tükid koodi, mida saab nõudmisel tuumale peale ja maha laadida. Moodulid lasevad meil laiendada tuuma funktsionaalsust ilma, et peaks päris sekkuma tuuma kesksesse koodi. Mooduleid saab lisada ka ilma süsteemi taaskäivitamata (enamustel juhtudel).

<b>Kuva nimekiri hetkel laetud moodulitest</b>

<pre>$ lsmod</pre>

<b>Lae moodul>/b>

<pre>$ sudo modprobe bluetooth</pre>

Kerneli moodulitel võivad samuti olla sõltuvused, modprobe laeb moodulite sõltuvused kui nad veel laetud ei ole.

<b>Mooduli eemaldamine</b>

<pre>$ sudo modprobe -r bluetooth</pre>

<b>Laadimine alglaadimisel</b>

Mooduleid saab laadida ka süsteemi alglaadimisel, selle asemel, et neid ajutiselt *modprobe* abil laadida (laetakse taaskäivitamisel jälle maha). Tuleb lihtsalt modigitseerida kataloogi <b>/etc/modprobe.d</b> ja lisada sinna sätete fail sedasi:

<pre>pete@icebox:~$ /etc/modprobe.d/maasikamoos.conf

options maasika_moos type=parim
</pre>

Natuke ebaraalne näide, kuid kui sul oleks moodul nimega maasika_moos ja sa tahaksid lisada tuuma parameetrid type=parim, saaksid sa seda laadida alglaadimisel selle sättefailiga. Olgu ära märgitud, et moodulitel on isiklikud tuuma paramteetrid, seega peaks lugema mooduli kohta, et nendest rohkem teada saada.

<b>Alglaadimisel mitte laadida</b>

Võib hoolitseda ka selle eest, et moodul kindlasti ei laeks alglaadimisel lisades sättefaili sedasi:

<pre>pete@icebox:~$ /etc/modprobe.d/maasikamoos.conf

blacklist maasika_moos
</pre>

## Harjutus

Eemalda modprobe abil bloetooth moodul ja vaata, mis juhtub. Kuidas seda uuest korda teha?

## Küsimus

Millise käsuga eemaldatakse moodul?

## Vastus

modprobe -r


