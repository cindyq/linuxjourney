# Umask

## Dərs Məzmunu

Yaradılan hər fayl, standart icazələr ilə yaradılır. Standart icazələri dəyişdirmək üçün, umask təlimatın istifadə olunur.
Bu təlimat digər rəqəmsal icazələrdə olunduğu kimi 3 bit dəyər qəbul edir.
Lakin umask verilən 3 bit dəyəri icazəyə əlavə etmir, tam tərsinə verilən dəyər qədər icazəni azladır. 

<pre>$ umask 021</pre>

Verilən nümunədə, biz artıq yeni yaradılacaq olan faylda istifadəçiyə tam icazəni qoruyuruq, qruplar üçün yazma icazəsini, digərləri üçün isə icra etmə icazəsini ləğv edirik.

Paylama dəstlərinin (Distribution) çoxunda standart olaraq umask 022 dəyəri istifadə olunur, 
bu o deməkdir ki, istifadəçiyə tam icazə verilir, qruplara və digər istifadəçilərə isə yazma icazəsi verilmir.

Umask təlimatını daxil etdiyimizdə yeni yaradılacaq fayllar üçün yeni icazələri bizə göstəriləcək.
Bu icazə dəyərlərini qeyd etmək üçün başlanğıç faylı da (.profile) dəyişdirməyimiz lazımdır, lakin bu başqa dərsin mövzusudur.  


## Çalışma

<ol>
<li>Yeni bir fayl yaradın və onun icazələrini qeyd edin</li>
<li>Umask təlimatı ilə icazələri dəyişdirin</li>
<li>Yaradılan fayl üçün icazələri yenidən yoxlayın, nə dəyişdi?</li>
<ol>

## Quiz Question

Faylların standart icazələrini dəyişdirmək üçün hansı təlimat istifadə olunur?

## Quiz Answer

umask
