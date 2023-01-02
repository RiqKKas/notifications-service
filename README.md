<h1 align="center"> Notifications Service (Serviço de Notificações) </h1>

<div align="center">
 <a href="#about">Sobre</a> |
 <a href="#entities">Entidades</a> |
 <a href="#routes">Rotas</a> |
 <a href="#technologies">Tecnologias</a> |
 <a href="#installation">Como executar</a> |
 <a href="#author">Desenvolvedor</a>
</div>

<h2 id="about">💡&nbsp; Sobre o projeto</h2>

Microsserviço de notificações desenvolvido com nestjs, a fim de desenvolver o aprendizado sobre o framework e as tecnologias que se integram a ele.

---

<h2 id="entities">👥&nbsp; Entidades </h2>

```bash
Notification {
  id          String    @id
  recipientId String
  content     String
  category    String
  readAt      DateTime?
  canceledAt  DateTime?
  createdAt   DateTime  @default(now())

  @@index([recipientId]) //phantom foreign key
}
```

---

<h2 id="routes">📍&nbsp; Rotas </h2>

- GET /notifications/count/from/:recipientId - retorna a quantidade de notificações enviadas para um recipiente
- GET /notifications/from/:recipientId - retorna todas as notificações enviadas para um recipiente
- POST /notifications - cria uma notificaçao para um determinado recipiente
- PATCH /notifications/:id/cancel - cancela uma notificação
- PATCH /notifications/:id/read - marca uma notificação como lida
- PATCH /notifications/:id/unread - marca uma notificação como não lida

---

<h2 id="concepts">📒&nbsp; Conceitos utilizados </h2>

- Inversão de Dependência (Dependency Inversion)
- Repository Pattern

---

<h2 id="technologies">🛠&nbsp; Tecnologias</h2>

Este projeto foi desenvolvido com as seguintes tecnologias:

✔️ [NodeJs](https://nodejs.org/en/)

✔️ [TypeScript](https://www.typescriptlang.org/)

✔️ [NestJs](https://nestjs.com/)

✔️ [SQLite](https://sqlite.com/index.html)

✔️ [Prisma](https://www.prisma.io/)

✔️ [Jest](https://jestjs.io/)

---

<h2 id="installation">🚀&nbsp; Como executar </h2>

```bash
# Clone o repositório
git clone https://github.com/the-riquelme/notifications-service.git

# Entre na pasta da aplicação
cd notifications-service

# Instale as dependẽncias do projeto
npm i

# Inicie o servidor
npm run start

# Acesse o servidor pelas rotas a partir de http://localhost:3000
```

<h2 id="author">👨‍💻&nbsp;Desenvolvedor</h2>

👤 [Riquelme Damião Silva](https://github.com/the-riquelme)
