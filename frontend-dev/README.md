# Тестовое задание для Frontend разработчика

### Задание 1

- Необходимо присвоить значение false свойству "withOwner" всем животным, у которых его нет
- Получить список всех кошек без хозяев, которым больше 2х лет
- Указать на ошибки реализации и предложить свой вариант решения

```js
var animals = [
    { kind: 'cat', age: 3, withOwner: true },
    { kind: 'cat', age: 2, withOwner: false },
    { kind: 'dog', age: 5 },
    { kind: 'cat', age: 1 },
    { kind: 'parrot', age: 2, withOwner: true },
    { kind: 'cat', age: 6 }
];
for (let i = 1; i < animals.length; i++) {
    const animal = animals[i];
    if (!animal.withOwner) animal.withOwner = false;
}

var nobodysCatList = [];
for (let i = 1; i < animals.length; i++) {
    const animal = animals[i];
    if (!animal.withOwner && animal.age >= 2) nobodysCatList.push(animal);
}
console.log(nobodysCatList);
```

### Задание 2

- Имеется неупорядоченный массив пунктов меню
- Необходимо получить массив для построения многоуровневого меню вида

```
 Users  -  Outlets  -  Settings
     |           |            |
     Seller      Group A      Password
     Supervisor  Group B      Lang
```

```js
const MenuItems = [
  { id: 1, name: 'Пользователи', parentId: 'root' },
  { id: 7, name: 'ТТ категория B', parentId: 2 },
	{ id: 2, name: 'Торговые точки', parentId: 'root' },
	{ id: 4, name: 'Супервайзеры', parentId: 1 },
	{ id: 9, name: 'Категории точек', parentId: 5 },
  { id: 3, name: 'Настройки', parentId: 'root' },
	{ id: 10, name: 'Смена языка', parentId: 3 },
  { id: 6, name: 'ТТ категория A', parentId: 2 },
  { id: 8, name: 'Смена пароля', parentId: 3 },
	{ id: 5, name: 'Продавцы', parentId: 1 }
];
````

### Задание 3

- Дана структура данных в виде дерева, необходимо получить сумму вершин

```js
{
  value: 1,
  children: [
    {
      value: 2,
      children: [
        {
          value: 4
        },
        {
          value: 5
        }
      ]
    },
    {
      value: 3,
      children: [
        {
          value: 6
        },
        {
          value: 7
        }
      ]
    }
  ]
}
```
