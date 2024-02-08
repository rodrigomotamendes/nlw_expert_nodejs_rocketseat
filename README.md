<div align="center">
  <img src="./src/images/logo.png" width="300">
  <h1>NLW Expert - Trilha Node.js</h1>
</div>

## 🚀 Descrição

Um sistema de votação em tempo real onde os usuários podem criar uma enquete e outros usuários podem votar. O sistema gera um ranking entre as opções e atualiza os votos em tempo real.

## 🛠 Tecnologias

Tecnologias utilizadas para a criação da aplicação

- Node.JS
- TypeScript
- Docker
- Fastify
- Prisma
- Redis

## 📋 Rotas da aplicação

### HTTP

### - Post `/polls`

Crie uma nova enquete

### Request body

```json
{
  "title": "Qual melhor framework Node.js",
  "options": ["Express", "Fastify", "NestJS", "HapiJS"]
}
```

### Response body

```json
{
  "pollId": "194cef63-2ccf-46a3-aad1-aa94b2bc89b0"
}
```

### - GET `/polls/:pollId`

Retorne dados de uma única enquete.

### Response body

```json
{
  "poll": {
    "id": "e4365599-0205-4429-9808-ea1f94062a5f",
    "title": "Qual a melhor linguagem de programação?",
    "options": [
      {
        "id": "4af3fca1-91dc-4c2d-b6aa-897ad5042c84",
        "title": "JavaScript",
        "score": 1
      },
      {
        "id": "780b8e25-a40e-4301-ab32-77ebf8c79da8",
        "title": "Java",
        "score": 0
      },
      {
        "id": "539fa272-152b-478f-9f53-8472cddb7491",
        "title": "PHP",
        "score": 0
      },
      {
        "id": "ca1d4af3-347a-4d77-b08b-528b181fe80e",
        "title": "C#",
        "score": 0
      }
    ]
  }
}
```

### - Post `/polls/:pollId/votes`

Adicione um voto a uma enquete específica.

### Request body

```json
{
  "pollOptionId": "31cca9dc-15da-44d4-ad7f-12b86610fe98"
}
```

### WebSockets

### - ws `/polls/:pollId/results`

Número de votos de uma enquete.

### Message

```json
{
  "pollOptionId": "da9601cc-0b58-4395-8865-113cbdc42089",
  "votes": 2
}
```

## 🔥 Para Clonar o repositório

No terminal execute o seguinte código:

```bash
 git clone https://github.com/rodrigomotamendes/nlw_expert_nodejs_rocketseat
```

## 🔥 Executando o projeto

Utilize o **yarn** ou o **npm install** para instalar as dependências do projeto. Em seguida, inicie o setup e a aplicação.

Comando para iniciar o setup da aplicação docker.

```bash
docker compose up -d
```

Em seguida inicie a aplicação com o comando.

```bash
npm run dev
```

## 💜 Autor

Projeto criado por [rodrigomotamendes](https://www.linkedin.com/in/rodrigo-mota-mendes/)
