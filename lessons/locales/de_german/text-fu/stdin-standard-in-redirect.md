# stdin (Standard In)

## Übungsinhalt

In der vorangegangenen Lektion lernten wir, dass es verschiedene Output Streams gibt, die wir benutzen können (Bildschirm, Dateien, ...). Es gibt aber auch verschiedene Standard Inputs (stdin) die wir benutzen können. Wir wissen, das zum Beispiel ein Gerät ein stdin sein kann, die Tastatur zum Beispiel. Aber auch Dateien, Output von anderen Prozessen und von der Shell können genau so den Input eines Prozesses sein. Shau dir folgendes Beispiel an:

Benutzen wir doch nochmals die peanuts.txt Datei von der vorangegangenen Lektion. Weisst du noch, dass Hello World darin stand?

<pre>$ cat <b>&lt;</b> peanuts.txt <b>&gt;</b> banana.txt </pre>

Genau so wie wir <b>&gt;</b> für stdout Umleitung hatten, können wir <b>&lt;</b> für die stdin Umleitung benutzen.

Normalerweise gibst du dem cat Command eine Datei mit, diese Datei wird der stdin. Oben haben wir also gerade peanuts.txt so umgeleitet, dass es unser stdin wird. Der Output von peanuts.txt, der einfach Hello World wäre, wird in eine neue Datei namens banana.txt umgeleitet.

## Übung

Teste ein paar Commands aus:
<pre>
$ echo <b>&lt;</b> peanuts.txt <b>&gt;</b> banana.txt
$ ls <b>&lt;</b> peanuts.txt <b>&gt;</b> banana.txt
$ pwd <b>&lt;</b> peanuts.txt <b>&gt;</b> banana.txt
</pre>

## Quizfrage 

Welchen Umleitungsoperator benutzt du, um stdin umzuleiten?

## Quizantwort 

<
