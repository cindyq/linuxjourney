# stdin (Standard Eingabe)

## Inhalt der Lektion

In der letzten Lektion haben wir gelernt, dass wir verschiedene stdout Ströme, wie in eine Datei schreiben oder normal ausgeben, verwenden können. Aber es gibt auch unterschiedliche Standard Eingaben (stdin), die wir verwenden können. Eine Eingabe kann man durch die Tastatur machen, aus einer Datei lesen oder die Ausgabe eines Prozesses verwenden.

Verwenden wir die Datei peanuts.txt. Sie enthielt den Text Hello World.

<pre>$ cat <b>&lt;</b> peanuts.txt <b>&gt;</b> banana.txt </pre>

So, wie wir <b>&gt;</b> bei stdout hatten, können wir auch <b>&lt;</b> bei stdin verwenden.

Normalerweise verwendet man den Befehl cat, indem man eine Datei zu ihm schickt, welches zur Eingabe wird.In diesem Fall machen wir peanuts.txt zu unserer Eingabe. Dann wird die Ausgabe aus peanuts.txt in eine andere Datei mit dem Namen banata.txt weitergeleitet.

## Übung

Probiere ein paar Befehle aus:
<pre>
$ echo <b>&lt;</b> peanuts.txt <b>&gt;</b> banana.txt
$ ls <b>&lt;</b> peanuts.txt <b>&gt;</b> banana.txt
$ pwd <b>&lt;</b> peanuts.txt <b>&gt;</b> banana.txt
</pre>

## Quizfrage

Welches Zeichen verwendest für eine stdin Eingabe?

## Quiz Answer

<
