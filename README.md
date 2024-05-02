# Тестовое задание: SPA приложение

## Описание
Данное SPA (Single Page Application) приложение разработано в рамках тестового задания. Оно представляет собой одноэкранное приложение, которое содержит вертикальный список элементов, а также горизонтальные списки в каждом элементе вертикального списка.

## Задача
Разработать SPA приложение согласно следующим требованиям:

- Вертикальный список должен содержать рандомное количество элементов, превышающее 100.
- Каждый элемент вертикального списка должен содержать горизонтальный список с рандомным количеством элементов, превышающим 10.
- Каждая ячейка горизонтального списка должна быть представлена квадратиком с бордером и скругленными углами произвольного радиуса, отображающим случайное число.
- При наведении на квадратик он должен анимированно уменьшаться на 20% (при наведении уменьшаться, при уходе курсора за границы возвращаться к прежним размерам).
- Раз в секунду должно происходить обновление одного случайного числа во всех горизонтальных списках, при этом обновление должно происходить только в видимой области.
- Важным аспектом является оптимизация производительности приложения.

## Технологии
Для реализации SPA приложения использовались следующие технологии:

- Vue.js - JavaScript фреймворк для разработки пользовательских интерфейсов
- CSS - каскадные таблицы стилей для визуального оформления элементов приложения

## Установка и запуск
1. Склонируйте репозиторий на свой локальный компьютер.
2. Убедитесь, что на вашем компьютере установлен Node.js.
3. Установите зависимости, используя команду `npm install`.
4. Запустите приложение, выполнив команду `npm run serve`.
5. Откройте приложение в вашем веб-браузере, перейдя по адресу `http://localhost:8080` (или другому порту, если он указан в выводе команды `npm run serve`).

## Примечание
Данное приложение разработано исключительно в целях тестирования навыков программирования и не предназначено для использования в реальных проектах.
