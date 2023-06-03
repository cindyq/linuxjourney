# File Permissions

## Dərs Məzmunu

Daha əvvəl öyrəndik ki, faylların çeşidli izinləri və modları olur. Bu numunəyə baxaq:

<pre>$ ls -l Desktop/
drwxr-xr-x 2 pete penguins 4096 Dec 1 11:45 .
</pre>

Fayl icazələrinin üç hissəsi var. İlk hissə fayl çeşididir, bu fayl icazəsində ilk hərfdir və qovluq olduğu üçün <b>d</b> olaraq göstərilir.

Adi fayl üçün ən çox <b>-</b> görəcəksiniz. 

Digər hərflər isə icazələrinin özləridir və qruplaşdırılaraq hər biri 3 bit təskil edir.
İlk 3 bit istifadəçi, daha sonra qrup, ən son isə digər istifadəçilərin icazələri yer alır.

Asağıda daha rahat oxumaq üçün icazələr | ilə bölünüb.

<pre>d | rwx | r-x | r-x </pre>

Hər hərf fərqli icazəni təmsil edir:
<ul>
<li>r: readable - oxuma icazəsi</li>
<li>w: writable - yazma icazəsi</li>
<li>x: executable - çalışdırma icazəsi </li>
<li>-: empty - boş </li>
</ul>

Yuxarıda numunədən bilinir ki, pete adında istifadəçimizin oxuma, yazma və çalışdırma icazələri mövcuddur.
Penguins qupunun oxuma və yazma icazələri var.
Və nəhayət digər istifadəçilər (hərkəs) oxuma və çalışdırma icəzələrinə sahibdirlər.

## Çalışma

<pre> ls -l </pre> təlimatını bir neçə faylda istifadə edərək istifadəçi və qrup icazələrini izah edin.

## Quiz Question

Çalışdırma icazəsi üçün hansı hərf istifadə olunur?

## Quiz Answer

x
