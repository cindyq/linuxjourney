# stderr (Standard Fehler)

## Inhalt der Lektion

Lass uns jetzt etwas anderes ausprobieren. Wir versuchen den Inhalt eines Ordners, der nicht existiert, in eine Datei auszugeben.

<pre>$ ls /fake/directory > peanuts.txt </pre>

Du solltest folgendes sehen.

<pre>ls: cannot access /fake/directory: No such file or directory</pre>

Nun sollte diese Nachricht auch in die Datei geschrieben werden, oder? Dafür gibt es aber einen anderen I/O Strom mit dem Namen Standard Fehler (stderr). Normalerweise wird die Ausgabe von stderr ausgegeben, da es ein anderer Strom ist als stdout. Nun müssen wir die Ausgabe also umleiten.

Leider ist das nicht einfach mit <b>&lt;</b> oder <b>&gt;</b> möglich. Wir müssen eine kleine Erweiterung, in Form einer Zahl, verwenden. Die Erweiterungen für stdin, stdout und stderr sind 0, 1 und 2.

Wenn wir jetzt die Ausgabe von stderr in eine Datei schreiben wollen, können wir das wie folgt tun:

<pre>$ ls /fake/directory 2> peanuts.txt</pre>

Jetzt solltest Du die Fehlernachricht in der Datei peanuts.txt vorfinden.

Nun möchte ich stderr und stdout in die Datei peanuts.txt schreiben. Dies ist mit Erweiterungen, wie folgt möglich:

<pre>$ ls /fake/directory > peanuts.txt 2>&1</pre>

Dies schickt die Ausgabe, durch die Erweitung 2>&1, von ls /fake/directory und stderr in den Strom stdout. Hierbei ist die Reihenfolge der Erweiterungen wichtig, da 2>&1 die Ausgabe von stderr zu dem Zielort, auf den stdout zeigt, geschickt wird. In diesem Fall zeigt stdout auf eine Datei und so wird stderr in eine Datei geschickt. Wenn wir jetzt peanuts.txt öffnen, solltest Du stderr und stdout sehen. In unserem Fall gibt der Befehl aber nur stderr zurück.

Es gibt aber auch eine kürzere Methode, um beide Ströme in eine Datei zu schreiben:

<pre>$ ls /fake/directory &> peanuts.txt</pre>

Was ist also, wenn ich die Fehlernachrichten überhaupt nicht mehr erhalten möchte? Wir können die Ausgabe auch in eine spezielle Datei mit dem Namen /dev/null schicken, damit sie sofort wieder gelöscht wird.

<pre>$ ls /fake/directory 2> /dev/null</pre>

## Übung

Was macht folgender Befehl?

<pre>$ ls /fake/directory >> /dev/null 2>&1</pre>

## Quizfrage

Wie lautet die Erweitung für stderr?

## Quiz Antwort

2>
