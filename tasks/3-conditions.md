# Условные конструкции

Создайте функцию `grid-container-width`, которая высчитывает ширину в зависимости от того, сколько колонок мы хотим использовать.

Вам доступны две переменные:

- `$grid-width` — ширина одной колонки.
- `$gutter-width` — ширина отступа от колонки.

Функция принимает один аргумент — количество колонок, которые должен занимать элемент. На выходе получаем число с единицей измерения.

Если переданное число колонок меньше или равно нулю, то возвращается ширина одной колонки.

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
```scss
$grid-width: 45px;
$gutter-width: 15px;

.container {
  width: grid-container-width(-15);
}
```
```scss
.container {
  width: 45px;
}