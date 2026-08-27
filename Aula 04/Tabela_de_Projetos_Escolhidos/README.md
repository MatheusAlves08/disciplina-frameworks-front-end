# 🚀 TaskFlow — Gerenciador de Tarefas Fullstack (API REST + React)

> 🔗 **Repositório do Projeto**: [https://github.com/MatheusAlves08/taskflow-fullstack](https://github.com/MatheusAlves08/taskflow-fullstack)

O **TaskFlow** é um projeto de aprendizado de uma aplicação web fullstack com arquitetura Monorepo:
- **Backend**: API REST construída com **Node.js** e **Express** (armazenamento de dados em memória, sem banco de dados).
- **Frontend**: Single Page Application (SPA) construída com **React**, **Vite** e estilizada com **CSS moderno / Dark Mode**.

---

## 🛠️ Tecnologias Utilizadas

### Backend
- **Node.js**: Ambiente de execução Javascript no servidor.
- **Express**: Framework web para criação de rotas e da API REST.
- **CORS**: Middleware para liberação de acessos do frontend.
- **Dotenv**: Gerenciamento de variáveis de ambiente.

### Frontend
- **React**: Biblioteca para construção da interface de usuário em componentes.
- **Vite**: Bundler rápido para projetos modernos frontend.
- **Lucide React**: Biblioteca de ícones vetoriais modernos.
- **Vanilla CSS**: Estilização personalizada com Variáveis CSS, Glassmorphism e Dark Mode.

---

## 📁 Estrutura do Projeto

```text
taskflow_api_rest/
├── backend/
│   ├── src/
│   │   └── server.js          # API REST (Endpoints GET, POST, PUT, DELETE)
│   ├── .gitignore
│   └── package.json           # Dependências e scripts do servidor
├── frontend/
│   ├── src/
│   │   ├── App.jsx            # Aplicação React e consumo da API
│   │   ├── index.css          # Estilização e Design System
│   │   └── main.jsx           # Entrypoint do React
│   ├── .env.example           # Modelo para configuração de variáveis de ambiente
│   ├── package.json           # Dependências do frontend
│   └── vite.config.js
└── README.md                  # Documentação do projeto
```

---

## 🔌 Rotas da API REST

A API do backend disponibiliza as seguintes rotas na porta `3001`:

| Método | Endpoint | Descrição | Corpo da Requisição (JSON) |
|---|---|---|---|
| `GET` | `/` | Health check (Status da API) | N/A |
| `GET` | `/api/tasks` | Retorna todas as tarefas | N/A |
| `POST` | `/api/tasks` | Cria uma nova tarefa | `{ "title": "Minha tarefa" }` |
| `PUT` | `/api/tasks/:id` | Atualiza o status/título de uma tarefa | `{ "completed": true }` |
| `DELETE` | `/api/tasks/:id` | Remove uma tarefa existente | N/A |

---

## 💻 Como Rodar o Projeto Localmente

### Pré-requisitos
Ter o **Node.js** instalado na sua máquina.

### 1️⃣ Executando o Backend
Abra um terminal na raiz do projeto e execute:
```bash
cd backend
npm run dev
```
O backend estará acessível em: `http://localhost:3001`

### 2️⃣ Executando o Frontend
Em outro terminal (na raiz do projeto):
```bash
cd frontend
npm run dev
```
Abra o navegador na URL informada no terminal (geralmente `http://localhost:5173`).

---

## 🌐 Deploy na Nuvem (Render & Vercel)

### 1. Subindo o código no GitHub
No terminal da raiz do projeto (`taskflow_api_rest`):
```bash
git init
git add .
git commit -m "feat: TaskFlow fullstack completo"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/taskflow-fullstack.git
git push -u origin main
```

### 2. Deploy do Backend no Render
1. Acesse o [Render](https://render.com) e crie uma nova conta ou faça login.
2. Clique em **New +** > **Web Service**.
3. Selecione o repositório do GitHub `taskflow-fullstack`.
4. Defina os campos:
   - **Root Directory**: `backend`
   - **Build Command**: `npm install`
   - **Start Command**: `npm start`
5. Clique em **Create Web Service**. O Render vai gerar uma URL pública como `https://taskflow-backend.onrender.com`.

### 3. Deploy do Frontend na Vercel
1. Acesse a [Vercel](https://vercel.com) e faça login com sua conta do GitHub.
2. Clique em **Add New...** > **Project** e importe o repositório `taskflow-fullstack`.
3. Configure a opção **Root Directory** para a pasta `frontend`.
4. Em **Environment Variables**, insira:
   - **Name**: `VITE_API_URL`
   - **Value**: `https://taskflow-backend.onrender.com/api/tasks` *(URL da sua API gerada pelo Render no passo anterior)*
5. Clique em **Deploy**.

---

## 📝 Licença
Este projeto foi desenvolvido para fins educacionais e de aprendizado.
