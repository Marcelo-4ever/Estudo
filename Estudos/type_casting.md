
### Type Casting
---
Type casting é converter um tipo de dado em outro tipo como `int('10')`, onde a string `'10'` é convertida em um inteiro `10`. Claro que isso tem suas limitações, se você tiver uma string formada de letras ou letras e números e quiser transformar em um inteiro, o python vai mostrar um erro por que ele não consegue converter uma letra em um número.    
No type casting você só precisa colocar o nome do tipo de dado que você quer ter antes de algum valor para funcionar:
```py
int('10') # 10
int(10.0) # 10
str(10)   # '10'
str(10.0) # '10.0'
float('10') # 10.0
float(10)   # 10.0
bool(10)    # True
bool('10')  # True
```

Os valores booleanos vão retornar True ou False como já foi falado, e eles funcionam da seguinte forma: se você tiver uma comparação e for verdade ele retorna True e se for falsa ele retorna False.
```py
print(10 == 10) #10 é igual a 10? True
print(5 < 0) # 5 é menor que 0? False
```
Mas e se não tiver comparação? Bom, qualquer valor VAZIO  retorna *False* e qualquer outro valor ele vai retornar *True*:

```py
bool(10) # Tem um valor: True
bool('10') # Tem um valor: True
bool('') # String vazia: False
bool(()) # Tupla vazia: False
bool([]) # Lista vazia: False
bool({}) # Dicionário vazio: False 
```
> Esses tipos de dados que ainda não foram citadas vão ser explicados em outros tópicos no futuro. 