# api-de-games-docs
Esta API é utilizada
## Endpoints
### GET / games
Esse endpoint é responsável por retornar a listagem de todos os games cadastrados no banco de dados.
#### Parametros
Nenhum
#### Resposta
#####  Ok! 200
Caso essa resposta aconteça você vai receber a listagem de todos os games.

Exemplo de resposta:

```
[
	{
		"id": 23,
		"title": "Call of duty MW",
		"year": 2019,
		"price": 60
	},
	{
		"id": 65,
		"title": "Sea of thieves",
		"year": 2018,
		"price": 40
	},
	{
		"id": 2,
		"title": "Minecraft",
		"year": 2012,
		"price": 20
	}
]
```
##### Falha na autenticação! 401
Caso essa resposta aconteça, isso significa que aconteceu alguma falha durante o processo de autenticação da requisição. Motivos: Token inválido, Token expirado.

Exemplo de resposta:
```
{
	"err": "Token inválido"
}
```

## Endpoints
### POST / auth
Esse endpoint é responsável por fazer o processo de login.
#### Parametros
email: E-mail do usuário cadastrado no sistema

password:: Senha do usuário.
```
{
	"email": "vinicius100@live.com",
	"password": "123456"
}
```
#### Resposta
#####  Ok! 200
Caso essa resposta aconteça você vai receber o token JTW para conseguir acessar endpoints protegidos na API.

Exemplo de resposta:

```
{

```
##### Falha na autenticação! 401
Caso essa resposta aconteça, isso significa que aconteceu alguma falha durante o processo de autenticação da requisição. Motivos: Senha ou e-mail incorreto.

Exemplo de resposta:
```
{
	"err": "Credencial inválida"
}
```
