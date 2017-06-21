# Цели Systemd

## Содержание урока

Мы не будем подробно описывать системные файлы unit. Тем не менее, мы рассмотрим краткое описание файла unit и способы ручного управления устройствами.

Here is a basic service unit file: foobar.service

<pre>
[Unit]
Description=My Foobar
Before=bar.target

[Сервис]
ExecStart=/usr/bin/foobar

[Установка]
WantedBy=multi-user.target
</pre>

Это простая служебная цель, в начале файла мы видим секцию для [Unit], она позволяет нам дать нашему файлу устройства описание, а также контролировать порядок, когда активировать устройство. Следующая часть - раздел [Сервис], здесь мы можем запустить, остановить или перезагрузить службу. И раздел [Установка] используется для зависимости. Это только верхушка айсберга для записи системных файлов, поэтому я прошу вас прочитать эту тему, если вы хотите узнать больше.

Теперь давайте рассмотрим некоторые команды, которые вы можете использовать с системными модулями: 

<b>Список units</b>

<pre>$ systemctl list-units</pre>

<b>Просмотреть статус unit</b>

<pre>$ systemctl status networking.service</pre>

<b>Запустить сервис</b>

<pre>$ sudo systemctl start networking.service</pre>

<b>Остановить сервис</b>

<pre>$ sudo systemctl stop networking.service</pre>

<b>Перезапустить сервис</b>

<pre>$ sudo systemctl restart networking.service</pre>

<b>Включить unit</b>

<pre>$ sudo systemctl enable networking.service</pre>

<b>Отключить unit</b>

<pre>$ sudo systemctl disable networking.service</pre>

Опять же, вы еще не видели, насколько глубоко systemd попадает в, так что читать на нем, если вы хотите узнать больше.

## Задание

Просмотрите состояния устройства, запустите и остановите нескольких служб. Что вы видете?

## Вопрос

Какая команда запускает службу с именем peanut.service?

## Ответ

sudo systemctl start peanut.service