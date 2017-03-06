# sort

## Inhalt der Lektion

Der Befehl sort hilft dabei, Zeilen zu sortieren.

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

Du kannst das ganze aber auch umdrehen (reverse):

<pre>$ sort -r file1.txt
elephant
dog
cow
cat
bird
</pre>

Oder aber auch nach dem Nummernwer sortieren:

<pre>$ sort -n file1.txt
bird
cat
cow
elephant
dog
</pre>

## Übung

Der Befehl sort wird erst wirklich nützlich, wenn Du ihn mit anderen Befehlen verknüpfst. Probiere den folgenden Befehl aus und finde heraus was passiert.

<pre>$ ls /etc | sort -rn</pre>

## Quizfrage

Welches Attribut verwendest Du, um den Befehl umzudrehen?

## Quiz Antwort

-r
