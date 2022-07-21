## **Funções built-in**

As funções built-in são funções que já vêm por padrão no python, não é necessário instalar nenhum módulo ou importar alguma biblioteca. [Aqui está o link](https://docs.python.org/3/library/functions.html) se você quiser ver todas elas. 

Vamos pensar em um pequeno problema, você usa dois inputs para fazer a soma de valores inteiros:

```
valor1 = input('Digite um valor: ') 
valor2 = input('Digite um valor: ') 
```

Mas o usuário querendo testar o programa não responde nenhum valor inteiro e sim algumas letras e quebra o seu programa, como faz? O python não vai converter automaticamente para você em nenhuma situação o valor do usuário p/ verificar se é um número ou se não é - algo que pode acontecer em outras linguagens -, então nesse caso podemos usar uma função built-in chamada 'isdigit()' que é uma string method.     
Ou seja, é uma função - que na verdade é chamado de método - , e é aplicada somente nas strings e vai verificar se uma string é um valor numérico ou não.

*Você pode ver todas as string methods [nesse link](https://docs.python.org/3/library/stdtypes.html#string-methods) 

```
valor1 = str(input('Digite um valor: ')) 
valor2 = str(input('Digite um valor: ')) 

if valor1.isdigit() and valor2.isdigit(): # confirmar se os dois valores são numéricos
	print(int(valor1) + int(valor2)) # convertendo p/ inteiro, fazendo a soma e imprimindo na tela 

else:
	print('Digite valores válidos.')
``` 

Esse método 'isdigit()' retorna um valor booleano True ou False, sendo True quando um valor **pode** ser convertido para número e False quando **não pode**. No entanto, esse método e outros como 'isnumeric() e 'isdecimal' vão verificar como verdadeiro apenas números que tenham os dígitos de 0-9, então um valor inteiro negativo('-2') não seria considerado um número e nem um valor float('2.0') por causa do `.`.   
Isso é um grande problema e como não pôde ser resolvido com as funções do próprio python nós precisaríamos *criar* novas funções, mas isso é um assunto mais avançado e não será mostrado agora😅. 

## 

Existem outros métodos 'isAlgumaCoisa()', como exemplo temos:

- x.islower() - verifica se todos os caracteres são minúsculos, número não faz diferença                                         
- x.isupper() - verifica se todos os caracteres são maiúsculo, número não faz diferença                                            
- x.isspace() - verifica se a string tem somente espaços

E você pode ver todas as outras nesse [link](https://docs.python.org/3/library/stdtypes.html#string-methods), que é o mesmo dos strings methods - porque é um método que acontece nas strings -. Para encontrar mais rápido é só dar um 'CTRL + F' ou 'F3' e escrever **'.is'** 
