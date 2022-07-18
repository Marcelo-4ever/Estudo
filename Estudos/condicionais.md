## Condição ***IF, ELIF, ELSE***

Antes de explicar essas condições, vamos imaginar um usuário criando um e-mail e uma senha.        
Depois de criar e salvar o e-mail e a senha, quando ele quiser entrar novamente na conta dele vai ser necessário digitar tudo exatamente igual, então só *SE* o e-mail que ele digitar for igual ao e-mail que ele criou e *SE* a senha for igual a senha que ele criou que ele vai conseguir entrar no e-mail.    
E quando a gente pensa nas condições, *`if`* vem do inglês e significa *`se`*, então é só trocar. E caso a condição for verdadeira, ou seja, o email e a senha digitados forem igual ao email e senha criado, teremos um valor booleano True.       
Agora colocando isso como um código, ficaria assim: 

```
email = 'issoeumexemplo@gmail.com
senha = '1234'

pedir_email_usuario = input('Digite seu email: ')
if pedir_email_usuario == email: # SE o email que o usuário digitar for igual(==) ao email salvo na nossa variável
	pedir_senha_usuario = input('Digite sua senha: ')
		if pedir_senha_usuario == senha: #verificando se a senha também é igual
			print('Bem vindo!)
```

No Python a hierarquia dos códigos funciona através de espaços, que vai ser chamado de *indentação*, então quando tiver uma condição *if*, a próxima linha de código precisa ter pelo menos 1 espaço a mais que a linha anterior, mas por convenção é utilizado 4 espaços ou 1 tab.     
Quando um código tiver com muitos espaços ou tiver faltando espaços, vai ser falado por quem ler o código que há uma má identação. 

```py
nome = 'Marcelo'
if nome == 'Marcelo: 
print(f'Prazer, {nome}') # sem espaços, então está má indentado e não vai funcionar
```

```py
nome = 'Marcelo'
if nome == 'Marcelo': 
 print(f'Prazer, {nome}') # vai funcionar, mas não está com a indentação padrão
```

```py
nome = 'Marcelo'
if nome == 'Marcelo': 
	print(f'Prazer, {nome}') # bem indentado, vai funcionar
```

Perceba que o bloco de código dentro da condição if só acontece se a função for verdadeira, ou *True* em valores *booleanos*, se ela for False nada dentro do bloco irá acontecer: 

```
quantidade_gatos_no_bairro = 200
if quantidade_gatos_no_bairro == 199: 
	print('Tem 199 gatos no bairro')
print('O bloco dentro da condição if não aconteceu')

#output
O bloco dentro da condição if não aconteceu
```

Esse exemplo acima a função print que foi executada *sempre* irá acontecer, independente de existir a condição if. Mas em muitos momentos vamos precisar fazer algo como: SE tal coisa for verdade faça isso SENÃO faça essa outra coisa.          
Ainda com a história do email, e se ele digitasse a senha errada? Ou o próprio email? Vamos ver agora.


```py
email = 'issoeumexemplo@gmail.com
senha = '1234'

pedir_email_usuario = input('Digite seu email: ')
if pedir_email_usuario == email:
	pedir_senha_usuario = input('Digite sua senha: ')
		if pedir_senha_usuario == senha: 
			print('Bem vindo!')
		else:
			print('Você errou a senha!')
else: 
	print('Você errou o email!')

```

Agora toda vez que ele errar irá aparecer uma mensagem avisando que o usuário errou por causa da condição else, ou seja:     
*SE* o email estiver certo faço isso *SENÃO* faça isso aqui, *SE* a senha estiver certa faça isso *SENÃO* faço isso aqui. Simples, não?      
Mas perceba que cada if/else está indentado com a mesma quantidade de espaços,  cada um exatamente na mesma linha vertical e isso *precisa* ser sempre assim, se tiver 1 espaço ou até mesmo meio espaço - nem sei se é possível -, o código não irá funcionar.

##

Por últimos temos o elif, que é uma junção do else + if. Ele serva para quando for necessário checar várias condições até achar uma verdadeira. E o `elif` fica entre o if e o else. 
Vamos ver: 


```
nome1 = 'Roberto'
nome2 = 'Márcia'
nome3 = 'Ângelo'
nome4 = 'Nara'

nome = input('Digite seu nome: ')

if nome == nome1:
	print(f'Como você está, {nome1}? ')
elif nome == nome2:
	print(f'Como você está, {nome2}? ')
elif nome == nome3:
	print(f'Como você está, {nome3}? ')
elif nome == nome4:
	print(f'Como você está, {nome4}? ')
else:
	print('Nome desconhecido.')
```

Esse código funciona da seguinte maneira: 

1. Se o nome for igual ao nome1 ele executa a função print e o código acaba
2. Se o nome for igual ao nome2 ele executa a função print e o código acaba
3. Se o nome for igual ao nome3 ele executa a função print e o código acaba
4. Se o nome for igual ao nome4 ele executa a função print e o código acaba
5. Se o nome não for nenhum desses ele executa a função print e o código acaba

Ou seja, se o 1 for False passa para o próximo, se o 2 for False passa para o próximo, se o 3 for False passa para o próximo, se o 4 for False passa para o próximo, o 5 é o else e ele não precisa de uma expressão pedindo para verificar se algo é True/verdadeiro ou False/falso para acontecer, se chegou nele o código irá acontecer.