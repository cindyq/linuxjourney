# Уровни привилегий

## Содержание урока

Следующие несколько уроков становятся довольно теоретическими, поэтому, если вы ищете какой-то практический материал, вы можете пропустить их и вернуться позже.

Почему у нас разные уровни абстракции для пространства пользователя и ядра? Почему вы не можете объединить обе силы в один уровень? Ну есть очень хорошая причина, почему эти два слоя существуют отдельно. Оба они работают в разных режимах, kernel работает в режиме ядра, а пользовательское пространство работает в пользовательском режиме. 

В режиме kernel ядро имеет полный доступ к оборудованию, оно контролирует все. В режиме пользовательского пространства имеется очень малое количество безопасной памяти и процессора, к которым вам разрешен доступ. В основном, когда мы хотим делать что-либо, что касается аппаратного обеспечения, чтения данных с наших дисков, записи данных на наши диски, управления нашей сетью и т.д. Все это делается в режиме ядра. Почему это необходимо? Представьте, что ваша машина была заражена шпионскими программами, вы не хотели бы, чтобы она имела прямой доступ к оборудованию вашей системы. Он может получить доступ ко всем вашим данным, веб-камере и т.д.

Эти различные режимы называются уровнями привилегий и часто называются кольцами защиты. Чтобы сделать эту картину более ясной, скажем, вы узнаете, что Бритни Спирс находится в городе у вашего местного клерба, ее защищают ее группы, затем ее личные телохранители, а затем вышибала у клерба. Вы хотите получить ее автограф (потому что почему бы и нет?), Но вы не можете добраться до нее, потому что она в большой степени защищена. Кольца работают одинаково, самое внутреннее кольцо соответствует самому высокому уровню привилегий. В архитектуре x86-архитектуры есть два основных уровня или режима. Ring #3 - это привилегия, с которой запускаются приложения пользовательского режима, Ring #0 - это привилегия, с которой работает ядро. Ring #0 может выполнять любую системную команду и получает полное доверие. Итак, теперь, когда мы знаем, как работают эти уровни привилегий, как мы что-либо можем написать на нашем оборудовании? Всегда ли нам нужно будет переключаться в пользовательский режим? 

Ответ заключается в системных вызовах, системные вызовы позволяют нам выполнять привилегированную команду в режиме ядра и затем снова переключаться в пользовательский режим.

## Задание

Никаких упражнений для этого урока.

## Вопрос

Какой номер кольца имеет самые высокие привилегии?

## Ответ

0