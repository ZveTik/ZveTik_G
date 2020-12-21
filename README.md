# ZveTik_G
Это ёлочная гирлянда на основе WS2811(и подобных) светодиодов. Ответвление от основного проекта #ZveTik. Проект реализован на Arduino Nano (328p), из-за ограниченного в 32КБ Flash, скорее всего переедет на Mega2560, но в проекте предусмотрена возможность "закомментировать" эффекты, и уложиться в 32КБ, что бы использовать Nano. Количество SRAM так же накладывает ограничение на количестве используемых светодиодов. В текущий момент проект разрабатывается на ленте в 50 светодиодов, будет адаптирован по гирлянду в 100 светодиодов, под 2 модуля (по 50шт) гирлянд от "BTF-LIGHTING".  
В проекте заложена возможность использовать: 255 режимов отображения, несколько режимов демонстрации, управление с ИК пульта, сохранение настроек, использование параметров отображения, легкая интеграция "авторских" и удаление "не нужных" режимов. 

# Режимы
[1-10] Очень спокойные режимы, без ярких всплесков, градиентов, режимы "классических" гирлянд.
[11-20] Спокойные градиентные переливы.
[21-100] Планируются встроенные режимы, переливы, градиенты, анимация.
[101-200] Планируются "авторские режимы", режимы написанные различными авторами.
[201-255] "Сложные" и тяжелые режимы, с длительной поэтапной анимацией.

# Управление
Управление осуществляется с пульта ИК (21 кнопка). Изначально управление осуществлялось с ИК пульта на 17 кнопок, но из-за большого количества режимов, количества параметров было принято решение перейти на пульт с 21 кнопкой, весь код пульта на 17 кнопок вырезан, использование пульта на 17 кнопок не планируется.
ZveTik_G использует систему команд, поэтому можно реализовать любое управление, внутреннее через кнопки, или же, внешнее через Com порт или LAN (а надо ли?)

# Трудности разработки эффектов
Все светодиоды различаются своей яркостью и цвето передачей. С цвето передачей на гирлянде можно смерится, но вот яркость вносит свои коррективы в разработку. Я разрабатываю эффекты за компьютером, на ленте 60 светодиодов на метр. Лента дает очень яркий, резкий цвет. Гирлянда состоит из матовых RGB светодиодов, которые дают очень мягкий, приятный, но не яркий свет. Поэтому все эффекты "обкатанные" на столе, на гирлянде отображаются совсем по другому. И яркость не та, и тайминги отображения (слишком быстро), и то что светодиоды расположенные с разрывом друг от друга, и то что по спирали гирлянда лежит на елке. Приходится вносить много корректировок, и когда эффект начинает смотрется на "елке", на столе, на ленте, он вообще не смотрится. 
