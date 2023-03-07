# File Permissions

## Dərs Məzmunu

Daha əvvəl öyrəndik ki, faylların çeşidli izinləri və modları olur. Bu numunəyə baxaq:

<pre>$ ls -l Desktop/
drwxr-xr-x 2 pete penguins 4096 Dec 1 11:45 .
</pre>

Fayl icazələrinin üç hissəsi var. İlk hissə fayl çeşididir, bu fayl icazəsində ilk hərf olaraq göstərilir.
burada göstərilən qovluq olduğu üçün <b>d</b> göstərilir.

Adi fayl üçün ən çox <b>-</b> görəcəksiniz. 

Digər fayl modunun hərfi isə icazələrinin özüdür.
İcazələrin qruplaşdırılıb hər biri 3 bit təskil edir.
İlk 3 bit istifadəçi icazələridir, daha sonra qrup icazələri gəlir, ən son ise digər istifadəçilərin icazələri yazılır.
Daha rahat oxumaq üçün | ilə icazələri bolmüşük.

<pre>d | rwx | r-x | r-x </pre>

Hər hərf fərqli icazəni təmsil edir:
<ul>
<li>r: readable - oxuma icazəsi</li>
<li>w: writable - yazma icazəsi</li>
<li>x: executable - çalışdırma icazəsi </li>
<li>-: empty - boş </li>
</ul>

Yuxarıda numunədən bilinir ki, pete adında istifadəçimizin oxuma, yazma və çalışdırma icazələri mövcuddur.
Penguins quppası oxuma və yazma icazələrinə sahibdir.
Və nihayi olaraq da, digər istifadəçilər (hərkər) oxuma və çalışdırma icəzələrinə sahiblər.

## Exercise

Use the ls -l command on multiple files and recite their permissions, user and group. 

## Quiz Question

What permission bit is used for executable? 

## Quiz Answer

x