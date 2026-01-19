# 🚀 Desafio Técnico: Protocolo "Stardust"

**Bem-vindo a bordo, cadete!** 👩‍🚀👨‍🚀

Estamos no ano de **2254**. A humanidade já colonizou Marte e as luas de Júpiter, mas o **Mercado de Ações Interplanetário** está um caos. O último engenheiro que tentou organizar as finanças da Federação "esqueceu" de escrever testes, causou um *overflow* num arredondamento de Créditos Solares e agora a economia da galáxia está em risco.

Você foi convocado pelo Alto Comando para liderar a construção do **"Stardust Ledger"**. Sua missão é criar uma interface segura e uma API robusta para que nossos Traders possam acompanhar seus ativos.

> **⚠️ Aviso do Comandante:** Nossa equipe de Tech Lead é obcecada por **qualidade, padronização e processos**. Não aceitamos "gambiarra espacial". Queremos ver como você constrói o software, não apenas o resultado final.

---

## 🛰️ A Missão (Escopo Técnico)

Você deve desenvolver uma aplicação Fullstack para gerenciar uma carteira de investimentos.

### 1. Backend: O Núcleo do Reator ⚛️
**Linguagens Permitidas:** Python, Node.js ou Go.

O sistema de propulsão não pode falhar. Por isso, **TDD (Test Driven Development) é o protocolo de segurança padrão.**

* **O Objetivo:** Criar uma API RESTful simples.
* **Funcionalidades (Endpoints):**
    * `POST /assets`: Registra um ativo (ex: `symbol`: "BTC", `amount`: 0.5, `price_paid`: 25000).
    * `GET /assets`: Lista todos os ativos da carteira.
    * `GET /summary`: Retorna o total investido e, se possível, uma estimativa do valor atual (pode usar dados mockados para a cotação atual).
* **Regra de Ouro (TDD):** Analisaremos a **"Caixa Preta" da nave (seu histórico do Git)**.
    * Queremos ver o ciclo **Red-Green-Refactor**.
    * Se virmos a implementação aparecendo antes do teste, ou commits gigantes com tudo pronto, a missão será abortada.

### 2. Frontend: O Painel de Controle 🖥️
**Frameworks Permitidos:** React, Vue ou Svelte.

Os monitores das naves variam de tamanho. Precisamos de um sistema modular e reutilizável.

* **Atomic Design:** Organize seus componentes em Atoms, Molecules e Organisms.
* **Storybook:** Todo componente visual (Atoms/Molecules) deve estar documentado e visível no Storybook.
* **Container/Presenter Pattern (Smart vs Dumb):**
    * **Componentes Visuais (Dumb):** Apenas recebem `props` e mostram dados. **Proibido** fazer chamadas de API aqui.
    * **Páginas/Containers (Smart):** Aqui reside a lógica. Eles buscam os dados na API e passam para os componentes visuais.
* **Testes:** Testes unitários nos componentes principais são obrigatórios.

---

## 🚫 Alertas de Perigo (Critérios de Desclassificação)

Evite as práticas que causaram a explosão da última nave:

1.  **"O Commit do Apocalipse":** Entregar o projeto todo em um único commit ("Initial commit"). Queremos ver a evolução passo a passo.
2.  **"Espaguete Espacial":** Misturar chamadas `fetch/axios` dentro de um botão ou card de apresentação.
3.  **"Falsos Positivos":** Entregar código sem testes, ou com testes que não testam a lógica real.
4.  **"Piloto Automático (IA)":** Usar IA para gerar todo o código sem critério. Saberemos identificar se você não souber explicar o que o código faz no vídeo.

---

## 📦 Protocolo de Entrega

Para submeter sua solução, siga os passos abaixo:

### 1. Repositório
Crie um repositório **público** no GitHub (ou privado e nos convide) com seu código.

### 2. Relatório da Missão (`ARCHITECTURE.md`)
Crie um arquivo chamado `ARCHITECTURE.md` na raiz do projeto. Ele deve conter:

**Parte A: Engenharia da Nave (Técnico)**
* **Decisões de Design:** Por que escolheu essas ferramentas/bibliotecas específicas?
* **Escalabilidade:** Se a Federação crescer para 1 milhão de usuários, onde o sistema falharia primeiro? O que mudaria na arquitetura?
* **Atomic Design:** Como essa estrutura ajudou na organização visual?

**Parte B: Diário de Bordo (Pessoal & Processo)**
* **Turbulências:** Qual foi a maior dificuldade técnica ou de processo que enfrentou? (Seja honesto).
* **Velocidade de Cruzeiro:** O que foi mais fácil do que esperava? O código "fluiu" em algum momento?
* **Feedback do Protocolo:** Como você se sentiu sendo "forçado" a usar TDD e separar componentes Burros/Inteligentes? Você já trabalhava assim ou teve que se adaptar?

### 3. Transmissão de Vídeo (Obrigatório) 📹
Grave um vídeo curto (Loom, YouTube, etc.) de **no máximo 5 minutos** mostrando:
* Seus testes rodando (mostre um falhando e depois passando).
* Seu Storybook em ação.
* Uma breve explicação sobre como garantiu que os componentes são reutilizáveis.

---

**Boa sorte, cadete. O futuro financeiro da galáxia está em suas mãos!** 🖖
