# ArrayListJs

## Map, Filter e Reduce

## Map
O méotodo map tem como finalidade executar uma função de cada item do array, se parece muito com o for each,mas
a diferença é que no map ele retorna um novo array diferente do foreach que só sobreescreve o array, como por exemplo se
eu tiver uma lista de números e quiser multiplicar eles por 5, se eu der um console.log na variável antiga vai aparecer
os valores antigos antes da multiplicação, e seu eu fizer um console.log na nova variável vai aparecer todos os valores
multiplicados.

### exemplos

```
const numeros = [1, 2, 3]
const multiplicarNumero = numeros.map(numero => numero * 5);
console.log(numeros);
console.log(multiplicarNumero);
```

```
const pessoas = [
  { nome: "João", idade: 25 },
  { nome: "Luis", idade: 30 },
  { nome: "Simão", idade: 22 }
];

const nomes = pessoas.map(pessoa => pessoa.nome);
console.log(nomes); 
```

```
const frutas = [
  { nome: "maçã", cor: "vermelha" },
  { nome: "banana", cor: "amarela" },
  { nome: "uva", cor: "roxa" }
];

const nomesDasFrutas = frutas.map(function(fruta) {
  return fruta.nome;
});

console.log(nomesDasFrutas);
```

### Vantagens
> O map permite criar um novo array, preservando o original
> Código se torna mais limpo


## Filter

O filter é um método usado para filtrar elementos de um array com base em uma condição. 
Ele cria um novo array com os elementos que atendem à condição e não altera o array original,
A função fornecida ao filter retorna true ou false para cada item, ele
vai incluir no novo array apenas os itens para os quais a função retorna true.


### exemplos

```
const numeros = [5, 10, 15, 20];
const maioresQueDez = numeros.filter(num => num > 10);
console.log(maioresQueDez);
```

```
const numeros = [-1, 2, -3, 4, -5];
const negativos = numeros.filter(num => num < 0);
console.log(negativos);
```

```
const frutas = ["maçã", "banana", "manga", "laranja"];

const frutasComM = frutas.filter(function(fruta) {
  return fruta[0] === "m";
});

console.log(frutasComM);
```
### Vantagens
> Permite que você filtre os dados de forma simples com base em qualquer condição

## Reduce

O método reduce é usado para reduzir um array a um único valor, aplicando uma função acumuladora que
processa cada elemento do array. Ele recebe dois argumentos: a função de callback, que é executada em cada item 
e um valor inicial,que pode ser opcional. O reduce itera sobre os elementos do array, acumulando
um resultado, que pode ser uma soma, um objeto ou qualquer outro valor.


### exemplos


```
const numeros = [1, 2, 3, 4];
const soma = numeros.reduce(function(acumulador, numero) {
  return acumulador + numero;
}, 0);
console.log(soma);
```

```
const palavras = ["Olá", "mundo"];
const frase = palavras.reduce(function(acumulador, palavra) {
  return acumulador + " " + palavra;
});
console.log(frase);
```



### Vantagens
> Manipular valores acumulados de maneira mais flexível
> Pode ser usado em uma ampla variedade de situações, desde simples somas até manipulações complexas de objetos
