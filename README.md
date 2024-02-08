<p align="center">
  <img src="./src/images/logo.png" width="300">
</p>

<h2>🚀 Descrição</h2>

  <p>Um sistema de votação em tempo real onde os usuários podem criar uma enquete e outros usuários podem votar. O sistema gera um ranking entre as opções e atualiza os votos em tempo real.</p>

<h2>🛠 Tecnologias</h2>

<p> Tecnologias utilizadas para a criação da aplicação</p>

<u>
 <li>
  <a href='https://nodejs.org/en' target="_blank" rel="nofollow">Node.JS</a>
 </li>
 
 <li>
  <a href='https://www.typescriptlang.org/' target="_blank" rel="nofollow">TypeScript</a>
 </li>
 
 <li>
  <a href='https://www.docker.com/' target="_blank" rel="nofollow">Docker</a>
 </li>
 
 <li>
  <a href='https://fastify.dev/' target="_blank" rel="nofollow">Fastify</a>
 </li>
 
 <li>
  <a href='https://www.prisma.io/' target="_blank" rel="nofollow">Prisma</a>
 </li>
 
 <li>
  <a href='https://redis.io/' target="_blank" rel="nofollow">Redis</a>
 </li>
</u>

<h2>📋 Rotas da aplicação</h2>

<h3>HTTP</h3>

<h3>- Post <i>/polls</i> </h3>

<p>Crie uma nova enquete</p>

<h3>Request body</h3>

<div class="highlight highlight-source-shell">
 <pre>
  {
    "title": "Qual melhor framework Node.js",
    "options": ["Express","Fastify","NestJS","HapiJS"]
  }
</pre>
</div>

<h3>Response body</h3>

<div class="highlight highlight-source-shell">
 <pre>
  {
    "pollId": "194cef63-2ccf-46a3-aad1-aa94b2bc89b0"
  }
</pre>
</div>

<h3>- GET <i>/polls/:pollId</i> </h3>

<p>Retorne dados de uma única enquete.</p>

<h3>Response body</h3>

<div class="highlight highlight-source-shell">
 <pre>
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
</pre>
</div>

<h3>- Post <i>/polls/:pollId/votes</i> </h3>

<p>Adicione um voto a uma enquete específica.</p>

<h3>Request body</h3>

<div class="highlight highlight-source-shell">
 <pre>
  {
    "pollOptionId": "31cca9dc-15da-44d4-ad7f-12b86610fe98"
  }
</pre>
</div>

<h3>WebSockets</h3>

<h3>- ws <i>/polls/:pollId/results</i> </h3>

<p>Número de votos de uma enquete.</p>

<h3>Message</h3>

<div class="highlight highlight-source-shell">
 <pre>
  {
    "pollOptionId": "da9601cc-0b58-4395-8865-113cbdc42089",
    "votes": 2
  }
</pre>
</div>

<h2>🔥 Para Clonar o repositório</h2>

<p>No terminal execute o seguinte código: </p>

<div class="highlight highlight-source-shell">
 <pre>
 git clone https://github.com/rodrigomotamendes/nlw_expert_nodejs_rocketseat
</pre>

</div>

<h2>🔥 Executando o projeto</h2>

<p>Utilize o <b>yarn</b> ou o <b>npm install</b> para instalar as dependências do projeto. Em seguida, inicie o setup e a aplicação.</p>

<p>Comando para iniciar o setup da aplicação docker.</p>

<div class="highlight highlight-source-shell">
<pre>
docker compose up -d
</pre>
</div>

<p>Em seguida inicie a aplicação com o comando.</p>

<div class="highlight highlight-source-shell">
<pre>
npm run dev
</pre>
</div>

<h2>💜 Autor</h2>

<p>Projeto criado por <a href='https://www.linkedin.com/in/rodrigo-mota-mendes/' rel="nofollow">rodrigomotamendes</a></p>
