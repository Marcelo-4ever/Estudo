## Operadores relacionais

| Operadores relacionais |      Significado:     |
|:----------------------:|:--------------------- |
| >                      | maior que             |
| >=                     | maior que ou igual a  |
| <                      | menor que             |
| <=                     | menor que ou igual a  |
| ==                     | igual a               |
| !=                     | diferente             |

Eles são feitos para realizar comparações e quando forem utilizados será devolvido um valor booleano, por exemplo, se nós temos o código `print(5 > 4)` será devolvido True, pois é verdade, 5 é maior que 4. Talvez você fique na dúvida entre `=` e `==`, mas vamos ver outros exemplos antes de explicar: 

```
2 > 1 # 2 é maior que 1? True
2 >= 1 # 2 é maior OU igual a 1? True, ele é maior
2 < 1 # 2 é menor que 1? False 
2 <= 1 # 2 é menor OU igual? False, ele não é menor
2 == 1 # 2 é igual a 1? False, ele não é igual  
2 != 1 = 2 é diferente de 1? True, ele é diferente 
```

## 

A diferença entre `=` e `==` é que com o sinal `=` você atribui um valor, é como se você falasse 'Isso vai ter esse valor e acabou', por exemplo:

```
valor = 5 # eu quero que a variável 'valor' passe a valer 5
valor = 10 # agora eu quero que ela passe a valer 10 
valor = valor + 2 # agora eu quero que ela pegue o valor dela e some 2, ou seja, como ela vale 10 vai ser 10 + 2, então vai passar a valer 12 a partir de agora 
```
Já o operador `==` não tem essa confiança todo de afirmar que algo vai valer tanto, ele apenas pergunta "Hey, isso aqui é maior que isso? E isso aqui, é menor? É maior?" e nós temos a resposta sendo `True` que é basicamente "Sim, tal valor é maior/menor/igual/diferente que o outro valor", e `False` é "Po, te falar que isso ai é fake news.". 
Como já foi dado alguns exemplos com todos os operadores, tente descobrir a resposta dos valores abaixo e depois coloque no seu editor de código: 

```
valor = 1 
10 > valor     # ?
-5 >= valor    # ?
2 > valor + 1  # ?  
5 < valor	   # ?

outro_valor = 8
6 <= valor + outro_valor  # ?
9 == valor + outro_valor  # ?
0 > valor - outro_valor   # ?
valor >= outro_valor      # ?
1 != 2  # ?
-7 != valor - outro_valor # ?
```
## 

Uma coisa que você deve lembrar é que `2` != `'2'`, `2` != `2.0` e `'2'` != `2.0`  então preste atenção nos valores, duas aspas podem te dar uma resposta diferente do esperado. Por exemplo: 

```
usuario = input('Digite um valor: ')
print(usuario == 2)

#output
Digite um valor: 2
False
``` 
Como assim False se o input foi 2? O input por padrão recebe qualquer valor como uma string, então a pergunta não foi `2` == `2` e sim `'2'` == `2`, o que não é verdade, por isso False. 

Podemos também atribuir uma comparação a uma variável dessa forma: 

```
valor1 = 2
valor2 = 5
comparar_valores = valor1 == valor2  
```
Aqui temos duas variáveis e cada uma com um valor diferente, depois criamos mais uma variável e falamos que ela vai ser o resultado do que for a resposta de `valor1 == valor2`. Como 2 não é igual a 5, o valor atribuido a `compararar_valores` será `False`

##

### Exemplificando em um código: 

```
idade = 18 
if idade == 18:
	print('Você tem 18 anos.')
if idade != 18: 
	print('Você tem mais ou tem menos de 18, mas não tem 18 anos.)
if idade > 18: 
	print('Você não tem 18 anos, você tem no mínimo 19.')
if idade < 18:
	print('Você não tem 18 anos, no máximo tem 17.')
if idade >= 18: 
	print('Ou você tem 18 anos, ou você tem mais que 18.)
if idade <= 18: 
	print('Ou você tem 18 anos, ou você tem menos que 18.)
```

## 

Além disso tudo, podemos comparar duas coisas ou mais ao mesmo tempo usando os operadores `and` e `or`, se liga:

```
dinheiro = 15 
divida = 10

if dinheiro == 15 or dinheiro >= 15 or dinheiro > 15:
	print('Ou você tem exatamente 15, ou tem exatamente 15 e se bobear tem mais, ou tem 16 pra cima.' )

if dinheiro != 10 and dinheiro > 10:
	print('Você não tem exatamente 10 reais, mas tem mais que isso)

if dinheiro >= 10 and divida == 10 or divida <= 10:  
	print('Então você tem 10 ou mais, e a sua dívida é 10 ou até menor que isso, pode ir pagar!)

```

O `and` vem do inglês e significa `e` e o `or` significa `ou`, então quando utilizamos o *and* queremos saber se duas coisas acontecem ao mesmo tempo e quando usamos o *or* queremos saber se uma coisa ou outra está acontecendo. 
*Veremos mais sobre esses operadores no próximo tópico.

##

Ter esse conhecimento de saber se algo vai retornar True ou False é muito necessário e vai te ajudar bastante, então treine e estude bastante esse tópico para conseguir pegar essas comparações de uma maneira mais rápida! :)


