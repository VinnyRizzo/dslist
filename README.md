🎮 DSList - Projeto de Listagem de Jogos
Este projeto é uma API REST desenvolvida com Java e Spring Boot, que permite o gerenciamento e listagem de jogos. A aplicação permite obter informações como título, ano de lançamento, descrição curta e longa, gênero, plataformas, pontuação e imagem dos jogos. Os jogos são organizados em listas.

🚀 Tecnologias Utilizadas
Java 17+

Spring Boot

Spring Web

Spring Data JPA

H2 Database (para testes locais)

Maven

📦 Estrutura do Projeto
O projeto está dividido em pacotes organizados por responsabilidade:

<img width="938" height="737" alt="Image" src="https://github.com/user-attachments/assets/77a988b3-526a-4512-abec-53dfc1c7ad09" />


<img width="909" height="684" alt="Image" src="https://github.com/user-attachments/assets/22289ddf-b1db-4715-ad4c-b4731227afbf" />

Copiar
Editar
com.devsuperior.dslist
├── controllers
├── dto
├── entities
├── repositories
├── services
🧩 Entidades principais
Game: representa os dados de um jogo.

GameList: representa uma lista de jogos.

Belonging: entidade intermediária que relaciona jogos e listas, com uma posição definida.

📌 Funcionalidades
🔎 Listar todos os jogos

🗂️ Listar todas as listas de jogos

📥 Listar jogos pertencentes a uma lista específica

🧾 Informações completas sobre cada jogo

📡 Endpoints
Verbo HTTP	Endpoint	Descrição
GET	/games	Lista todos os jogos cadastrados
GET	/lists	Lista todas as listas de jogos
GET	/lists/{listId}/games	Lista todos os jogos de uma lista específica

🛠️ Como executar
Clone o repositório:

bash
Copiar
Editar
git clone https://github.com/seu-usuario/dslist.git
cd dslist
Abra o projeto em uma IDE como IntelliJ ou Eclipse

Execute o projeto

A aplicação pode ser iniciada diretamente pela IDE ou via terminal com:

bash
Copiar
Editar
./mvnw spring-boot:run
Acesse o navegador:

bash
Copiar
Editar
http://localhost:8080/games
http://localhost:8080/lists
📷 Exemplos de Resposta
/games
json
Copiar
Editar
[
  {
    "id": 1,
    "title": "The Witcher 3",
    "year": 2015,
    "shortDescription": "A breathtaking RPG in a fantasy world..."
  },
  ...
]
/lists/1/games
json
Copiar
Editar
[
  {
    "id": 3,
    "title": "Red Dead Redemption 2",
    "year": 2018,
    "shortDescription": "An epic Western action-adventure game..."
  }
]
