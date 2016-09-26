# regex (Regular Expressions, reguläre Ausdrücke)

## Inhalte der Lektion

Reguläre Ausdrücke sind sehr mächtig, wenn man eine musterbasierte Selektion an einem Text vornehmen will. Spezielle Zeichen erlauben, ein solches Muster zu bauen. Die *-Wildcard haben wir ja schon kennengelernt.

In dieser Lektion werden wir die gängigsten Ausdrücke kennenlernen, du kannst sie auch in fast allen Programmiersprachen verwenden.

Das ist unser Test-String:
<pre>
Sally verkauft Muscheln
an der Meeresküste
</pre>

<b>1. Beginn einer Linie mit ^</b>

<pre>
<b>^</b>an
würde passen zur Linie "an der Meeresküste"
</pre>

<b>2. Ende einer Linie mit $</b>

<pre>
Meeresküste<b>$</b>
würde zur Linie "an der Meeresküste" passen
</pre>

<b>3. Jeder beliebige Buchstabe wird beschrieben durch ein .</b>

<pre>
a<b>.</b>
würde passen zu "an"
</pre>

<b>4. Klammerausdrücke mit [] und ()</b>

Das kann ein bisschen knifflig sein. Die eckige Klammer erlaubt uns, eine Buchstabenauswahl anzugeben.

<pre>
f<b>[ei]</b>nster
würde passen zu: fenster, finster
</pre>

Der vorher genannte Anker-Tag ^ in einer solchen Klammer meint "alles ausser" die Buchstaben in der Klammer.

<pre>
Sch<b>[^i]</b>le
würde passen zu: Schule, Schale, aber nicht Schile. Das Beispiel ist ein bisschen schlecht, da auch Schkle erlaubt ist, aber ich hoffe du verstehst den Punkt.
</pre>

Man kann ein Buchstabenset auch einfacher angeben.

<pre>
d<b>[a-c]</b>g
würde zu Mustern wie dag, dbg, and dcg passen.
</pre>

Passe aber auf, bei den Ausdrücken wird immer unterschieden zwischen Gross- und Kleinbuchstaben:

<pre>
d<b>[A-C]</b>g
passt zu dAg, dBg und dCg aber nicht dag, dbg und dcg
</pre>

Das waren ein paar Basics.
## Übung

Probiere eine Regex mit grep zu kombinieren und durchsuche einige deiner Dateien.

<pre>
grep [hier kommt die Regex] [Datei]

## Quizfrage

Welche Regex würdest du nehmen, um genau einen Buchstaben zu beschreiben?

## Quizantwort

.
