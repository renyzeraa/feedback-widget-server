# Widget de Feedback - Servidor 📥

Uma API RESTful construída com Node.js seguindo os princípios SOLID para coletar e gerenciar feedback de usuários.

[Repositório do Frontend](https://github.com/renyzeraa/feedback-widget-web)

## 🚀 Tecnologias

- [Node.js](https://nodejs.org/)
- [TypeScript](https://www.typescriptlang.org/)
- [Fastify](https://www.fastify.io/)
- [Prisma](https://www.prisma.io/)
- [PostgreSQL](https://www.postgresql.org/)
- [Nodemailer](https://nodemailer.com/)
- [Jest](https://jestjs.io/)
- [Zod](https://zod.dev/)

## 📋 Funcionalidades

- Envio de feedback (BUG, IDEIA, OUTRO)
- Notificações por email
- Anexos de screenshots
- Validação de entrada
- Tratamento de erros
- Testes unitários

## 🏗️ Arquitetura

O projeto segue os princípios SOLID e Clean Architecture:

- **Controllers**: Manipulam requisições/respostas HTTP
- **Casos de Uso**: Contêm a lógica de negócios
- **Repositórios**: Camada de acesso a dados
- **Entidades**: Modelos de domínio
- **Adaptadores**: Integração com serviços externos (email)

## 💻 Começando

### Pré-requisitos

- Node.js
- Docker
- Docker Compose

### Instalação

1. Clone o repositório:

```bash
git clone https://github.com/seuusuario/feedback-widget-server.git
```

2. Instale as dependências:

```bash
npm install
```

3. Crie o arquivo de ambiente:

```bash
cp .env.example .env
```

4. Inicie o banco de dados PostgreSQL:

```bash
docker-compose up -d
```

5. Execute as migrações:

```bash
npx prisma migrate dev
```

6. Na base do projeto possui a collection para realizar requisições pelo postman.

### Executando

Modo desenvolvimento:

```bash
npm run dev
```

Build de produção:

```bash
npm run build
npm start
```

Testes:

```bash
npm run test
```

## 📝 Documentação da API

### Enviar Feedback

```http
POST /api/v1/feedbacks
```

Corpo da requisição:

```json
{
  "type": "BUG", // BUG, IDEIA, OUTRO
  "comment": "Algo não está funcionando",
  "screenshot": "data:image/png;base64,..." // opcional
}
```

## 🧪 Testes

O projeto inclui testes unitários para os principais casos de uso utilizando Jest:

- Validação de envio de feedback
- Envio de email
- Validação de screenshot
- Tratamento de erros

## 📦 Variáveis de Ambiente

- `DATABASE_URL`: String de conexão PostgreSQL
- `PORT`: Porta do servidor (padrão: 3333)
- `NODE_ENV`: Ambiente (dev, test, production)

## 🛠️ Construído com Princípios SOLID

- Princípio da **R**esponsabilidade Única
- Princípio **A**berto/Fechado
- Princípio da **S**ubstituição de Liskov
- Princípio da **S**egregação de Interface
- Princípio da **I**nversão de Dependência

---

Se você tiver alguma dúvida ou sugestão, entre em contato e sinta-se à vontade para contribuir !

<img align="left" src="https://avatars.githubusercontent.com/renyzeraa?size=100">

Feito por [Renan L. Silva](https://github.com/renyzeraa)! <br>
🛠 Dev. FullStack <br>
📍 Santa Catarina - Brasil <br>

<a href="https://www.linkedin.com/in/renyzeraa" target="_blank"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn Badge" height="20"></a>&nbsp;
<a href="mailto:renansilvaytb@gmail.com" target="_blank"><img src="https://img.shields.io/badge/Gmail-D14836?style=flat&logo=gmail&logoColor=white" alt="Gmail Badge" height="20"></a>&nbsp;
<a href="#"><img src="https://img.shields.io/badge/Discord-%237289DA.svg?logo=discord&logoColor=white" title="renan_s#7826" alt="Discord Badge" height="20"></a>&nbsp;
<a href="https://www.github.com/renyzeraa" target="_blank"><img src="https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white" alt="GitHub Badge" height="20"></a>&nbsp;

<br clear="left"/>
