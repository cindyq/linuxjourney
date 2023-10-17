# Kabuk

## Ders İçeriği

Dünya sizin istiridyenizdir ya da aslında kabuk sizin istiridyenizdir. Kabuk nedir? Kabuk temel olarak komutlarınızı klavyeden alan ve bunları gerçekleştirmesi için işletim sistemine gönderen bir programdır. Daha önce grafik arayüze (GUI) sahip bir uygulama kullandıysanız, muhtemelen "Terminal" veya "Konsol" gibi programlar görmüşsünüzdür, bunlar sadece sizin için bir kabuk başlatan programlardır. Tüm bu kurs boyunca kabuğun harikalarını öğreneceğiz. 

Bu kursta bash (Bourne Again shell) kabuk programını kullanacağız, neredeyse tüm Linux dağıtımları varsayılan olarak bash kabuğunu kullanır. Ksh, zsh, tsch, fish gibi başka kabuklar da mevcuttur, ancak bunların hiçbirine girmeyeceğiz. 

Hemen başlayalım! Kullandığınız dağıtıma bağlı olarak kabuk isteminiz değişebilir, ancak çoğunlukla aşağıdaki biçime uymalıdır:
<pre>username@hostname:current_directory
pete@icebox:/home/pete $</pre>

Komut isteminin sonundaki $ işaretine dikkat ettiniz mi? Farklı kabukların farklı istemleri olacaktır, bizim durumumuzda $, Bash, Bourne veya Korn kabuğunu kullanan normal bir kullanıcı içindir, komutu yazarken istem (prompt) sembolünü eklemezsiniz, sadece orada olduğunu bilirsiniz.

Basit bir komutla başlayalım, echo. echo komutu sadece kendisine girdi olarak verilen metin değişkenlerini ekrana yazdırır.
<pre>$ echo Hello World</pre>

## Alıştırma

Diğer Linux komutlarını deneyin ve ne çıktı verdiklerine bakın:

<ol>
<li>$ date</li>
<li>$ whoami</li>
</ol>

## Quiz

echo Hello World yazdığınızda ekrana ne çıkmalıdır?

## Quiz Cevabı

Hello World
