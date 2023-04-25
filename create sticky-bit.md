# The Sticky Bit

## Dərs mövzusu

Sonda xususi icazə bit-i olan “the sticky bit” haqqında danışmaq istərdim.

Bu icazə bit- inin vəzifəsi  fayl və direktoriyaları möhkəmlətməkdir.( sticks a file/directory) Bu o deməkdir ki, yalnız proyektin sahibi (owner) və ya kök istifadəçi (the root user) faylı silə və ya redaktə edə bilər. Bu paylaşılan direktoriyalar (shared directories) üçün çox əlverislidir. Aşağıdakı nümunəyə diqqət edin:

<pre>$ ls -ld /tmp
drwxrwxrwxt 6 root root 4096 Dec 15 11:45 /tmp
</pre>

Siz sonda <b>t</b> xüsusi icazə bitini görəcəksiz. Bu xüsusi bit hər kəsin /tmp direktoriyasında fayl əlavə edə, fayl yaza, fayl redaktə edə biləcəyini , ancaq “the /tmp directory” direktoriyasının yalnız kök istifadəçi tərəfindən silinə biləcəyini göstərir.

<b>Modify sticky bit</b>

<pre>$ sudo chmod +t mydir

$ sudo chmod 1755 mydir</pre>

<b>1</b> sticky bit-in rəqəmsal göstəricisidir. 

## Çalışma

Daha hansı fayl və direktoriyalar  sticky bit- i aktivləşdirir?

## Quiz Question

Hansı simvol the sticky bit- i təyin edir?

## Quiz Answer

t
