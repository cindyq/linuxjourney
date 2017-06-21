# Типы устройств

## Содержание урока

Прежде чем мы поговорим о том, как управляются устройства, давайте взглянем на некоторые устройства.

<pre>$ ls -l /dev
brw-rw----   1 root disk      8,   0 Dec 20 20:13 sda
crw-rw-rw-   1 root root      1,   3 Dec 20 20:13 null
srw-rw-rw-   1 root root           0 Dec 20 20:13 log
prw-r--r--   1 root root           0 Dec 20 20:13 fdata
</pre>

Столбцы выглядят следующим образом слева направо:

<ul>
<li>Разрешения</li>
<li>Владелец</li>
<li>Группа</li>
<li>Основной номер устройства</li>
<li>Незначительный номер устройства</li>
<li>Отметка времени</li>
<li>Имя устройства</li>
</ul>

Помните, что в команде ls вы можете увидеть тип файла с первым битом в каждой строке. Файлы устройств обозначаются следующим образом:

<ul>
<li>c - символ</li>
<li>b - блок</li>
<li>p - канал(пайп)</li>
<li>s - сокет</li>
</ul>

<b>Символьное устройство</b>

Это устройство передаёт данные, но по одному символу за раз. Вы увидите множество псевдоустройств (/dev/null) в качестве символьных устройств, эти устройства физически не подключены к машине, но они позволяют операционной системе быть функциональной.

<b>Блок устройство</b>

Эти устройства передают данные, но в больших блоках фиксированного размера. Чаще всего вы увидите устройства, которые используют блоки данных в качестве блочных устройств, таких как жесткие диски, файловые системы и т.д. 

<b>Канальные устройство</b>

Именованные каналы позволяют двум или более процессам взаимодействовать друг с другом, они похожи на символьные устройства, но вместо того, чтобы выводить данные на устройство, они отправляются в другой процесс. 

<b>Устойство сокет</b>

Устройства сокетов облегчают обмен данными между процессами, похожими на канальные устройства, но они могут взаимодействовать со многими процессами одновременно. 

<b>Характеристика устройства</b>

Устройства характеризуются двумя номерами: <b>основным номером устройства</b> и <b>младшим номером устройства</b>. Вы можете увидеть эти цифры в приведенном выше примере ls, они разделены запятой. Например, скажем, устройство имело номер устройства: <b>8, 0</b>:

Основной номер устройства представляет используемый драйвер устройства, в данном случае 8, который часто является основным номером для устройств блока sd. Младший номер сообщает ядру, какое уникальное устройство находится в этом драйвер классе, 0 используется для представления первого устройства (a).

## Задание

Посмотрите на свой каталог /dev и узнайте, какие типы устройств там находятся.

## Вопрос

Какой символ используется для символьных устройств в команде ls -l?

## Ответ

c