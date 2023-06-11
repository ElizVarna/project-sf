# Bookshop

## ЗАДАНИЕ
**В рамках проекта вам необходимо:**

- Сверстать главную страницу интернет-магазина Bookshop. Макет находится здесь.
- Подключить Google Books API так, чтобы данные о книгах подгружались с сервера.
- Подключить созданный вами ранее слайдер.
- Поработать над правильной организацией проекта:
  - реализовать модульную структуру;
  - подключить Webpack;
  - настроить сборку с минификацией.
- Применить пройденные вами ранее инструменты оптимизации.

Теперь распишем требования более подробно.

## ФУНКЦИОНАЛЬНЫЕ ТРЕБОВАНИЯ
В рамках проекта нужно создать одну (главную) страницу книжного магазина. На странице должен быть следующий набор элементов:
### Шапка сайта
Шапка содержит логотип, навигацию и набор кнопок. Ссылки в меню можно оставить пустыми, так как реализация остальных страниц сайта в проекте не предусмотрена.
Кнопки авторизации, поиска и корзины неактивны. Однако при добавлении товара в корзину у иконки должен появиться бейджик с количеством товара в корзине.
При прокрутке сайта шапка должна оставаться закреплённой в верхней части экрана.
### Слайдер
Под шапкой сайта располагается слайдер. Чтобы сократить время разработки, рекомендуем вам использовать слайдер, которые вы создали при прохождении модулей по JavaScript.

Слайдер автоматически пролистывает изображения каждые 5 секунд, а после последнего изображения вновь переключается на первое. Перелистывать изображения можно также с помощью точек под слайдером.
Справа от слайдера располагаются цветные блоки. Их нужно сверстать как ссылки, адреса ссылок можно оставить пустыми.
### Список категорий и список книг
Под слайдером в левой части экрана располагается список категорий. Активная категория должна быть выделена визуально.
По умолчанию в качестве активной выбрана первая категория в списке. Клик на неактивную категорию делает её активной, и список книг перезагружается, чтобы отобразить книги из этой категории.

Список книг подгружается из Google Books API в соответствии с выбранной категорией. Для списка книг необходимо реализовать ленивую загрузку: сначала подгружаются первые 6 книг, по клику на кнопку «Load more» — ещё 6, и так далее.
### Карточка книги
**В карточке книги должна быть отображена следующая информация:**

1) Обложка. Если API не возвращает обложку, подставить вместо неё любую картинку-плейсхолдер.
2) Автор. Если авторов несколько, перечислить их через запятую.
3) Заголовок.
4) Рейтинг: от 1 до 5 звёздочек плюс общее количество отзывов. Если в данных о книге нет рейтинга, не показывать эту строчку.
5) Описание. Если текст в описании занимает больше 3-х строк, его нужно обрезать и добавить в конце многоточие.
6) Цена с указанием валюты. Если в данных о книге нет цены, не показывать эту строчку.

