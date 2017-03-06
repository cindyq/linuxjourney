# stdout (Standard Out)

## Übungsinhalt

Bis jetzt haben wir uns an die vielen Kommandonamen und deren Output gewöhnt. Das bringt uns zum nächsten Thema: I/O (Input/Output) Streams. Führe einfach mal den folgenden Command aus und wir klären nachher, was er bewirkt.

<pre>$ echo Hello World > peanuts.txt</pre>

Was ist da gerade passiert? Prüfe mal das Verzeichnis in dem du diesen Command ausgeführt hast und siehe da, eine neue Datei namens peanuts.txt wurde erstellt. Wenn du jetzt denn Inhalt dieser Datei anschaust wirst du den Text "Hello World" sehen. Es ist gerade sehr viel passiert, wir schauen uns alles Schritt für Schritt an.

Der erste Teil im Detail:

<pre>$ echo Hello World</pre>

Wie wir wissen, wird damit Hello World auf den Bildschirm geschrieben. Aber wie? Prozesse nutzen I/O Streams (Ströme) um Input zu erhalten und Output zu generieren. Standardmässig nimmt der echo Command den Standartinput als Input, abgekürzt den stdin, von der Tastatur und gibt den Output standardmässig auf dem Bildschirm aus (stdout). Das ist also der Grund, weshalb echo Hello World einen Text Hello World auf den Bildschirm bringt. Das Tolle an der Sache ist, dass man diese Ströme nun umleiten kann und dadurch eine grossartige Flexibilität im Umgang mit Commands und Dateien erhält.

Schauen wir und den nächsten Teil des Commands an:

<pre> > </pre>

Das > ist ein Umleitungsoperator, welcher uns erlaubt, den Standard Output umzuleiten. Wir können damit den Output von echo Hello World in eine Datei umleiten anstatt auf den Bildschirm. Falls die Datei nicht schon existiert, wird sie für uns erstellt. Passe aber auf, denn falls die Datei schon existiert, wird sie einfach überschrieben (abhängig von der Shell die du benutzt, kannst du dies mit einem Flag verhindern).

Und das ist eigentlich das gesamte Prinzip, wie die stdout- Umleitung funktioniert.

Nun nehmen wir mal an, ich wollte die Datei peanuts.txt nicht überschreiben. Auch dafür gibt es einen Umleitungsoperator, und zwar >>:

<pre>$ echo Hello World >> peanuts.txt</pre>

Dies fügt den Text Hello World ans Ende von peanuts.txt. Auch hier wird die Datei zuerst erstellt, falls sie noch nicht existiert.

## Übung

Versuche ein paar Commands:

<pre>
$ ls -l /var/log > myoutput.txt
$ echo Hello World > rm
$ > somefile.txt 
</pre>

## Quizfrage

Welchen Umleitungsoperator benutzt du, um an das Ende einer Datei zu schreiben?

## Quiz Antwort

>>
