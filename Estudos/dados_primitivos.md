# Dados primitivos

## Tipos de Dados

Python é uma linguagem de tipagem dinâmica, ou seja, você não precisa declarar a todo instante se é uma string ou um inteiro pois o Python consegue detectar o tipo sozinho. 
Durante o básico os tipos mais usado vão ser:

- *Strings* que são textos dentro de aspas simples, duplas ou triplas: 

``` py
print('Olá')
print("Eu me chamo Marcelo")
print("""Tudo bem com você?""")
print('''Espero que sim!''')
```

- *Inteiros* que são os números negativos e positivos, incluindo 0.  

``` py
-20, 0, 20
```

- *Float* são os números reais ou de ponto flutuante(por causa do ponto) e é todo número positivo e negativo que tem um ponto ' . '.    
  - Na programação ao invés de vírgula é sempre usado um ponto em números.

```py
-230.00, 0.0, 322.0
```

- *Bool* são os booleanos ou valores lógicos e eles têm apenas dois valores: True ou False, e servem para validar se algo é verdadeiro ou falso. Geralmente é usado em comparações como: 

```py
#Input
print(10 > 12)
print(2 < 3)

#Output
False
True
```

## Tipo de um valor

### Função type()

Para saber o tipo primitivo de um valor pode ser usada a função *type()*. Por exemplo, `type('Qualquer coisa')` vai mostrar na tela `<class 'str'>`, ou seja, uma string.                                      
```py
type('Marcelo') # string                                
type('10') # string                          
type(10) # inteiro          
type(10.0) # float                       
type(10 > 9) # bool           
```

- OBS: o 10 é considerado uma string quando é escrito com aspas e é considerado um inteiro quando está sem aspas. Não esqueça, se você quiser tratar um número como um número, seja inteiro ou float, não escreva *entre aspas*.
```py
#input
print('10' + '10') 

#output
1010

# '10' é uma string pois tem aspas, então o sinal de + irá fazer uma concatenação, que é juntar os dois valores, por isso o resultado foi '1010'

#input
print(10 + 10) 

#output
20

# 10 sem aspas é um inteiro, então o sinal de + vai funcionar como uma conta normal e vai mostrar na tela 20.
```
Se você for testar escrever `(10 + '10')` vai dar erro, pois, os dois precisam ser do mesmo tipo para funcionar. E com isso vamos para o próximo tópico: [type casting](https://github.com/Marcelo-4ever/Estudo/blob/main/Estudos/type_casting.md).



