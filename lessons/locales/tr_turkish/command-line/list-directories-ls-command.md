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

<pre>pete@icebox:~$ ls -l
total 80
drwxr-x--- 7 pete penguingroup   4096 Nov 20 16:37 Desktop
drwxr-x--- 2 pete penguingroup   4096 Oct 19 10:46  Documents
drwxr-x--- 4 pete penguingroup   4096 Nov 20 09:30 Downloads
drwxr-x--- 2 pete penguingroup   4096 Oct  7 13:13   Music
drwxr-x--- 2 pete penguingroup   4096 Sep 21 14:02 Pictures
drwxr-x--- 2 pete penguingroup   4096 Jul 27 12:41   Public
drwxr-x--- 2 pete penguingroup   4096 Jul 27 12:41   Templates
drwxr-x--- 2 pete penguingroup   4096 Jul 27 12:41   Videos</pre>

Commands have things called flags (or arguments or options, whatever you want to call it) to add more functionality. See how we added -a and -l, well you can add them both together with -la. The order of the flags determines which order it goes in, most of the time this doesn’t really matter so you can also do ls -al and it would still work.

<pre>$ ls -la</pre>

## Alıştırma

ls komutunu farklı parametrelerle deneyip komut çıktılarını inceleyin. 

## Quiz

Gizli dosyaları görmek için hangi komut kullanılır?

## Quiz Cevabı

ls -a