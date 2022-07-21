## Operadores Lógicos

Os operadores lógicos são *and*, *or*, *in*, *not* e *not in*. 

Os operadores **and** e **or** acontecem entre duas comparações:

```
a = 2
b = 2
c = 3
print(a == b and a < c) # True, pois as duas comparações são verdade
print(a == b and a > c) # False, pois só uma comparação é verdade

print(a == b or a < c)  # True, pois pelo menos uma comparação é verdade
print(a == b or a > c)  # True, pois pelo menos uma comparação é verdade
print(a != b or a > c)  #False, pois as duas comparações são falsas
```

| comparação1   comparação2 | Resultado |
|---------------------------|:---------:|
| verdadeiro and verdadeiro | True      |
| verdadeiro and  falso     | False     |
| falso      and  falso     | False     |
| verdadeiro or verdadeiro  | True      |
| verdadeiro or   falso     | True      |
|    falso   or   falso     | Falso     |

##

O operador **not** não precisa de duas expressões, apenas uma. E ele é chamado de inversor, pois inverte o valor da expressão/comparação. 

```
a = 2
b = 3

if b > a: # se o b for maior que a 
	print('b é maior que a')

if not b > a: # se b NÃO for maior que a
	print('b não é maior que a')
```

Ou seja, se temos uma comparação verdadeira como `b > a` o bloco de código dela será executado. Agora se a gente não quiser o que o código aconteça podemos colocar um *not* antes, pois ele irá inverter o True para False.     
Já foi falado bem no início dos tópicos de python que valores vazios retornam False, então podemos criar códigos assim: 

```
v = ''

if v: # isso significa "if v == True"
	print('Algo foi escrito')

if not v: # se v for False(vazio), inverte e virá True
	print('Nada foi escrito')
```
Se você não entendeu muito bem o *not*, não se preocupe, eu também demorei um tempo p/ entender e ainda levo um tempo para entender o que tal expressão significa. Esse é o passo a passo do código acima: 

1. `v` é uma string vazia
2. Valores vazios equivalem a um valor booleano **False**
3. A condição `if v:` é uma forma curta de escrever `if v == True`
    - `v` só poderia ser **True** se outro valor fosse atribuído a ele; adicionar uma letra já funcionaria
    - Isso acontecendo seria printado `Algo foi escrito`
4. A condição `if not v:` significa que se `v` for False - não tiver nenhum valor -, a expressão `not v` inverte o valor para True
    - Com o valor True a linha de código será executada e irá printar: `Nada foi escrito`

Espero ter ficado o mais claro possível. :)

##

Os operadores **in** e **not in**, que também retornam valores booleanos, respondem se algo *está* ou *não está* alguma outra coisa, por exemplo:  

```
vogais = 'aeiou'
print('a' in vogais') # True, tem a letra 'a' em 'aeiou'
print('a' not in vogais) # False, letra 'a' está sim em 'aeiou'
```








