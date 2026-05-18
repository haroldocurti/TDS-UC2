# Guia da Aula 07: Trabalho Colaborativo na Prática (18/05/2026)

Bem-vindos(as) a mais uma etapa prática! Hoje sairemos do trabalho individual e passaremos a simular o dia a dia real de uma equipe de desenvolvimento de software.

## 🎯 Objetivos da Aula
A aula será uma simulação do ambiente corporativo de TI. Vamos integrar seus conhecimentos de controle de versão (Git/GitHub - UC2) com os códigos da linguagem JavaScript e Node.js (UC5). 
Vocês vivenciarão o fluxo completo que um desenvolvedor enfrenta ao chegar no trabalho: ler tickets de problemas num Kanban (MS Planner), isolar seu ambiente criando *branches*, corrigir o código e pedir para a equipe revisar sua solução usando *Pull Requests*.

---

## 🧠 Competências Mobilizadas

### 📊 Indicadores (O que estamos medindo)
- **4.** Armazena as informações usando recursos local ou em nuvem, de acordo com o projeto.
- **5.** Implanta rotinas de documentação automatizadas, considerando as necessidades da produtividade e a integração com equipe de trabalho.

### 📚 Conhecimentos (O que você precisa saber)
- Sistemas de controle de versão distribuído (Git).
- Gestão de repositórios remotos (GitHub).
- Ramificações de código (*Branches*).
- Revisão de código em equipe (*Pull Requests* e *Merge*).
- Interpretação e depuração de pequenos scripts em Node.js.

### 🛠️ Habilidades (O que você vai fazer)
- Baixar (*clonar*) repositórios em nuvem para a máquina local.
- Navegar e selecionar tarefas a partir de um sistema ágil de tickets (MS Planner).
- Isolar ambientes de desenvolvimento criando e alternando entre `branches`.
- Solicitar a integração do seu código no projeto principal através de revisão por pares.

### 🤝 Atitudes e Valores (Como vamos nos portar)
- **Colaboração e Comunicação:** Trabalhar em harmonia e clareza nas revisões de código.
- **Autonomia Digital:** Capacidade de buscar, baixar e resolver problemas de forma independente usando o sistema de tickets.
- **Visão Crítica:** Analisar o código de outro desenvolvedor que contém erros e propor a solução mais adequada sem afetar o resto da aplicação.

---

## 🚀 Passo a Passo da Missão de Hoje

### Missão 1: Sincronização Total 🏁
Sua primeira tarefa do dia é garantir que as aulas passadas não foram em vão.
1. Abra as pastas dos seus projetos locais (UC1, UC2 e UC5).
2. Certifique-se de que todas as alterações feitas até hoje estão aterrissadas na nuvem. Use o ciclo que vocês já dominam:
   - `git status` (para ver o que falta salvar)
   - `git add .` (para preparar os arquivos)
   - `git commit -m "Sua mensagem clara e direta"` (para empacotar e rotular)
   - `git push` (para enviar ao GitHub)

### Missão 2: Entrando no Projeto da Equipe (O Clone) 📦
O professor preparou um repositório central contendo mini-aplicações em Node.js (integração com a UC5). Porém, há bugs propositais espalhados pelos arquivos.
1. Acesse o **MS Planner** com a sua conta. Lá você verá o quadro do projeto com diversos "Tickets" detalhando os problemas relatados nessas aplicações.
2. Copie a URL do repositório central fornecida pelo professor.
3. No seu terminal (abra em uma pasta neutra onde você organiza seus projetos, **fora** de um repositório já existente), baixe o projeto completo:
   ```bash
   git clone [URL-DO-REPOSITORIO]
   ```

### Missão 3: Isolando seu Trabalho (Branches) 🔀
**Regra de Ouro Corporativa:** Em equipe, nunca se programa diretamente na versão "oficial" (a branch `main`).
1. Escolha no MS Planner (ou receba atribuído a você) **pelo menos 2 tickets** para resolver.
2. No terminal do projeto clonado, crie uma área isolada apenas para corrigir o **primeiro** erro:
   ```bash
   git checkout -b fix/nome-do-erro-1
   ```
3. Abra o VS Code, encontre o erro relatado pelo ticket no código JavaScript, corrija-o e faça um teste.
4. Salve sua correção no seu ambiente isolado (*branch* atual):
   ```bash
   git add .
   git commit -m "Corrigindo o erro X conforme ticket Y"
   ```
5. Envie essa *branch* contendo a correção para a nuvem:
   ```bash
   git push -u origin fix/nome-do-erro-1
   ```
6. **Importante - Repetindo o processo para o segundo erro:** 
   - Volte para a versão limpa oficial do projeto: `git checkout main`
   - (Opcional, mas recomendado) Veja se há novidades: `git pull`
   - Crie a nova *branch* para o ticket 2: `git checkout -b fix/nome-do-erro-2` e repita os passos 3, 4 e 5.

### Missão 4: Solicitando Revisão (Pull Request) 🤝
O seu código corrigido está salvo na nuvem dentro das suas *branches* isoladas. Agora precisamos pedir que o Tech Lead (o professor) junte o seu conserto ao projeto oficial.
1. Acesse o repositório no GitHub pelo navegador.
2. Você verá um aviso em amarelo com um botão **"Compare & pull request"**. Clique nele.
3. Preencha o formulário: Escreva o que você alterou e cite o número/nome do ticket do Planner que está sendo resolvido.
4. Confirme a criação do Pull Request (PR).
5. O professor atuará como *Tech Lead*, revisando seu código.
   - **Aprovado (Merge):** Sua correção fará parte da versão oficial.
   - **Solicitação de Ajuste:** O professor comentará o que precisa mudar. Você deverá voltar ao VS Code, na mesma branch, alterar, fazer commit e dar push novamente.

---

## 🧰 Guia de Sobrevivência (Comandos-Chave)

| Comando | O que faz? | Analogia |
| :--- | :--- | :--- |
| `git clone [URL]` | Baixa o projeto inteiro da nuvem para sua máquina. | Fazer o download do "trabalho base do grupo". |
| `git branch` | Lista as ramificações (*branches*) locais. | Ver quais "rascunhos" você tem guardados na gaveta. |
| `git checkout -b [nome]` | Cria uma nova branch e já muda para ela imediatamente. | Tirar uma cópia do documento oficial para rascunhar sem medo de quebrar o original. |
| `git checkout main` | Volta para a ramificação principal oficial. | Guardar os rascunhos e voltar a olhar para o documento original. |
| `git push -u origin [nome-da-branch]`| Envia a sua branch para o GitHub. | Colocar o seu rascunho na nuvem para a equipe poder visualizar. |

Bom código e bons Pull Requests, equipe! 🚀
