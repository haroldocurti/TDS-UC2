# Guia da Aula 08: Reforço Prático de Colaboração (19/05/2026)

Bem-vindos(as) a mais uma etapa prática! Como vimos na aula anterior, o fluxo de colaboração com Git e GitHub (Branches, Pull Requests) requer um pouco de prática para que os comandos se tornem instintivos.

Hoje faremos uma dinâmica ágil: cada um criará uma página base simples, atuará como contribuidor no projeto de um colega sugerindo três melhorias isoladas, e depois atuará como o dono do seu próprio projeto aprovando ou rejeitando as sugestões recebidas.

## 🎯 Objetivos da Aula
Criar "memória muscular" no uso de comandos Git e fluxo do GitHub. Consolidar os conceitos de fluxo de trabalho *Open Source* e de equipes corporativas isoladas utilizando **Forks**, múltiplas **Branches** e **Pull Requests (PRs)**. 

---

## 🧠 Competências Mobilizadas

### 📊 Indicadores (O que estamos medindo)
- **4.** Armazena as informações usando recursos local ou em nuvem, de acordo com o projeto.
- **5.** Implanta rotinas de documentação automatizadas, considerando as necessidades da produtividade e a integração com equipe de trabalho.

### 📚 Conhecimentos (O que você precisa saber)
- Trabalho em repositórios de terceiros (Conceito de *Fork*).
- Ramificações de código (*Branches*) aplicadas a *features* isoladas.
- Revisão de código e integração (*Code Review* e *Merge*).

### 🛠️ Habilidades (O que você vai fazer)
- Realizar um *Fork* pelo GitHub e clonar o repositório resultante.
- Criar e alternar entre diferentes *branches* no terminal sem perder o referencial da `main`.
- Abrir requisições de integração (*Pull Requests*) para projetos de outros desenvolvedores.
- Analisar, aprovar e reprovar alterações propostas por terceiros no seu projeto.

### 🤝 Atitudes e Valores (Como vamos nos portar)
- **Autonomia Digital:** Executar as sequências de comandos Git com segurança e repetição consciente.
- **Visão Crítica:** Avaliar criteriosamente se o código sugerido pelo seu colega deve ou não entrar no seu projeto.
- **Colaboração e Comunicação:** Sugerir melhorias claras no projeto alheio através de PRs descritivos.

---

## 🚀 Passo a Passo da Missão de Hoje

### Missão 1: Criando a sua Base 📝
Você precisa de um "terreno" para receber as contribuições dos colegas.
1. No seu **GitHub**, crie um repositório público chamado `meu-site-simples`.
2. No seu computador, abra o terminal e clone esse repositório recém-criado ou inicialize a pasta localmente (`git init`, adicione o remote, etc).
3. Abra o VS Code e crie um arquivo chamado `index.html`. 
4. Crie uma estrutura HTML muito básica, colocando seu nome e um hobby (Ex: "Bem-vindo à página do João, eu gosto de tocar violão").
5. Salve e envie para a nuvem:
   - `git add .`
   - `git commit -m "Commit inicial da minha página"`
   - `git push -u origin main`

### Missão 2: O Poder do Fork 🍴
Agora você vai escolher a página de **um colega** (combine com alguém do seu lado) para contribuir.
1. Acesse o perfil do GitHub do colega e entre no repositório `meu-site-simples` dele.
2. No canto superior direito, clique no botão **Fork**. Isso criará uma cópia idêntica do projeto do colega **na sua conta** do GitHub.
3. Agora, vá para o seu terminal e clone esse **SEU Fork**:
   ```bash
   git clone [URL-DO-SEU-FORK]
   ```
   *(Atenção: A URL deve conter o seu usuário, não o do colega!)*

### Missão 3: As Três Contribuições (Branches e PRs) 🔀
Você tem a missão de sugerir **3 melhorias separadas** para a página do seu colega.
1. No terminal do projeto clonado, certifique-se de estar na branch principal (`git status` deve mostrar `main`).
2. **Melhoria 1 (ex: Adicionar uma cor de fundo):**
   - Crie a branch isolada: `git checkout -b feature/adicionar-cor`
   - Modifique o `index.html` no VS Code. Salve.
   - Faça o commit: `git add .` e `git commit -m "Adiciona cor de fundo azul"`
   - Suba a branch: `git push -u origin feature/adicionar-cor`
   - Vá ao GitHub e abra o **Pull Request** para o repositório original do seu colega.
3. **⚠️ PASSO CRUCIAL ANTES DA MELHORIA 2:**
   - Volte para a base limpa! `git checkout main`
4. **Melhoria 2 (ex: Adicionar uma lista de filmes):**
   - Crie a nova branch: `git checkout -b feature/lista-filmes`
   - Altere, salve, faça commit e push. Abra o **segundo Pull Request**.
5. **⚠️ PASSO CRUCIAL ANTES DA MELHORIA 3:**
   - Volte para a base limpa! `git checkout main`
6. **Melhoria 3 (ex: Adicionar uma imagem):**
   - Crie a branch: `git checkout -b feature/imagem-perfil`
   - Altere, salve, faça commit e push. Abra o **terceiro Pull Request**.

### Missão 4: O Papel do Mantenedor (Code Review e Merge) 🤝
Troca de papéis! Agora você volta a ser o dono do seu projeto.
1. Acesse o seu repositório original (`meu-site-simples`) no GitHub.
2. Na aba **Pull Requests**, você deve ver as três sugestões do seu colega.
3. Analise cada uma individualmente:
   - Leia os arquivos modificados na aba *Files changed*.
   - Se gostou, clique em **Merge pull request**.
   - Se houver conflitos ou algo que não gostou, comente e peça para o colega consertar na branch dele (sim, o commit na branch do fork atualiza o PR automaticamente!).
4. Após resolver e dar os Merges no site, volte ao terminal do seu projeto original e puxe as novidades:
   ```bash
   git pull origin main
   ```

---

## 🧰 Guia de Sobrevivência (Comandos-Chave)

| Comando / Ação | O que faz? | Analogia |
| :--- | :--- | :--- |
| **Botão FORK** (No site) | Copia um repositório de outra pessoa para a sua conta. | Tirar xerox do trabalho do colega para rabiscar por cima. |
| `git clone [URL]` | Baixa o projeto da nuvem para sua máquina. | Fazer o download do projeto para sua mesa de trabalho. |
| `git checkout -b [nome]` | Cria uma nova branch e já muda para ela imediatamente. | Separar uma folha limpa para rascunhar uma nova ideia isoladamente. |
| `git checkout main` | Volta para a ramificação principal oficial. | Guardar os rascunhos e voltar a olhar para o documento original, limpo, para basear a próxima ideia. |
| `git pull origin main` | Puxa as atualizações do GitHub para o seu computador. | Sincronizar sua pasta local com o que foi aprovado na nuvem. |

Bora praticar! A repetição é a chave do aprendizado! 🚀
