# Aula 08 — React Lab: Catálogo de Conceitos

> **Disciplina:** Frameworks Front-End  
> **Instituição:** SENAI  
> **Semestre:** 2º Semestre  

---

## 📌 Sobre esta aula

Nesta aula desenvolvemos uma aplicação React completa do zero, chamada **React Lab — Catálogo de Conceitos**, com o objetivo de colocar em prática os seis conceitos fundamentais estudados em sala:

| Conceito | Descrição |
|---|---|
| **JSX** | Sintaxe declarativa para descrever interfaces no React |
| **Componentes** | Funções reutilizáveis que retornam JSX |
| **Props** | Mecanismo de passagem de dados entre componentes |
| **Virtual DOM** | Representação em memória que torna as atualizações eficientes |
| **Listas** | Uso de `map()` e `filter()` para renderizar coleções |
| **Renderização Condicional** | Exibição de elementos de acordo com condições (ternário, `&&`) |

---

## 🚀 Projeto desenvolvido

### React Lab — Catálogo de Conceitos

Uma landing page interativa que apresenta os conceitos fundamentais do React em cartões organizados. O usuário pode pesquisar conceitos pelo nome e a lista é filtrada em tempo real pelo React — sem manipulação manual do DOM.

**Funcionalidades:**
- Hero section com layout split e cards flutuantes animados
- Barra de pesquisa em tempo real (demonstrando Virtual DOM)
- Grid de conceitos em layout bento assimétrico
- Mensagem condicional quando nenhum resultado é encontrado
- Design responsivo (mobile, tablet e desktop)
- Landing page moderna com paleta rosa/fúcsia

---

## 🔗 Links

| | Link |
|---|---|
| **📦 Repositório GitHub** | [github.com/MatheusAlves08/react-lab-catalogo-conceitos](https://github.com/MatheusAlves08/react-lab-catalogo-conceitos) |
| **🌐 Deploy (Vercel)** | [react-lab-catalogo-conceitos.vercel.app](https://react-lab-catalogo-conceitos.vercel.app) |

---

## 🗂️ Estrutura do projeto

```
react-lab-catalogo-conceitos/
├── src/
│   ├── components/
│   │   ├── Cabecalho.jsx        # Hero section com cards flutuantes
│   │   ├── BarraDePesquisa.jsx  # Campo de busca com renderização condicional
│   │   ├── ListaDeConceitos.jsx # Bento grid com map() e condicional ternário
│   │   ├── CardConceito.jsx     # Cartão individual de conceito
│   │   └── Rodape.jsx           # Rodapé da landing page
│   ├── data/
│   │   └── conceitos.js         # Array com os 6 conceitos
│   ├── App.jsx                  # Componente principal (useState + filter)
│   ├── App.css                  # Design system e estilos
│   ├── main.jsx                 # Ponto de entrada
│   └── index.css                # Variáveis CSS globais
├── index.html
├── package.json
├── vite.config.js
└── README.md
```

---

## 🛠️ Tecnologias utilizadas

- **React 19** — Biblioteca para interfaces
- **Vite 8** — Dev server e bundler
- **JavaScript (ES6+)** — Sem TypeScript
- **CSS Vanilla** — Com variáveis CSS e design system próprio
- **Google Fonts** — Inter
- **Vercel** — Plataforma de deploy

---

## ⚙️ Como executar localmente

```bash
# Clonar o repositório
git clone https://github.com/MatheusAlves08/react-lab-catalogo-conceitos.git

# Acessar a pasta
cd react-lab-catalogo-conceitos

# Instalar dependências
npm install

# Iniciar servidor de desenvolvimento
npm run dev
```

Acesse **http://localhost:5173** no navegador.

---

## 📝 Conceitos demonstrados no código

### JSX
Toda a interface é construída com JSX. Exemplo em `CardConceito.jsx`:
```jsx
<article className="card-conceito">
  <h3 className="card-conceito__titulo">{titulo}</h3>
  <p className="card-conceito__descricao">{descricao}</p>
</article>
```

### Componentes
A interface é dividida em 5 componentes com responsabilidade única:
`Cabecalho` · `BarraDePesquisa` · `ListaDeConceitos` · `CardConceito` · `Rodape`

### Props
Dados fluem do pai para os filhos:
```jsx
<CardConceito id={1} titulo="JSX" descricao="Sintaxe declarativa..." />
```

### Virtual DOM
`useState` em `App.jsx` dispara re-renderizações sem tocar no DOM:
```jsx
const [busca, setBusca] = useState("");
```

### Listas
`filter()` + `map()` em `ListaDeConceitos.jsx`:
```jsx
{conceitos.map((conceito) => (
  <CardConceito key={conceito.id} {...conceito} />
))}
```

### Renderização Condicional
Ternário e `&&` usados em `ListaDeConceitos.jsx` e `BarraDePesquisa.jsx`:
```jsx
{conceitos.length > 0 ? <Grade /> : <MensagemVazia />}
{busca.length > 0 && <BotaoLimpar />}
```

---

*Atividade acadêmica — Frameworks Front-End · SENAI · 2026*
