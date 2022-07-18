## **Input**

A função input serve para pedir alguma informação ao usuário. Nela você escreve uma string e a resposta também será uma string por padrão. 

```
input('Qual o seu nome? ')
 
#output 
Qual o seu nome? Marcelo
```
Claro, você pode escrever valores inteiros no input, mas como geralmente você está pedindo alguma informação não faz muito sentido escrever algo como: 

```
exemplo = input(12345 )

#output
12345 # O que o programa está pedindo? 
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
A idade é interpretada como '18', e não 18. Então não seria possível fazer contas com a resposta já que precisa ser um valor inteiro. Vamos ver um exemplo: 


```
idade = input('Qual sua idade? ')
print(idade + 10)

#output
Qual sua idade? 18
#vai mostrar um erro 
```
##

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
## 

### Alguns Problemas

Nesses exemplos onde a variável idade é convertida para o tipo inteiro, isso só vai acontecer quando o usuário digitar um valor numérico e isso serve para o tipo _float_ também: 

```
km = input('Você estava a quantos km hora? )
print(km)

#output 
Você estava a quantos km hora? 45
45.0 # converteu para float
```

Mas e se ele não fizer isso? Se ele quiser testar o programa ou digitou errado alguma coisa igual no exemplo abaixo:

```
km = input('Você estava a quantos km hora? )
print(km)

#output 
Você estava a quantos km hora? 45ab
# vai causar um erro
```

Nesses casos é necessário fazer uma validação, e para validar precisamos aprender sobre as condições _if, elif, else_ que vão ser mostradas no próximo tópico. E junto do conhecimento dessas condições _você_ tem que pesquisar sobre o método `isdigit()` em python e tentar validar esse código: 

```
senha = 1234
usuário = input('Digite sua senha: ')

#output 
Digite sua senha: abcd # eai, como que você vai fazer? Primeiro leia o próximo tópico e depois volte nesse probleminha.
```

## 

[Continuar](https://github.com/Marcelo-4ever/Estudo/blob/main/Estudos/condicionais.md)











