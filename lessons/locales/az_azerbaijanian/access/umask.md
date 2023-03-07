# Umask

## Dərs Məzmunu

Yaradılan hər fayl, standart icazələr ilə yaradılır. Əgər ki bu standart icazələri dəyişdirmək istəyirsiniz isə bu umask təlimatı ilə mümkündür.
Bu təlimatda da rəqəmsal icazələrdə olunduğu kimi 3 bit dəyər qəbul edir.
Lakin bu icazələri əlavə eləmək yerinə, umask bu icazələri götürür.

<pre>$ umask 021</pre>

Verilən numunədə, biz yeni yaradılacaq olan fayllda artıq istifadəçilərə tam izin, 
gruplar üçün yazmaq icazəsini ləğv edirik digərləri üçün isə icra etmək icazəsini ləğv edirik.

Distrubutionların çoxunda standart olaraq umask 022 dəyəri istifadə olunur, 
bu deməkdir ki istifadəçi üçün tam izin, lakin gruppalara və digər istifadəçilərə yazmaq icazəsi verilmir.

Umask təlimatını daxil elədiyimizdə yeni yaradılacaq fayllar üçün yeni icazələri bizə göstərəcək.
Lakin, bu icazə dəyərlərini qeyd eləmək üçün başlanğıç fayl da (.profile) dəyişdirməmiz lazımdır, ancaq bu basga bir dərsin mövzusudur.  


## Çalışma

<ol>
<li>Yeni bir fayl yaradın və onun icazələrini qeyd edin</li>
<li>Umask təlimatı ilə icazələri dəyişdirin</li>
<li>Createm a new file, then note it's permissions.</li>
<li>Yaradılan fayl üçün icazələri yenidən yoxlayın, nə dəyişdi?</li>
<ol>

## Quiz Question

Faylların standart icazələrini deyişdirmək üçün hansı təlimat istifadə olunur?

## Quiz Answer

umask
