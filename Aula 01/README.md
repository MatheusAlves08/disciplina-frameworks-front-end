# 🎓 Faculdade SENAI Sorocaba - Página de Vendas Interativa

Esta é uma página de vendas institucional e altamente interativa desenvolvida de forma responsiva para a **Faculdade SENAI Sorocaba**. O projeto foi construído utilizando **Vanilla JS (HTML, CSS e JavaScript puros)** e empacotado com **Vite** para entregar performance ágil de desenvolvimento.

A página adota a identidade visual corporativa do SENAI (Tema Claro com as cores oficiais Azul `#0054a6` e Vermelho `#e30613`), trazendo uma proposta moderna, fluida e com alto foco em conversão e engajamento do candidato.

🔗 **Repositório GitHub**: [https://github.com/MatheusAlves08/projeto-senai-vanilla-js](https://github.com/MatheusAlves08/projeto-senai-vanilla-js)

---

## ✨ Funcionalidades Interativas

- **🎯 Quiz Vocacional ("Descubra seu Perfil")**: Um questionário interativo em 3 etapas que ajuda o candidato a encontrar seu curso ideal com base em suas afinidades de lógica, eletrônica, mecânica ou liderança.
- **💰 Simulador de ROI (Retorno sobre Investimento)**: Uma ferramenta matemática que calcula o tempo de amortização do investimento total no curso baseando-se no valor da mensalidade e na expectativa salarial local pós-formado.
- **🔍 Galeria com Hotspots Interativos**: Pontos de informação dinâmicos sobrepostos às fotos dos laboratórios (Robótica KUKA e TI Xeon), detalhando os recursos reais que o aluno operará nas aulas.
- **📚 Filtro do Catálogo de Cursos**: Seletor dinâmico que exibe os cursos conforme a categoria (Engenharias, Tecnologia ou Gestão).
- **🎓 Modais de Matrizes Curriculares**: Exibe a grade de disciplinas completa semestre a semestre de cada graduação ao clicar em "Ver Matriz".
- **💬 Carrossel de Depoimentos**: Depoimentos reais de ex-alunos inseridos nas maiores montadoras e indústrias de Sorocaba e região (Toyota, Flex, Schaeffler).
- **❓ Central de Dúvidas (FAQ) com Busca**: Accordion com pesquisa dinâmica em tempo real para ajudar na solução de dúvidas frequentes.
- **📝 Formulário LGPD Validado**: Cadastro com máscara de telefone em tempo real `(15) XXXXX-XXXX` e validações de integridade nos campos.

---

## 🛠️ Tecnologias Utilizadas

- **Estruturação**: HTML5 Semântico
- **Estilização**: CSS3 (CSS Grid, Flexbox, Keyframes, Variáveis CSS)
- **Comportamento**: Vanilla JavaScript (ES6, IntersectionObserver, CDNs como Lucide Icons)
- **Ferramental de Dev**: [Vite](https://vitejs.dev/) & Node.js

---

## 🚀 Como Executar o Projeto Localmente

### Pré-requisitos
Você precisará ter instalado em sua máquina:
- [Node.js](https://nodejs.org/) (recomendado v18 ou superior)
- NPM (incluso com o Node.js)

### Instruções

1. **Clone o repositório**:
   ```bash
   git clone https://github.com/MatheusAlves08/projeto-senai-vanilla-js.git
   ```

2. **Acesse a pasta do projeto**:
   ```bash
   cd projeto-senai-vanilla-js
   ```

3. **Instale as dependências**:
   ```bash
   npm install
   ```

4. **Inicie o servidor de desenvolvimento**:
   ```bash
   npm run dev
   ```

5. **Acesse no seu navegador**:
   Abra o endereço fornecido no terminal (geralmente [http://localhost:5173/](http://localhost:5173/)).

---

## 📦 Build para Produção

Para compilar a versão final de produção otimizada para publicação/hospedagem (gerando os arquivos finais na pasta `/dist`):
```bash
npm run build
```
