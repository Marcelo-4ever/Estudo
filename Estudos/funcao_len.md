## **Função len()**

A função **len()** conta a quantidade de índices de algo. Ela funciona com strings e outros tipos de dados que veremos futuramente(listas, dicionários, tuplas..), mas não funciona com tipos numéricos como int, float e também não funciona com o tipo bool:

```
len(1213232)
len(132.23)
len(True)

#output
ERROR
ERROR
ERROR
```

Vamos imaginar que uma senha precisa de 7 caracteres exatos para ser cadastrada, agora com a função len() podemos fazer dessa forma: 

```
senha = str(input('Digite sua senha: '))
if len(senha) == 7:
	print(f'{len(senha)} índices. Senha cadastrada')
else:
	print('Senha inválida')

#output
Digite sua senha: 1234567
7 índices. Senha cadastrada
```

Para não se confundir, lembre que essa função conta os espaços também, ou seja, `len(' ')` é igual a 1, e a cada espaço dado será +1.      

## 

Como você pode ver, ela retorna um valor inteiro, o que possibilita fazer contas sem precisar converter de um valor para o outro.  
Exemplo: 

```
a = str(input('Digite algo: '))
tamanho = len(a)
print(tamanho * 2)

#output
Digite algo: Bola # 4 índices(B, o, l, a)
8
```

E podemos fazer contas desse tipo: 

```
palavra1 = 'céu'
palavra2 = 'mar'
print(f'O total de caracteres é {len(palavra1) + len(palavra2)}')

#output
O total de caracteres é 6
```

