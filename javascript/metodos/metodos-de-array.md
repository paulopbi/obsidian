---
tags:
  - javascript
  - array
  - métodos
---
## array.includes()

O método `includes()` verifica se um array contém um determinado valor ou elemento, retornando um booleano `true` ou `false` caso inclua ou não o valor determinado.

```js
const arr = ['Júlia', 'Paulo Victor', 'Ricardo', 'Luana', 'Roberto']

arr.includes("Júlia") //true
[1, 2, 3].includes(2); // true
[1, 2, 3].includes(4); // false
```

_Sintaxe:_ `array.includes(searchElement, fromIndex)`

- `searchElement`: O elemento que será buscado.
- `fromIndex`: A posição no array de onde a busca pelo `searchElement` se iniciará. Por padrão, 0 (_opcional_).
## array.from()

O método `Array.from()` cria uma nova instância de um `Array` quando for passado um array-like ou um iterable object como argumento.

```js
let li = document.querySelectorAll('li'); // NodeList
li = Array.from(li); // Array

const carros = {
  0: 'Fiat',
  1: 'Honda',
  2: 'Ford',
  length: 4,
}

const carrosArray = Array.from(carros);
```

 _Sintaxe:_ `Array.from(arrayLike, mapFn, thisArg)`

- `arrayLike`: Espera um array-like ou um objeto iterável para converter em array.
- `mapFn`: Função Map que será chamada para cada elemento do array (_opcional_).
- `thisArg`: Valor a ser utilizado como this quando a `mapFn` for chamada.
## array.filter()

O `filter` retorna um novo array que filtra os dados  a partir de uma condição logica retiramos algo indesejado, deixando apenas os elementos que queremos!

```js
//exemplo 1
const numbers = [2, 20, 23, 24, 12, 10, 16, 43, 54, 43, 6, 16, 4];

numbers.filter((value, index, array) => {
  if (value >= 20) {
    console.log(value);
    //20, 23, 24, 43, 54, 43
  }
});

//exemplo 2
function isBigEnough(value) {
  return value >= 10;
}
var filtered = [12, 5, 8, 130, 44].filter(isBigEnough);
// filtered is [12, 130, 44]
```

_Sintaxe_ `array.filter(callback(value, index, array) => {})`

- `callback`: É a função que é passada dentro do método.
- `value`: É o elemento atual que está no array.
- `index`: O índice do elemento atual que está no array.
- `array`: O array original que o `filter` foi chamado.
## MAP

O `map` percorre todos os elementos e mapeia os dados gerando um novo array que podemos modificar (se estiver atribuído a uma variável).

```js
const products = [
  { name: "Camisa", price: 2000, category: "Roupa" },
  { name: "AirForce", price: 164, category: "Tenis" },
  { name: "Pocophone F5", price: 5322, category: "SmartPhone" },
  { name: "Iphone", price: 2434, category: "SmartPhone" },
  { name: "Samsung", price: 6566, category: "SmartPhone" },
];

products.map((product) => {
  if (product.category === "SmartPhone") {
    product.onSale = true;
  }
});
  
console.log(products); //todos os itens smartphone tem onsale true
```

_Sintaxe_ `arr.map(callback(value, index, array) => {})`