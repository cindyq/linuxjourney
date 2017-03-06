# stderr (Standard Error)

## Inhalt der Lektion

Lass uns nun etwas anderes probieren, versuchen wir den Inhalt eines Verzeichnisses zu listen, welches gar nicht existiert und leiten den Output wieder in die peanuts.txt Datei.

<pre>$ ls /fake/directory > peanuts.txt </pre>

Du solltest folgendes sehen:

<pre>ls: cannot access /fake/directory: No such file or directory</pre>

Jetzt denkst du vielleicht, dass diese Nachricht in peanuts.txt geschrieben worden ist. Das ist aber nicht so. Es gibt nämlich noch einen anderen I/O Stream, der Standard error Stream (stderr). Standardmässig sendet dieser seinen Output auf den Bildschirm, sowie der stdout. Er ist aber komplett anders als stdout. Also muss auch dessen Output anders umgeleitet werden als der von stdout.

Unglücklicherweise ist der Umleitungsoperand nicht einfach <b>&lt;</b> oder <b>&gt;</b> aber er ist ziemlich ähnlich. Wir müssen Dateideskriptoren benützen. Ein Dateideskriptor ist eine positive Zahl, welche benutzt wird um auf Ströme oder Dateien zuzugreifen. Später werden wir genäuer darauf eingehen, jetzt musst du nur wissen, dass stdin 0, stdout 1 und stderr 2 als Dateideskriptor hat.

Wenn wir also unseren stderr zu der Datei umleiten möchten, können wir folgendes tun:

<pre>$ ls /fake/directory 2> peanuts.txt</pre>

Die Fehlermeldung steht jetzt in peanuts.txt.

Was ist, wenn ich den stdout und den stderr in peanuts.txt sehen möchte? Auch das kann man mit Dateideskriptoren lösen:

<pre>$ ls /fake/directory > peanuts.txt 2>&1</pre>

Der Output von ls /fake/directory wird an peanuts.txt gesendet und dann wird der stderr zum stdout mit 2>&1 umgeleitet. Es spielt eine Rolle, in welcher Reihenfolge die Operationen dastehen! 2>&1 sendet stderr zu dem Ort, wo stdout darauf zeigt. In diesem Fall zeigt stdout auf eine Datei, also leitet 2>&1 stderr auch auf eine Datei um. Wenn du also peanuts.txt liest, solltest du stderr und stdout Outputs sehen. Aber in diesem Beispiel wird sowieso nur ein Fehler produziert, deshalb wirst du nur die Fehlermeldung vorfinden.

Es gibt noch einen kürzeren Weg um stdout und stderr zu einer Datei umzuleiten:

<pre>$ ls /fake/directory &> peanuts.txt</pre>

Was ist nun, wenn ich den ganzen Müll nicht will und einfach alle stderr Nachrichten verschwinden sollen? Naja, du kannst den Output tatsächlich in den Mülleimer werfen, dafür gibt es die spezielle Datei namens /dev/null, welche jeglichen Input wegwirft.

<pre>$ ls /fake/directory 2> /dev/null</pre>

## Übung

Was tut der folgende Command:

<pre>$ ls /fake/directory >> /dev/null 2>&1</pre>

## Quizfrage

Was ist der Umleitungsoperator für stderr?

## Quizantwort

2>
