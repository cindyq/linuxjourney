# pwd (Print Working Directory)

## Ders İçeriği

Linux'ta herşey bir dosyadır, Linux yolculuğunda ilerledikçe bunu anlayacaksınız ama şimdilik aklınızda bulunsun. Her dosya hiyerarşik dizin ağacı yapısında organize olmuştur. Dosya sistemindeki ilk dizin, hakettiği isimle, kök dizin olarak adlandırılır. Kök dizin altında, daha fazla klasör ve dosya vb. depolayabileceğiniz birçok klasör ve dosya bulunur. Aşağıdaki örnekte dizin ağacının neye benzediği görülmektedir:

<pre>/
|-- bin
|   |-- dosya1
|   |-- dosya2
|-- etc
|   |-- dosya3
|   `-- dizin1
|       |-- dosya4
|       `-- dosya5
|-- home
|-- var
</pre>

Dosyalar ve dizinlerin bulunduğu konumlara yol denir. Eğer home klasörünüz içinde sinan adında bir klasör ve bu klasör içinde de Filmler adında başka bir klasör olduğunu düşünürsek, yolumuz: /home/sinan/Filmler şeklinde olacaktır, oldukça basit değil mi?

Nerede olduğunuzu ve nereye gittiğinizi biliyorsanız, dosya sisteminin navigasyonu gerçek hayattaki gibi çok faydalıdır. Nerede olduğunuzu görmek için pwd komutunu kullanabilirsiniz. Bu komut, "çalışma dizinini yaz" (print working directory) anlamına gelir ve size o an içinde bulunduğunuz dizini gösterir. Bu arada, yolun kök dizin ile başladığına dikkat edin.

<pre>$ pwd</pre>

Neredesin? Neredeyim? Deneyin.

## Alıştırma

Bu ders için alıştırma yok.

## Quiz

Şu anda hangi dizinde bulunduğunuzu nasıl bulabilirim?

## Quiz Cevabı

pwd