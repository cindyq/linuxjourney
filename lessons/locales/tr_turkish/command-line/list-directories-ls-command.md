# ls (List Directories)

## Ders İçeriği

Artık dosya sisteminde nasıl dolaşacağımızı biliyoruz, peki etrafımızda neler olduğunu nasıl göreceğiz, çünkü şu an karanlıkta yürüyor gibiyiz. Evet, dizin içeriklerini listelemek için ls komutunu kullanabiliriz. ls komutu, varsayılan olarak geçerli dizin içindeki dizin ve dosyaları listeler, bununla birlikte dizinlerini listelemek istediğiniz yolu belirtebilirsiniz. 
<pre>$ ls
$ ls /home/sinan</pre>

ls oldukça kullanışlı bir araçtır, ayrıca baktığınız dosya ve dizinler hakkında size ayrıntılı bilgi sunar. 

Bu arada bir dizindeki tüm dosyaların görünmeyeceğini unutmayın. "." ile başlayan dosya isimleri gizlidir, ancak bunları ls komutunu -a (all)parametresiyle kullanarak görüntüleyebilirsiniz. 

<pre>$ ls -a</pre>

Ayrıca ls komutunun, dosyaların detaylı listesini uzun bir düzende gösteren -l (long) şeklinde kullanışlı bir başka parametresi daha vardır. Bu size, soldan başlayarak: dosya izinleri, link sayısı, sahip ismi, sahip grubu, dosya boyutu, dosyanın son değişim tarihi bilgisi ve dosya/dizin ismi gibi ayrıntılı bilgileri gösterecektir.

<pre>$ ls -l</pre>

<pre>sinan@ayasofya:~$ ls -l
total 80
drwxr-x--- 7 sinan penguingroup   4096 Kas 20 16:37 Masaüstü
drwxr-x--- 2 sinan penguingroup   4096 Eki 19 10:46 Dokümanlar
drwxr-x--- 4 sinan penguingroup   4096 Kas 20 09:30 İndirilenler
drwxr-x--- 2 sinan penguingroup   4096 Eki  7 13:13 Müzik
drwxr-x--- 2 sinan penguingroup   4096 Eyl 21 14:02 Resimler
drwxr-x--- 2 sinan penguingroup   4096 Tem 27 12:41 Ortak
drwxr-x--- 2 sinan penguingroup   4096 Tem 27 12:41 Şablonlar
drwxr-x--- 2 sinan penguingroup   4096 Tem 27 12:41 Videolar</pre>

Komutlar parametre adı verilen argümanlarla (veya seçeneklerle) daha fazla işlevsellik kazanırlar. -a ve -l parametrelerini nasıl eklediğimizi inceleyin, parametreleri -la şeklinde bitişik de yazabilirsiniz. Parametrelerin yazılış sırası, işletilme sırasını belirler ama genelllikle bu sıranın önemi yoktur, ls -al komutu da aynı sonucu verecektir.

<pre>$ ls -la</pre>

## Alıştırma

ls komutunu farklı parametrelerle deneyip komut çıktılarını inceleyin. 

## Quiz

Gizli dosyaları görmek için hangi komut kullanılır?

## Quiz Cevabı

ls -a
