# sort

## Inhalte der Lektion

Der sort command wird verwendet um Linien zu sortiern.

<pre>
file1.txt
dog
cow
cat
elephant
bird

$ sort file1.txt
bird
cat
cow
dog
elephant
</pre>

Folgendermassen würdest du eine umgekehrte (reversed, -r) Sortierung vornehmen:

<pre>$ sort -r file1.txt
elephant
dog
cow
cat
bird
</pre>

Und auch mit nummerischen Werten kann man sortieren:

<pre>$ sort -n file1.txt
bird
cat
cow
elephant
dog
</pre>

## Übung

Die Stärke von sort kommt erst zum Vorschein, wenn man den Befehl mit anderen Befehlen kombiniert. Probiere folgenden Befehl aus und schaue was passiert:

<pre>$ ls /etc | sort -rn</pre>

## Quizfrage

Welches Flag benutzt du um eine umgekehrte Sortierung vorzunehmen?

## Quizantwort

-r
