#  Циклы

Напишите миксин `colors`, принимающий на вход цветовую тему в виде ассоциативного массива и тон темы. Для каждого цвета из массива создаётся два селектора вида:

- *bg-название цвета в теме*. Внутри этого селектора находится свойство `background` с необходимым значением.
- *text-название цвета в теме*. Внутри этого селектора находится свойство `color` с необходимым значением.

Цветовая схема в качестве значения каждого цвета имеет ассоциативный массив из двух элементов: цвет для светлой темы и цвет для тёмной темы. Выбор тона темы настраивается с помощью второго аргумента миксина – `$tone`, который по умолчанию имеет значение *light*.

## Пример

```scss
$theme-colors: (
  "primary":    ("light": "#F5E6E8", "dark": "#1B262C"),
  "secondary":  ("light": "#D5C6E0", "dark": "#0F4C75"),
  "success":    ("light": "#AAA1C8", "dark": "#3282B8"),
  "info":       ("light": "#967AA1", "dark": "#F9F9F9"),
  "warning":    ("light": "#192A51", "dark": "#BBE1FA"),
);

@include colors($theme-colors);
```

После компиляции должен получиться следующий CSS-код (для примера будут выведены только селекторы для *primary* и *secondary*):

```css
.bg-primary {
  background: #F5E6E8;
}

.text-primary {
  color: #F5E6E8;
}

.bg-secondary {
  background: #D5C6E0;
}

.text-secondary {
  color: #D5C6E0;
}
```

## Подсказки

- Если вам надо удалить кавычки в строке, то воспользуйтесь функцией [unquote](https://sass-lang.com/documentation/modules/string/#unquote).

```scss
$quote-string: "ABC";
$clear-string: string.unquote($quote-string);
```