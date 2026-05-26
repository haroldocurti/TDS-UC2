# Guia da Aula 09: Inteligência Artificial na Escrita Técnica (26/05/2026)

Bem-vindos(as) à nossa preparação para o Projeto Integrador (PI)! A partir de agora, vocês vão projetar e construir aplicações reais. Para que o projeto seja profissional, a escrita técnica e a documentação (requisitos, escopo, READMEs, contratos de equipe) são tão importantes quanto o próprio código.

Hoje faremos um **Crash Course interativo sobre Inteligência Artificial (IA)**. Vamos aprender como os desenvolvedores modernos utilizam assistentes de IA de forma produtiva e crítica. Passaremos desde o funcionamento básico e a identificação de alucinações, até a engenharia de prompts avançada e o uso inteligente de assistentes na IDE com engenharia de contexto.

---

## 🎯 Objetivos da Aula
- Compreender a mecânica básica de funcionamento de LLMs (modelos de linguagem) e como mitigar alucinações.
- Desenvolver habilidades de **Engenharia de Prompts** para estruturar a escrita técnica e gerar artefatos em Markdown.
- Utilizar recursos de **Engenharia de Contexto** dentro da IDE para gerar documentação integrada ao código existente.
- Iniciar a base documental do Projeto Integrador utilizando assistentes virtuais de forma guiada e analítica.

---

## 🧠 Competências Mobilizadas

### 📊 Indicadores (O que estamos avaliando)
- **3.** Seleciona a ferramenta de documentação, de acordo com o projeto de software desenvolvido.
- **5.** Implanta rotinas de documentação automatizadas, considerando as necessidades da produtividade e a integração com equipe de trabalho.

### 📚 Conhecimentos (O que você precisa saber)
- O que são LLMs, mecanismos probabilísticos e alucinações.
- Pilares da Engenharia de Prompts (System Prompt, Contexto, Instrução, Exemplos - Few-shot, Restrições e Delimitadores).
- Engenharia de Contexto em IDEs (Uso de arquivos locais, árvore de diretórios e comandos contextuais em assistentes como Copilot, Cursor ou Claude Code).

### 🛠️ Habilidades (O que você vai fazer)
- Escrever instruções estruturadas para guiar a geração de documentação por IAs.
- Usar extensões de IA na IDE para produzir documentações e comentários associados ao código real.
- Analisar criticamente, corrigir e formatar textos técnicos gerados artificialmente.

### 🤝 Atitudes e Valores (Como vamos nos portar)
- **Visão Crítica:** Avaliar com rigor as respostas geradas por IA, compreendendo que ela é um copiloto probabilístico, não um tomador de decisão consciente.
- **Autonomia Digital:** Saber configurar o contexto e os delimitadores ideais na IDE para que o assistente gere saídas altamente assertivas.

---

## 🚀 Passo a Passo da Missão de Hoje

### Missão 1: O Chatbot Genérico e o Problema da Alucinação 🧠
Você vai testar como uma IA reage a instruções vagas e como ela pode "inventar" detalhes técnicos.
1. Abra um chatbot de navegador (como Gemini, ChatGPT ou Claude).
2. Envie um prompt simples e sem contexto:
   > *"Faça uma proposta comercial e um escopo técnico para um aplicativo de delivery."*
3. Analise atentamente a resposta. Copie o texto e marque em seu editor:
   - Quais partes são clichês ou vagas?
   - Onde o chatbot assumiu regras que você não especificou?
   - Identifique possíveis "alucinações" (ex: tecnologias incompatíveis ou recursos exagerados que não caberiam em um MVP ágil).

---

### Missão 2: Escrevendo Prompts Profissionais (Engenharia de Prompts) ✍️
Agora você vai aplicar técnicas formais de Engenharia de Prompts para obter um documento de requisitos preciso.
1. Use as técnicas aprendidas de **Persona**, **Contexto**, **Instrução** e **Restrição**.
2. Formule um novo prompt estruturado no chatbot. Siga este modelo mental:
   > **Aja como:** Um Engenheiro de Requisitos Sênior especializado em metodologias ágeis.
   >
   > **Contexto:** Nosso projeto é um MVP de um aplicativo de delivery local focado apenas em pequenas padarias de bairro. A equipe é formada por 3 desenvolvedores juniores e temos 1 mês de prazo.
   >
   > **Restrições:** O aplicativo NÃO terá sistema de pagamento online neste MVP (será pago apenas na entrega). Não utilize termos genéricos como "tecnologia de ponta" ou "plataforma inovadora".
   >
   > **Instrução:** Escreva a seção de "Escopo do MVP e Requisitos Funcionais Principais" em formato de tabela Markdown.
3. Compare a qualidade, a precisão e a utilidade prática deste documento com o resultado gerado na Missão 1.

---

### Missão 3: Engenharia de Contexto na IDE (Alimentando com Código Real) 🗂️
Chegou a hora de sair do navegador e trabalhar na IDE (VS Code com Copilot/Cursor, ou linha de comando com Antigravity/Claude Code), onde a IA consegue "ler" seus arquivos reais.
1. Abra a pasta do projeto da aula anterior (`meu-site-simples` ou seu projeto de código JavaScript da UC5) no VS Code.
2. Abra o chat integrado da IDE ou utilize os comandos de contexto (como `@workspace`, `#file` ou simplesmente selecione o código desejado).
3. Faça com que o assistente escreva a documentação técnica com base no seu código real:
   - **Exemplo de instrução contextual:** *"@workspace Crie um arquivo README.md detalhando o funcionamento deste repositório, incluindo como rodar a aplicação localmente e explicando a estrutura de pastas existente."*
   - Ou selecione uma função JavaScript que você escreveu e peça: *"Gere a documentação dessa função em formato JSDoc, explicando cada parâmetro."*
4. Repare como a IA não alucina, pois ela tem acesso ao código fonte real como contexto do prompt.

---

### Missão 4: Pastas de Agentes e Automação de Repositórios 🚀
Agora você vai aprender como customizar as instruções de um assistente de IA criando uma pasta de regras na raiz do seu projeto. O objetivo é criar um agente de organização que automatizará a estruturação da sua pasta de desenvolvimento (`/dev` ou sua pasta de exercícios) e fará o envio automático para o GitHub.

1. **Configurando a Pasta de Regras:**
   - Na raiz do seu repositório local, crie um arquivo de regras locais. O nome do arquivo depende do assistente que você está usando (ex: `.cursorrules` se usar o Cursor, `.github/prompts/organizar.md` ou `.copilot/instructions.md` no VS Code, ou `.agent/rules.md` em sistemas autônomos).
2. **Escrevendo as Regras do Agente:**
   - Abra o arquivo de regras criado e cole as seguintes instruções (ajuste-as como quiser):
     ```markdown
     # Regras do Agente de Organização do Diretório Dev

     Você é um agente especialista em refatoração e limpeza de repositórios. Sua missão é organizar a pasta `/dev`.

     Siga estritamente estas diretrizes ao receber o comando de organização:
     1. Analise todos os arquivos de código na pasta `/dev`.
     2. Renomeie arquivos que tenham espaços no nome ou letras maiúsculas misturadas para o formato kebab-case (ex: `Meu Exercicio.js` vira `meu-exercicio.js`).
     3. Remova arquivos temporários vazios ou sem extensão que sejam lixo.
     4. Crie um arquivo `README.md` dentro de `/dev` com um sumário elegante em tabela, listando todos os arquivos da pasta e explicando resumidamente o que cada código faz.
     5. Realize o commit das mudanças usando o padrão de commits semânticos: `git add .` e `git commit -m "style: organiza diretório dev e atualiza readme"`.
     6. Envie as alterações para o repositório remoto: `git push origin main`.
     ```
3. **Invocando a Automação (Tooling na prática):**
   - Abra o chat do assistente de IA da IDE ou a linha de comando do agente (como Claude Code ou Antigravity).
   - Peça: *"Leia as regras do meu arquivo de configuração e execute a organização da pasta dev."*
4. **⚠️ VISÃO CRÍTICA (Muito importante):**
   - Assista à IA executando os passos (lendo os arquivos, editando o README, rodando comandos Git).
   - O assistente pedirá sua permissão para rodar comandos de gravação, commits e pushes. **Analise detalhadamente o que o agente pretende fazer antes de clicar em APROVAR.**
   - Garanta que ele não está deletando códigos importantes antes de aceitar.

---

## 🧰 Guia de Sobrevivência (Conceitos-Chave)

| Termo / Conceito | O que significa na prática? | Como usar a seu favor |
| :--- | :--- | :--- |
| **Alucinação** | Respostas factualmente erradas que a IA gera com alta confiança estatística. | Nunca copie código ou texto técnico sem revisar linha por linha. |
| **Prompt Engineering** | A estruturação correta de regras, personas e exemplos no prompt. | Diga claramente quem a IA é, o que ela deve fazer e o que ela **NÃO** pode fazer. |
| **Janela de Contexto** | O limite de informações (memória de curto prazo) que a IA consegue processar de uma só vez. | Evite enviar arquivos gigantescos e desnecessários; passe apenas os arquivos relevantes. |
| **Engenharia de Contexto** | Fornecer arquivos locais e a árvore de diretórios para alimentar o prompt de forma específica. | Use comandos como `@workspace`, `#file:nome_do_arquivo` ou cole trechos de código exatos no chat da IDE. |
| **Pastas de Agentes (`.agent`, `.github`, `.copilot`)** | Diretórios ou arquivos especiais na raiz do repositório onde definimos diretrizes personalizadas que a IA lê antes de interagir com o projeto. | Crie arquivos de regras customizadas para ensinar à IA os padrões de design, commits e nomenclatura da sua equipe. |
| **Tooling & Skills** | Capacidade de um agente de IA de usar ferramentas externas (ex: ler arquivos do computador, rodar comandos Git, rodar testes). | Permita que assistentes executem tarefas rotineiras de escrita e versionamento, mantendo sempre o papel de revisor final. |

A IA é um ótimo acelerador de produtividade, mas o **cérebro do projeto** e a **decisão final** continuam sendo seus! Bom trabalho! 🚀
