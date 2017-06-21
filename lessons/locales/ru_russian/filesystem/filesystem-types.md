# Filesystem Types

## Содержание урока

Существует множество различных реализаций файловой системы. Некоторые из них быстрее, чем другие, некоторые поддерживают хранилище большей емкости, а другие работают только на хранилище с меньшей емкостью. Различные файловые системы имеют разные способы организации своих данных, и мы подробно рассмотрим, какие типы файловых систем существуют. Поскольку существует так много различных реализаций, приложениям нужен способ справиться с различными операциями. Таким образом, есть что-то, что называется уровнем абстракции виртуальной файловой системы (VFS). Это слой между приложениями и разными типами файловой системы, поэтому независимо от того, какая файловая система у вас есть, ваши приложения смогут с ней работать. 

На ваших дисках может быть много файловой системы, в зависимости от того, как они разделены, и мы рассмотрим это на следующем уроке.

<b>Journaling</b>

Journaling происходит по умолчанию для большинства типов файловой системы. Предположим, вы копируете большой файл и внезапно теряете власть. Хорошо, если вы находитесь в не журнальной файловой системе, файл будет поврежден, и ваша файловая система будет непоследовательна, а затем при загрузке резервная копия ваша система проверит проверку файловой системы, чтобы убедиться, что все в порядке. Тем не менее, ремонт может занять некоторое время в зависимости от того, насколько велика ваша файловая система.

Теперь, если вы были в журналированной системе, прежде чем ваша машина даже начнет копировать файл, она напишет, что вы собираетесь делать в файле журнала. Теперь, когда вы фактически копируете файл, после его завершения журнал отмечает эту задачу как завершенную. Из-за этого файловая система всегда находится в постоянном состоянии, поэтому она точно знает, где вы остановились, если вы внезапно отключились. Это также уменьшает время загрузки, потому что вместо проверки всей файловой системы она просто смотрит на ваш журнал.

<b>Общие типы файловых систем</b>

<ul>
<li>ext4 - Это самая последняя версия родных файловых систем Linux. Он совместим со старыми версиями ext2 и ext3. Он поддерживает объемы дисков до 1 экзабайта и размер файлов до 16 терабайт и многое другое. Это стандартный выбор для файловых систем Linux.</li>
<li>Btrfs - «Better or Butter FS» - это новая файловая система для Linux, которая поставляется с моментальными снимками, инкрементными резервными копиями, повышением производительности и многое другое. Он широко доступен, но еще не вполне стабилен и совместим.</li>
<li>XFS - Высокопроизводительная журналируемая файловая система, отлично подходит для системы с большими файлами, таким как медиа-сервер.</li>
<li>NTFS and FAT - Файловые системы Windows</li>
<li>HFS+ - файловая система Macintosh</li>
</ul>

Проверьте, какие файловые системы находятся на вашем компьютере:

<pre>
pete@icebox:~$ df -T
Filesystem     Type     1K-blocks    Used Available Use% Mounted on
/dev/sda1      ext4       6461592 2402708   3707604  40% /
udev           devtmpfs    501356       4    501352   1% /dev
tmpfs          tmpfs       102544    1068    101476   2% /run
/dev/sda6      xfs       13752320  460112  13292208   4% /home
</pre>

Команда <b>df</b> сообщает об использовании дискового пространства файловой системы и других подробностях о вашем диске. Мы поговорим об этом инструменте позже.

## Задание

Прогуглите другие типы файловых систем: ReiserFS, ZFS, JFS и другие.

## Вопрос

Каков стандартный тип файловой системы Linux?

## Ответ

ext4