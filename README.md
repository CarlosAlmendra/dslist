# DSLIST

DSLIST é um software que permite buscar um jogo ou uma lista de jogos através de requisições HTTP. Além disso, ele oferece uma funcionalidade interativa onde é possível arrastar a posição dos jogos dentro da lista, movimentando-os entre a posição inicial e a posição final.

## Tecnologias Utilizadas

- **Java**
- **Spring Boot**
- **JPA / Hibernate**
- **H2 Database / PostgreSQL**

## Funcionalidades

- Buscar um jogo específico por ID.
- Listar todos os jogos cadastrados.
- Movimentar a posição dos jogos dentro da lista via requisição HTTP.
- Gerenciar jogos utilizando um banco de dados relacional.

## Como Executar o Projeto

### Backend

1. Clone o repositório:
   ```bash
   git clone https://github.com/CarlosAlmendra/dslist.git
   ```
2. Acesse o diretório do projeto:
   ```bash
   cd dslist
   ```
3. Execute a aplicação Spring Boot:
   ```bash
   ./mvnw spring-boot:run
   ```

## Endpoints Principais

### Buscar Todos os Jogos
```http
GET /games
```
Retorna uma lista com todos os jogos cadastrados.

### Buscar um Jogo por ID
```http
GET /games/{id}
```
Retorna os detalhes de um jogo específico.

### Retornar uma lista de Jogos
```http
GET /{listId}/games
```
Retorna todos os jogos de uma lista.

### Mover um Jogo na Lista
```http
POST /{listId}/replacement
```
Move o jogo para uma nova posição dentro da lista, passando um body:
```{
	"sourceIndex": 1,
    "destinationIndex": 4
}
```
Onde sourceIndex é a posição atual do jogo, e destinationIndex é a posição final,
onde será feito o reposicionamento.

## Contribuição

Sinta-se à vontade para contribuir com melhorias! Basta seguir os passos:
1. Faça um fork do repositório
2. Crie uma nova branch: `git checkout -b Nome_da_feature`
3. Faça suas alterações e commit: `git commit -m 'Nome_da_feature'`
4. Envie um pull request


Feito por Carlos Henrique Almendra (https://github.com/CarlosAlmendra)

