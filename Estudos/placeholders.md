## Pass e ellipsis como placeholders

Placeholders são "seguradores" de lugar, ou seja, quando você planeja escrever uma linha de código, mas não vai escrever agora, então guarda um lugar para isso.  
Temos como fazer de 2 formas: com o "pass" que foi feito para isso ou com as "ellipsis", que não foram exatamente para isso. 

```
valor = True 
if valor:
	pass # depois voltar aqui 
else:
	print('Fui')
```

```
valor = True 
if valor:
	... # as ellipsis são esses 3 pontos
else:
	print('Fui')
```

## 