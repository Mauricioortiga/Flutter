soma (a, b) {

print (a + b)

  **ou**

return a + b;

**Isto é um tipo Dynamic, podendo ser especificados como int.**

---

main () {

  soma (2, 3);

}

**ou**

main () {

  print ('O valor da soma é: ${soma(2, 3)}');

**ou**

main () {
  final r = soma(2, 3);

print ('O valor da soma é: $r');

}

---

**Podemos passar uma função como parâmetro:**

void exec(int a, int b, int Function (int, int) fn) {

  return fn (a + b);
}

main () {

  final r = exec(2, 3, (a, b) {

    return a - b;
});

  print ('O resultado é $r');
}

---

**Definindo como uma arrow function:**


main () {

  final r = exec(2, 3, (a, b) => a * b + 100);

  print ('O resultado é $r);

---

**Criando classes:**

class Produto {

  String nome;

  double preco;
}

main () {

  var p1 = new Produto();
  p1.nome = 'Lapis':
  p1.preco = 4.59;

  print ('O produto ${p1.nome} tem preço R\$${p1.preco}");

}

**Resultado:**

O produto Lapis tem preço R$ 4.59 

  **ou**

class Produto {

  String nome;

  double preco;

  Produto(String nome, double preco) {

    this.nome = nome;

    this.preco = preco;

  }

}

main () {

  var p1 = Produto('Caneta', 4.99);
  
  var p2 = Produto('Geladeira', 1454.99);

  print ("O produto ${p1.nome} tem preço R\$${p1.preco}");

   print ("O produto ${p2.nome} tem preço R\$${p2.preco}");

**Resultado:**

  O produto Caneta tem preço R$4.99

  O produto Geladeira tem preço 1454.99


ou

**Parâmetro Posicional:** A ordem que definimos no método vai ser a ordem que será aplicada no momento que chamar o método.

class Produto {

  String nome;

  double preco;

  Produto(this.nome, this.preco) {

    this.nome = nome;

    this.preco = preco;

main () {

  var p1 = Produto('Caneta', 4.99);
  
  var p2 = Produto('Geladeira', 1454.99);

  print ("O produto ${p1.nome} tem preço R\$${p1.preco}");

   print ("O produto ${p2.nome} tem preço R\$${p2.preco}");

  **ou**

**Parâmetro Nomeado:** É um parâmetro que tem um nome definido.

main () {

  var p1 = Produto(nome: 'Caneta');

Caso retirarmos o valor de 'Caneta', **POR PADRÃO**, Assume-se que é 4.99**
  
  var p2 = Produto(nome: 'Geladeira', preco: 1454.99);

  print ("O produto ${p1.nome} tem preço R\$${p1.preco}");

   print ("O produto ${p2.nome} tem preço R\$${p2.preco}");

  **ou**

**Parâmetros nomeados**

imprimirProduto ({String nome, double preco}) {

print ("O produto ${nome} tem preço R\$${preco}");

imprimirProduto (preco: p1.preco, nome: p1.nome);

imprimirProduto (preco: p2.preco, nome: p2.nome);

}

  **ou**

**Definir o número de vezes que eu quero que mostre o resultado:**

imprimirProduto(int qtde, {String nome, double preco})  {
  for (var i = 0; i < qtde; i++) {

  print ("O produto ${nome} tem preço R\$${preco});
  }
}

imprimirProduto (1, preco: p1.preco, nome: p1.nome);

imprimirProduto (20, preco: p2.preco, nome: p2.nome);

**Imprime o primeiro produto 1 vez e o segundo produto 20 vezes.**
