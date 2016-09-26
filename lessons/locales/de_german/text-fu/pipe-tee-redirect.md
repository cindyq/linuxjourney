# pipe and tee

## Inhalt der Lektion

Lernen wir ein bisschen Sanitärskunst. Gib mal folgenden Command ein:

<pre>$ ls -la /etc</pre>

Sieht nach einer sehr langen Liste aus, nicht? Eigentlich kann man diese nur schlecht lesen. Wäre es nicht super, wenn wir den Output von ls in einem anderen Command wie zum Beispiel less sehen könnten? Dann hätten wir nicht so viel Text auf einmal. Natürlich geht das!

<pre>$ ls -la /etc | less </pre>
Der Pipe Operator (pipe = Rohr), eine vertikale Linie |, erlaubt uns den stdout eines Commands zum stdin eines anderen Prozesses zu machen. In diesem Fall haben wir den stdout von ls -la /etc (was ja diese lange Liste ausgegeben hat) zum less Command <i>gepiped (umgeleitet)</i>. Der Pipe Operator ist sehr nützlich und wir werden ihn bis in alle Ewigkeit gebrauchen.

Ich kann damit auch den Output meines Commands auf zwei unterschiedliche Streams verteilen:

<pre>$ ls | tee peanuts.txt</pre>

Der Output sollte nun auf dem Bildschirm erscheinen, aber auch in der peanuts.txt Datei.

## Übung 

Probiere den folgenden Command aus:
<pre>$ ls | tee peanuts.txt banan.txt</pre>

## Quizfrage 

Welches Zeichen repräsentiert den Pipe Operator?

## Quizantwort 

|
