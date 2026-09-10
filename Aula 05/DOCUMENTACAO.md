# 📄 Documentação do Processo de Desenvolvimento e Evidências de Teste (Postman)

Este documento descreve detalhadamente todas as etapas do processo de desenvolvimento da aplicação **Projeto Notas** (API REST CRUD em Express.js + Interface Front-End em React.js), além de apresentar as evidências dos testes realizados no **Postman**.

---

## 🔗 Links Principais do Projeto

- **Repositório GitHub:** [https://github.com/MatheusAlves08/projeto-notas](https://github.com/MatheusAlves08/projeto-notas)
- **API Back-End (Render):** [https://projeto-notas-l6pd.onrender.com/api/notes](https://projeto-notas-l6pd.onrender.com/api/notes)
- **Aplicação Front-End (Vercel):** [https://projeto-notas-flax.vercel.app](https://projeto-notas-flax.vercel.app)

---

## 🛠️ 1. Processo de Desenvolvimento

O desenvolvimento da aplicação foi estruturado de forma modular e incremental, focando nas melhores práticas de arquitetura REST, versionamento com Git e hospedagem em nuvem.

### 📍 Passo 1: Inicialização e Controle de Versão
- Criação do repositório local e estruturação de pastas do projeto `projeto-notas`.
- Configuração do Git e padrão de mensagens de commit seguindo o **Conventional Commits** (`feat:`, `fix:`, `chore:`, `docs:`).

### 📍 Passo 2 & 3: Instalação das Dependências
- Instalação do servidor web **Express.js** (`npm install express`).
- Instalação do middleware **Body-Parser** (`npm install body-parser`) para manipulação de corpos de requisições HTTP em JSON.
- Instalação do **CORS** (`npm install cors`) para permitir requisições seguras entre origens cruzadas.

### 📍 Passo 4 & 5: Desenvolvimento do Back-End (`server.js`) e Banco de Dados (`data.json`)
- Criação do arquivo `data.json` contendo a estrutura de dados inicial para armazenamento persistente das notas (`id`, `titulo`, `texto`, `criadoEm`).
- Implementação das funções de leitura e escrita síncrona `readNotes()` e `saveNotes()` utilizando o módulo nativo `fs` do Node.js.
- Construção das rotas REST CRUD:
  - `GET /api/notes`: Retorna a lista completa de notas.
  - `GET /api/notes/:id`: Retorna os detalhes de uma nota específica pelo ID.
  - `POST /api/notes`: Cria uma nova nota com ID e timestamp automáticos.
  - `PUT /api/notes/:id`: Atualiza o título e texto de uma nota existente.
  - `DELETE /api/notes/:id`: Remove uma nota filtrando pelo ID.

### 📍 Passo 6: Testes Locais no Servidor Node.js
- Inicialização do servidor local na porta `3000` via `node server.js` e validação dos endpoints em ambiente de desenvolvimento.

### 📍 Passo 7: Desenvolvimento da Interface Front-End em React.js
- Criação da interface web moderna em React.js dentro do diretório `public/`.
- Uso de componentes funcionais React, gerenciamento de estado (`useState`, `useEffect`) e chamadas assíncronas `fetch()` para realizar operações de leitura, criação, edição e exclusão de notas em tempo real.
- Estilização com design moderno (glassmorphism, animações e responsividade).

### 📍 Passo 8 & 9: Deploy em Nuvem e Conexão dos Endpoints
- Publicação do repositório no GitHub: [MatheusAlves08/projeto-notas](https://github.com/MatheusAlves08/projeto-notas).
- Deploy do Back-End na plataforma **Render** (`https://projeto-notas-l6pd.onrender.com`).
- Deploy do Front-End na **Vercel** (`https://projeto-notas-flax.vercel.app`).
- Configuração dinâmica da variável `API_URL` para alternar automaticamente entre o ambiente local (`localhost:3000`) e a nuvem (`onrender.com`).

---

## 🧪 2. Testes dos Métodos HTTP no Postman (Evidências)

Todos os endpoints da API REST foram validados através do **Postman** conectando ao servidor online em produção.

---

### 1️⃣ Método `GET` - Listar todas as notas
- **Endpoint:** `GET https://projeto-notas-l6pd.onrender.com/api/notes`
- **Descrição:** Requisição para recuperar o array completo de notas armazenadas no servidor.
- **Status da Resposta:** `200 OK`

![GET Test](docs/images/get_test.png)

---

### 2️⃣ Método `POST` - Criar nova nota
- **Endpoint:** `POST https://projeto-notas-l6pd.onrender.com/api/notes`
- **Headers:** `Content-Type: application/json`
- **Corpo da Requisição (Body):**
  ```json
  {
    "titulo": "Minha Primeira Nota no Postman",
    "texto": "Testando a rota POST da API Express"
  }
  ```
- **Resposta do Servidor:** `200 OK` com o objeto da nota cadastrada contendo o `id` gerado (`1789052972999`).

![POST Test](docs/images/post_test.png)

---

### 3️⃣ Método `PUT` - Editar nota por ID
- **Endpoint:** `PUT https://projeto-notas-l6pd.onrender.com/api/notes/1789052972999`
- **Headers:** `Content-Type: application/json`
- **Corpo da Requisição (Body):**
  ```json
  {
    "titulo": "Lembretes Atualizados",
    "texto": "Comprar leite, pão e café da manhã"
  }
  ```
- **Resposta do Servidor:** `200 OK` com os campos da nota atualizados.

![PUT Test](docs/images/put_test.png)

---

### 4️⃣ Método `DELETE` - Excluir nota por ID
- **Endpoint:** `DELETE https://projeto-notas-l6pd.onrender.com/api/notes/1789052972999`
- **Descrição:** Remoção da nota cadastrada com ID `1789052972999`.
- **Resposta do Servidor:** `200 OK`
  ```json
  {
    "mensagem": "Nota removida"
  }
  ```

![DELETE Test](docs/images/delete_test.png)

---

## 📌 Conclusão
O desenvolvimento da API REST e da interface de gerenciamento de notas foi concluído com sucesso, atendendo a todos os requisitos funcionais do CRUD, persistência de dados em arquivo JSON, padrões de commit e implantação completa em ambiente de produção (Render & Vercel).
