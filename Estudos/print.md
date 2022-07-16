## Print
Print é o comando usado para imprimir algo na tela, no caso, os argumentos dentro dos parênteses.

```py
#Exemplo:
#Input
print('Marcelo', 'Ferreira') # são dois argumentos separados por vírgula e que serão imprimidos separados por um espaço.
#Output
Marcelo Ferreira
```

Se você começou python há pouquíssimo tempo, já tentou colocar aspas dentro da função print assim: 
`print('Hoje foi um dia \'legal\'')`

E recebeu uma exceção/erro, certo? O mesmo aconteceria se você trocasse todas as aspas simples para aspas duplas, e por isso existe os *caracteres de escape*. Eles consistem em você colocar uma contrabarra antes de um caractere específico, no nosso caso, as aspas. Vejamos:
```py
#input
print("Hoje foi um dia \"legal\"") 
#output
Hoje foi um dia "legal"
```

 
Os caracteres de escape são:   
|\n | Nova linha. Pula para o início da próxima linha.|   
\t - Tabulação Horizontal. Funciona como a tecla tab.   
\r - Retorno de carro. Move o cursor para o início da linha atual; não avança para a próxima linha   
\b - Backspace. Retrocede o cursor um caractere(come o último caractere digitado antes dele)                            
\\'  - Aspas simples.       
\\" - Aspas duplas.

Porém, se você quiser mostrar a contrabarra e as aspas na tela, você pode usar o prefixo 'r', que significa raw.
```
#Input
print(r"Hoje o dia foi muito \"legal\"")

#Output
Hoje o dia foi muito \"legal\"
```

Obs: Quando usar o prefixo 'r' cuidado para não colocar uma contrabarra antes da último aspa, aquela que termina a string, quando você faz isso a contrabarra muda a função da aspa: como já foi visto antes, a aspa se torna parte da frase e não um sinal especial.

```
#Input
print(r"Hoje o dia foi muito \"legal\") #Isso causará um erro no programa pois não existe uma aspa que funcione para terminar a string.
```


|p|p|p|p|
| - | - | - | - |
