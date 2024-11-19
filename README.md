### Задание:

- получит данные из любого публичного api
- вывести список данных на странице каталога
- сделать возможность фильтрации по избранному, добавления и удаления товаров
- просмтр отдельного товара на отдельной странице

### Как запустить проект:

- создать .env, затем скопировать в него .env.example
- открыть cmd и написать npm i
- после написать npm run dev

### Структура проекта

## Чем выше слой тем больше в нем логики. Поток данных должен быть однонаправленным следующего вида:

- shared(components|constants|helpers...) => entities => modules => pages => app

- app слой приложения

- pages слой страниц. Страницы собираются из модулей

- modules независимые переиспользуемые модули, нужны для компановки страницы. Для использования использовать public api (index.ts)

- entities сущности нужны чтобы не захламлять modules & shared->components. Например сущность карточки, пагинация и тд. Для использования использовать public api (index.ts)

- shared слой хелперов и утилит

- shared -> components глупые компоненты по типу input, page-block, button & etc
