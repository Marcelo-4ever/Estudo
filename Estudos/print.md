## Print
Print é o comando usado para imprimir na tela os argumenetos colocados dentro do seus parênteses. 

```
#Input
print('Marcelo', 'Ferreira') # são dois argumentos separados por vírgula e que serão imprimidos separados por um espaço.

#Output
Marcelo Ferreira
```

Se você começou python há pouquíssimo tempo, já tentou colocar aspas dentro da função print assim: 
`print('Hoje foi um dia 'legal'')`

E recebeu um erro, certo? O mesmo aconteceria se você trocasse todas as aspas simples para aspas duplas, e por isso existe os *caracteres de escape*. Eles consistem em você colocar uma contrabarra antes de um determinado caractere para que aconteça algo específico. Vejamos com as aspas:
```
#input
print("Hoje foi um dia \"legal\"") 
print('Hoje foi um dia \'legal\'')

#output
Hoje foi um dia "legal"
Hoje foi um dia 'legal'
```
Nesse exemplo todos as aspas logo depois da contrabarra aparecem na tela, legal né? E existem algumas outras formas de usar esses caracteres:

| CARACTERE |                                         O QUE ELE FAZ                                         |
|-----------|:--------------------------------------------------------------------------------------------- |
| \n        | Nova linha. Pula para o início da próxima linha.                                              |
| \t        | Tabulação Horizontal. Funciona como a tecla tab.                                              |
| \r        | Retorno de carro. Move o cursor para o início da linha atual; não avança para a próxima linha |
| \b        | Backspace. Retrocede o cursor um caractere(come o último caractere digitado antes dele)       |
| \\'        | Possibilita escrever aspas simples em qualquer lugar do código sem interferir outras aspas.   |
| \\"        | Possibilita escrever aspas duplas em qualquer lugar do código sem interferir outras aspas.    |


Caso você queira mostrar a contrabarra, as aspas e todos os outros caracteres de escape na tela você pode usar o prefixo 'r', que significa raw.
```
#Input
print(r"Hoje o dia foi muito \"legal\"")
print(r"Quero pular para a próxima linha aqui \nE continuar na próxima")

#Output
Hoje o dia foi muito \"legal\"
Quero pular para a próxima linha aqui \nE continuar na próxima   # se você não usar o prefixo 'r' quando for colocado o '\n' seria iniciado uma nova linha e terminaria a frase
```

Obs: Quando usar o prefixo 'r' cuidado para não colocar uma contrabarra antes da último aspa, aquela que termina a string, quando você faz isso a contrabarra muda a função da aspa: como já foi visto antes, a aspa se torna parte da frase e não um sinal especial.

```
#Input
print(r"Hoje o dia foi muito \"legal\") # Isso causa um erro no programa pois não existe uma aspa para finalizar a string.
```


