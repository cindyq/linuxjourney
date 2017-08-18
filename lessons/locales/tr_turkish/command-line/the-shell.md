# Kabuk

## Ders İçeriği

Kabuk ile sistemin tüm nimetleri elinin altında. Kabuk nedir? Kabuk temel olarak, klavyeden girilen komutları alıp çalıştırması için işletim sistemine gönderen bir programdır. Eğer daha önce bir grafik kullanıcı arayüzünde çalıştıysanız, muhtemelen "Terminal" veya "Console" gibi programlar görmüşsünüzdür, bunlar aslında size bir kabuk çalıştıran programlardır. Bu kursun tamamı boyunca kabuğun harikaları hakkında bilgi edineceğiz.

Bu kursta bash (Bourne Again Shell) kabuk programını kullanacağız, bash neredeyse tüm Linux dağıtımlarının varsayılan kabuk programıdır. ksh, zsh, tsch gibi başka kabuk programları da mevcuttur fakat biz bunların ayrıntısına girmeyeceğiz.

Hadi başlayalım! Dağıtımınıza bağlı olarak kabuk promptunuz değişebilir, ama çoğunlukla aşağıdaki biçime uymalıdır:
<pre>kullanıcıadı@bilgisayaradı:geçerli_dizin
pete@icebox:/home/pete $</pre>

Promptun sonundaki $ sembolünü farkettiniz mi? Farklı kabukların farklı promptları vardır, bizim örneğimizde $, Bash, Bourne, veya Korn kabuğunu kullanan normal kullanıcıları ifade eder. Komut yazarken prompt sembolünü koymanız gerekmez, sadece onun orada olduğunu bilin.

Hadi basit bir komutla, echo ile başlayalım. echo komutu, girilen metin argümanlarını ekrana yazdırır.

<pre>$ echo Merhaba Dünya</pre>

## Alıştırma

Diğer bazı Linux komutlarını deneyin ve çıktılarını görün:

<ol>
<li>$ date</li>
<li>$ whoami</li>
</ol>

## Quiz

echo Merhaba Dünya komutunun ekran çıktısı nedir? 

## Quiz Cevabı

Merhaba Dünya
