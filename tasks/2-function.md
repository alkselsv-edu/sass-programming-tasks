# Функции

Создайте функцию `grid-container-width`, которая высчитывает ширину в зависимости от того, сколько колонок мы хотим использовать.

Вам доступны две переменные:

- `$grid-width` — ширина одной колонки.
- `$gutter-width` — ширина отступа между колонками.

Функция принимает один аргумент — количество колонок, которые должен занимать элемент. На выходе получаем число с единицей измерения.

## Пример

```scss
$grid-width: 45px;
$gutter-width: 15px;

.container {
  width: grid-container-width(15);
}
```

```scss
.container {
  width: 885px;
}
```

## Подсказки

- Количество отступов между колонками на один меньше, чем количество колонок.