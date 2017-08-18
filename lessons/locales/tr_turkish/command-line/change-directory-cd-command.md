# cd (Change Directory)

## Ders İçeriği

Artık nerede olduğunuzu biliyorsunuz, şimdi dosya sisteminde biraz gezmeyi deneyelim. Bunun için yolları kullanmamız gerektiğini hatırlayın. Bir yol, mutlak veya bağıl olarak gösterilebilir.

<ul>
<li>Mutlak yol: Kök dizinden başlayarak yapılan yol gösterimidir. Kök dizini genellikle "/" şeklinde gösterilir. Yolunuz "/" ile başlıyorsa bu kök dizinden başlıyorsunuz demektir. Örnek, /home/sinan/Masaüstü.</li>

<li>Bağıl yol: Dosya sisteminde bulunduğunuz yerden yapılan yol gösterimidir. Mesela, /home/sinan/Dokümanlar klasöründesiniz ve Dokümanlar klasörü içindeki vergiler klasörüne geçmek istiyorsunuz, kök dizinden başlayarak /home/sinan/Dokümanlar/vergiler şeklinde tüm yolu yazmamıza gerek yok, bunun yerine sadece vergiler/ yazarak hedefimize ulaşabiliriz.</li>
</ul>

Artık yol mantığını kavradığımıza göre, bize istediğimiz dizine geçmemize yardımcı olacak bir şey lazım. Neyse ki, bu işi yapan cd (change directory) komutu var.

<pre>$ cd /home/sinan/Resimler</pre> 

Şimdi dizin konumunu /home/sinan/Resimler olarak değiştirdim.

Bu dizin içinde "Hawaii" adında bir klasör var, bu klasöre şu şekilde ulaşabilirim:

<pre>$ cd Hawaii</pre>

Zaten /home/sinan/Resimler klasöründe olduğum için sadece klasör adını kullandım.

Her zaman mutlak ve bağıl yolları kullanarak dosya sisteminde gezinmek epey yorucu olabilir, neyse ki işimiz kolaylaştıracak bazı kısayollar mevcuttur.

<ul>
<li>. (geçerli dizin). Şu an içinde bulunduğunuz dizindir. </li>
<li>.. (üst dizin). Sizi, içinde bulunduğunuz dizinin üstündeki dizine götürür.</li>
<li>~ (ev dizini). Ev dizini temsil eder. (örn. /home/sinan)</li>
<li>- (önceki dizin). Sizi, bulunduğunuz bir önceki dizine götürür.</li>
</ul>

<pre>$ cd .
$ cd ..
$ cd ~
$ cd -
</pre>
Bu örnekleri deneyelim!

## Alıştırma

<ol>
<li>Komutu parametresiz deneyin, sizi nereye götürüyor?</li>
</ol>

## Quiz

Eğer /home/sinan/Resimler klasöründeyseniz ve /home/sinan klasörüne gitmek istiyorsanız kullanmanız gereken komut nedir?

## Quiz Cevabı

cd ..