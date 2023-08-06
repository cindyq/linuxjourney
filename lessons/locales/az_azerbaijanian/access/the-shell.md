# The Shell

Qabıq nədir? Qabıq klaviaturadan əmrləri qəbul edən və icra üçün əməliyyat sisteminə göndərən proqramdır. Əgər siz heç vaxt GUI (qrafik istifadəçi interfeysi) istifadə etmisinizsə, "Terminal" və ya "Konsol" kimi proqramları görmüsünüz, bunlar sadəcə olaraq sizin üçün əmr qabığını işə salan proqramlardır. Bu kursda siz qabığın möcüzələrini öyrənəcəksiniz.

Bu kursda biz demək olar ki, bütün Linux paylamalarının standart olaraq daxil olduğu bash (Bourne Again shell) qabığından istifadə edəcəyik. Bundan başqa ksh, zsh, tsch kimi qabıqlar da var, lakin biz onları nəzərdən keçirməyəcəyik.

Gəlin birbaşa mətləbə keçək! Dağıtımdan (distribution), asılı olaraq, əmr qabığı dəyişə bilər, lakin əksəriyyəti aşağıdakı formata uyğun olacaq:

<pre>
username@hostname:current_directory

pete@icebox:/home/pete $
</pre>

Xəttin sonundakı $-işarəsiə ndiqqət yetirdinizmi? Fərqli qabığlarin fərqli göstərişləri var, bizim xalda $-işarəsi Bash, Bourne və ya Korn qabıqlarında - adi istifadəçi deməkdir, əmri yazarkən bu simvolu əlavə etməyə ehtiyac yoxdur, sadəcə bunun haqqında xəbərdar olun.

Gəlin <b>echo</b> adlı, sadə bir əmrlə başlayaq. Bu əmr sadəcə mətni ekrana çap edir.

<pre>
$ echo Hello World
</pre>

## Çalışma

Bəzi digər əmrləri yerinə yetirməyə çalışın və nə çıxardıqlarını görün:

<pre>
    <ol>
        <li>$ date</li>
        <li>$ whoami</li>
    </ol>
</pre>

### Test sual

echo Hello World yazdığınız zaman ekranda nə görünəcək?
