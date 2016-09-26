# pwd (Print Working Directory)

## Inhalt der Lektion

Alles in Linux ist eine Datei, während deiner Reise ins Innere von Linux wird dir das noch klarer werden. Jede Datei ist in einen hirarchischen Verzeichnisbaum einsortiert. Das erste Verzeichnis, das alle anderen beinhaltet heißt Wurzelverzeichnis (root directory). Das Wurzelverzeichnis beinhaltet einige Ordner und Dateien, die wiederum Ordner und Dateien enthalten usw. Hier ein Beispiel wie so ein Verzeichnisbaum aussieht:

<pre>/
|-- bin
|   |-- file1
|   |-- file2
|-- etc
|   |-- file3
|   `-- directory1
|       |-- file4
|       `-- file5
|-- home
|-- var
</pre>

Die Ortsangabe einer Datei oder eines Verzeichnisses nennt man Pfad. Wenn du einen Ordner namens home mit einem Ordner namens pete darin hast, indem sich wiederum ein Ordner namens Movies befindet, würde der Pfad folgendermaßen aussehen: `/home/pete/Movies`. Recht einfach, oder?

Wenn man im Verzeichnisbaum navigiert, ist es immer hilfreich zu wissen wo man sich gerade befindet und wo man sich hinbewegen möchte. Um zu sehen, wo man sich befindet, kann man das pwd Kommando verwenden. Der Befehl pwd steht für "print working directory", zu deutsch etwa "zeige Arbeitsverzeichnis". Dieser Befehl gibt also das Verzeichnis aus, in dem man sich gerade befindet. Es zeigt den Pfad beginnend beim Wurzelverzeichnis.

<pre>$ pwd</pre>

Wo bist du? Wo bin ich? Probiere es aus.

## Übung

Keine Übung für diese Lektion.

## Quizfrage

Mit welchem Befehl findest du das Verzeichnis heraus, in dem du gerade bist?

## Quiz Answer

pwd
