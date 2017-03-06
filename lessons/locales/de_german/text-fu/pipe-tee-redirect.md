# pipe und tee

## Inhalt der Lektion

Probiere folgenden Befehl aus:

<pre>$ ls -la /etc</pre>

Du wirst eine lange Liste mit vielen Dateien und Ordnern sehen. Da dies schwer zu lesen ist, wäre es doch geschickt die Ausgabe mit einem anderem Befehl wie less zu verknüpfen. Und das geht auch!

<pre>$ ls -la /etc | less </pre>

Das Verknüpfungssymbol | wird durch einen vertikalen Strich verwendet und lässt uns den stdout eines Befehl, zu einem stdin eines anderem Befehls machen. In diesem Fall verwendeten wir die Ausgabe von ls -la /etc und verknüpfen (<i>piped</i>) sie mit dem Befehl less. Dieser Befehl kann sehr nützlich sein.

Nun wollen wir die Ausgabe meines Befehls in zwei verschiedene Ströme schreiben. Das funktioniert mit dem Befehl tee:

<pre>$ ls | tee peanuts.txt</pre>

Du wirst die Ausgabe des Befehls sehen und wenn Du peanuts.txt öffnest, wird sich dort dieselbe Information befinden!

## Übung

Probiere folgenden Befehl aus:
<pre>$ ls | tee peanuts.txt banan.txt</pre>

## Quizfrage

Welches Symbol verwendest Du, um pipe aufzurufen?

## Quiz Antwort

|
