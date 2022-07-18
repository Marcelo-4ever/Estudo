## Input

A função input serve para pedir alguma informação ao usuário. Nela você escreve uma string e a resposta também será uma string por padrão. 

```
input('Qual o seu nome? ')
 
#output 
Qual o seu nome? Marcelo
```

Eu também posso salvar a resposta do usuário em uma variável: 

```
nome = input('Qual é o seu nome? ')
print(f'Prazer, {nome}!') 
print(type(nome)) #verificar se é uma string 

#output 
Qual o seu nome? Marcelo
Prazer, Marcelo!
<class 'str'>
```

Percebe que a classe realmente é do tipo string? E isso não funciona só com letras, com números também: 

```
idade = input('Qual sua idade? ')
print(type(idade))

#output
Qual sua idade? 18 
<class 'str'
```
A idade seria interpretada como '18', e não 18. Então não seria possível fazer contas com a resposta já que precisa ser um valor inteiro. Vamos ver um exemplo: 


```
idade = input('Qual sua idade? ')
print(idade + 10)

#output
Qual sua idade? 18
#vai mostrar um erro 
```

E como podemos resolver isso? Nós já vimos o type casting, então para transformar uma string em um inteiro é algo bem fácil e vou te mostrar duas formas:

Nessa a string é convertida para inteiro no momento que a conta está sendo feita:

```
idade = input('Qual a sua idade? ')
print(10 + int(idade)) 

#output
Qual a sua idade? 18
28
``` 

E desse jeito você converte para inteiro no momento que o usuário digita a idade: 

```
idade = int(input('Qual a sua idade? '))
print(10 + idade) 

#output
Qual a sua idade? 18
28
``` 