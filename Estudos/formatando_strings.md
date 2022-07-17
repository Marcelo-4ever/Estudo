# Formatando Strings 

## F-strings and  format

Talvez você já conheça as f-strings, mas caso não conheça vamos ver elas agora. Primeiro temos que criar algumas variáveis:

```py
quantidade_cachorro = 2
cachorro1 = 'Bob'
cachorro2 = 'Marley'
```

Agora que temos as variáveis como podemos escrever uma frase e colocar cada variável na frase? Podemos fazer dessa forma: 

---

### Sem f-strings:
```
#input
print('Eu tenho', quantidade_cachorro, 'cachorros e eles se chamam', cachorro1, 'e', cachorro2)

#output
Eu tenho 2 cachorros e eles se chamam Bob e Marley
```

Um pouco confuso, não? Cheio de aspas e vírgulas, felizmente existem as f-strings para facilitar a nossa vida. Vejamos: 

---

### Com f-strings

```py
print(f'Eu tenho {quantidade_cachorro} cachorros e eles se chamam {cachorro1} e {cachorro2}')
``` 

Para usar a f-strings você sempre coloca um *`f`* antes da primeira aspa, e quando você for colocar uma variável dentro da string como `quantidade_cachorro` é só abrir uma chave, coloca a variável dentro e fechar a chave. Bem mais fácil que usar várias vírgulas, certo? E você também não precisa se preocupar com o tipo de dado da variável, se é string, inteiro, float, bool etc.        
No outro exemplo se você quisesse concatenar as variáveis, ou seja, juntar as variáveis com as strings, dessa forma: 

```py
print('Eu tenho ' + quantidade_cachorro + ' cachorros e eles se chamam ' + cachorro1 + ' e ' + cachorro2)
```

Você receberia um TypeError pois a quantidade de cachorros é um valor *inteiro* e não pode ser concatenado com uma *string*, e esse é um problema que não é necessário se preocupar usando as f-strings. 

## Mais sobre as f-strings

Se eu quero fazer uma conta com duas variáveis e guardar o valor em uma outra variável e mostrar na tela eu posso fazer assim: 

```py
num1 = 10
num2 = 3
divisao = 10 / 3 

#input
print(f'{num1} / {num2} = {divisao}')

#output
3.3333333333333335
```
A resposta ficou um pouco grande demais, vamos ajeitar isso da seguinte maneira: 

```py
#input
print(f'{num1} / {num2} = {divisao:.2f}')

#output
3.33
```

O que aconteceu aqui? Vou te explicar passo a passo.    
Quando colocamos os dois pontos `:` dentro das chaves estamos falando para o python que vamos ter uma formatação, logo depois temos `'.2'` que significa que queremos apenas duas casas decimais, e por último o *`f`* que fala basicamente: 'duas casas decimais de pontos flutuantes'. Isso quer dizer que queremos 2 dígitos após o ponto flutuante, por isso o output foi 3.33.       
E se a conta tiver a resposta sendo um número inteiro? O python iria transformar em um valor *float* e adicionaria duas casas decimais: 

```py
divisao = 10 / 2 

#input
print(f'{divisao:.2f})

#output 
5.00
```
---
## Format

O format lembra um pouco as f-strings já que também usa chaves, porém, *eu* acho mais fácil usar as f-strings. Agora vamos ver alguns exemplos para entender esse método:

```
tamanho_em_metros = 23.5
tamanho_em_centimetros = 2350

#input
print('O tamanho da casa é {} metros ou {} centímetros'.format(tamanho_em_metros, tamanho_em_centímetros)) 

#output
O tamanho da casa é 23.5 metros ou 2350 centímetros
```
Passo a passo:
1. Abrir aspas
2. Coloca as chaves onde você vai querer suas variáveis
3. Fechar aspas
4. Escreve `.format()`
5. Dentro dos parênteses você vai escrever as variáveis na ordem que você quer que elas apareçam
6. Você precisa separá-las com vírgula
7. A quantidade de variáveis precisa ser a mesma ou menor que a quantidade de chaves dentro da string, se colocar mais você vai receber um erro

Sabendo desse disso, se você colocasse primeiro tamanho_em_centímetros e depois tamanho_em_metros a string ficaria assim:

```
O tamanho da casa é 2350 metros ou 23.5 centímetros
```

Para facilitar essa ordem, ao invés de ficar olhando a quantidade de chaves - imagina tem 5, 10 variáveis, você ficaria perdidinho vendo se tá colocando na ordem certa - você pode usar os índices. Vamos ver:

```py
graus_celsius = 30
graus_fahrenheit = 86
print('{0} graus celsius convertidos para fahrenheit é {1}'.format(graus_celsius, graus_fahrenheit))
```
 - Isso funciona da seguinte forma: as variáveis que estão dentro dos parênteses do format tem um índice começando do 0, então se você tiver uma variável ela terá o índice 0, se você colocar mais uma variável ela terá índice 1, se colocar mais uma ela terá índice 2...3,4,5 e assim vai.

Assim fica um pouco mais fácil de localizar as chaves para escrever as variáveis na ordem certa, e isso serve para quantas variáveis você quiser. 

E sabendo disso podemos fazer algo bem legal:

```
nome = 'Neymar'

#input
print('Então seu nome é {0}, ok, quer dizer que você é o {0}, aquele {0}? O {0} do Santos?'.format(nome))

#output
Então seu nome é Neymar, ok, quer dizer que você é o Neymar.. aquele Neymar? O Neymar do Santos?
```

Como a variável `nome` tem índice 0, quando eu colocar o `0` entre as chaves vou estar fazendo uma referência a ela. Se for colocada outra variável no lugar, todos os valores do *output* mudariam também.     
E não importa a ordem, olha só:

```
nome = 'Neymar'
nome2 = 'Messi' 

#input
print('Você é o {0} e ele o {1}? Certo, você é o {1} e ele é o {0}.'.format(nome, nome2))

#output
Você é o Neymar e ele o Messi? Certo, você é o Messi e ele é o Neymar.
```
Mas caso você *não* queira os índices 0, 1, 2, etc, você pode deixar explícito como você quer fazer referência a uma variável. Vamos ver:

```
nome1 = 'Marcelo'
nome2 = 'Antônio'
nome3 = 'Jorge'
nome4 = 'Nara' 

#input
print('5 pessoas vão para o festival: eu, {M}, {N}, {J}, {A}'.format(M=nome1, A=nome2, J=nome3, N=nome4))

#output
5 pessoas vão para o festival: eu, Marcelo, Nara, Jorge, Antônio

```
