# 21 perguntas de entrevista da CI&T (front-end) + como responder

Perguntas reais de uma entrevista técnica na CI&T. Para cada uma você encontra:

- **O que avaliam**: o que a pessoa entrevistadora quer descobrir de verdade.
- **Como responder**: um caminho de resposta que você adapta.
- **Evite**: o erro mais comum.

> **Importante:** os exemplos usam `[colchetes]` para você preencher com a **sua** experiência. Uma resposta com um caso real, ainda que pequeno, vale mais do que uma resposta perfeita e genérica.

## Antes de tudo: a regra que serve para quase todas

Para qualquer pergunta sobre experiência (projeto, desafio, bug, melhoria, conflito), responda em 3 passos:

1. **Problema** — qual era a situação e por que importava.
2. **Solução** — o que **você** fez (diga "eu", não só "a gente").
3. **Resultado** — o que mudou, de preferência com número ou efeito concreto.

Prepare **3 histórias** suas (um projeto, um bug difícil, um conflito ou melhoria). Com elas você responde metade das perguntas desta lista.

Dicas gerais:

- Fale **devagar**. Pausa passa segurança e dá tempo de pensar.
- Se não souber, diga o que sabe do assunto e como descobriria o resto. É melhor do que inventar.
- Se a pergunta for ambígua, confirme: *"Você quer dizer X ou Y?"*. Isso mostra critério.
- Em vagas internacionais, treine uma versão curta das respostas **em inglês**, principalmente os termos técnicos.

---

## Grupo 1 — Sobre você (4)

### 1. Fale sobre você

- **O que avaliam:** se você se comunica com clareza e se o seu perfil combina com a vaga.
- **Como responder:** use **presente → passado → futuro**, em 60 a 90 segundos.
  - Presente: *"Hoje sou desenvolvedora full stack e trabalho com [stack] em [tipo de projeto]."*
  - Passado: *"Tenho 5 anos de experiência, passei por [áreas/projetos] e aprendi [o que mais te marcou]."*
  - Futuro: *"Estou buscando [o que a vaga oferece e por que combina com você]."*
- **Evite:** contar a vida inteira ou ler o currículo em voz alta.

### 2. Fale sobre um projeto

- **O que avaliam:** se você entende o que construiu e consegue explicar. Foi aqui que muita gente trava, então ensaie.
- **Como responder:** **Problema → Solução → Resultado**, mais três itens:
  - Seu papel: *"Eu fui responsável por [parte]."*
  - A decisão técnica mais importante e **por que** a tomou.
  - O que faria diferente hoje.
- **Evite:** só listar tecnologias ("usei React, Node e AWS"). Diga qual problema elas resolveram.

### 3. Fale sobre um desafio

- **O que avaliam:** como você lida com dificuldade e o que aprende.
- **Como responder:** escolha um desafio **real e não catastrófico**. Estrutura: situação → o que era difícil → o que você fez → resultado → o que aprendeu.
- **Evite:** o desafio genérico ("prazo apertado") ou jogar a culpa nos outros.

### 4. O que você busca aprimorar como profissional?

- **O que avaliam:** autoconhecimento e se você tem plano de evolução.
- **Como responder:** cite algo **real** e mostre que já está agindo. Por exemplo: *"Estou me preparando para a certificação AWS Developer Associate, para aprofundar o uso de SDKs e segurança na nuvem. E estou trabalhando em comunicar melhor minhas decisões técnicas, inclusive produzindo conteúdo para explicar o que aprendo."*
- **Evite:** a falsa fraqueza ("sou perfeccionista") ou dizer que não tem nada a melhorar.

---

## Grupo 2 — Técnicas (6)

### 5. Como você testa o seu código?

- **O que avaliam:** se você tem hábito de qualidade, não só teoria.
- **Como responder:** explique em camadas.
  - **Testes unitários** para funções e regras de negócio (por exemplo Jest ou Vitest).
  - **Testes de componente** (Testing Library), focados no **comportamento** que a pessoa usuária vê, não na implementação interna.
  - **Testes end-to-end** (Cypress ou Playwright) para os fluxos críticos.
  - Diga o que **você realmente usa** e dê um exemplo: *"No projeto [X], cobri [fluxo] porque era o que mais quebrava."*
- **Evite:** perseguir cobertura de 100% como objetivo. Cobertura é um indicador, não a meta.

### 6. Já trabalhou com modules?

- **O que avaliam:** se você domina organização de código. A pergunta é ambígua, então **confirme**: *"Você se refere a ES Modules, à modularização do projeto ou a módulos em algum framework?"*
- **Como responder:** cubra o essencial.
  - **ES Modules** (`import`/`export`) vs. **CommonJS** (`require`/`module.exports`): sintaxe, carregamento e uso com bundlers.
  - **Modularização:** separar o código em módulos com responsabilidade clara, para facilitar manutenção e reuso.
  - **Import dinâmico** (`import()`) para carregar código sob demanda, o que ajuda na performance.
  - Exemplo: *"No projeto [X], organizei por [feature/domínio] para que cada módulo fosse independente."*
- **Evite:** responder só "sim, já usei" sem exemplo.

### 7. Já trabalhou com SPA?

- **O que avaliam:** se você entende os prós e contras da arquitetura, não só a ferramenta.
- **Como responder:**
  - **O que é:** *Single Page Application* carrega uma página e troca o conteúdo no cliente, com roteamento no front-end. A navegação fica fluida.
  - **Prós:** experiência rápida depois do carregamento e menos requisições de página inteira.
  - **Contras:** primeiro carregamento mais pesado (bundle grande), SEO mais difícil e acessibilidade de navegação que exige cuidado.
  - **Como mitiga:** code splitting, lazy loading e, quando SEO importa, SSR/SSG (como o Next.js).
  - Diga em qual projeto você usou: *"Trabalhei com SPA em React em [projeto]; em [outro], usei Next para renderização no servidor."*
- **Evite:** dizer que SPA é sempre melhor. Depende do caso.

### 8. Já precisou melhorar a performance? Como faria?

- **O que avaliam:** se você mede antes de otimizar.
- **Como responder:** **medir → achar o gargalo → agir → medir de novo.**
  1. **Medir:** Lighthouse, Chrome DevTools (aba Performance), React Profiler e métricas do Web Vitals (LCP, INP, CLS).
  2. **Gargalo:** bundle grande? Renders desnecessários? Imagens pesadas? Requisição lenta?
  3. **Ações possíveis:** code splitting e lazy loading, memoização (`React.memo`, `useMemo`, `useCallback`), virtualização de listas longas, imagens otimizadas, cache de dados, debounce em buscas.
  4. **Resultado:** *"Reduzi [métrica] de [valor] para [valor]."*
- **Evite:** sair listando técnicas sem dizer como descobriu o problema.

### 9. Como você organiza a estrutura de pastas dos projetos?

- **O que avaliam:** se você pensa em manutenção e em outras pessoas lendo seu código.
- **Como responder:** explique o **critério**, não só o desenho.
  - Duas abordagens comuns: **por tipo** (`components/`, `hooks/`, `services/`) e **por feature/domínio** (`features/login/` com tudo da feature junto). Em projetos que crescem, por feature costuma escalar melhor.
  - Mantenha junto o que muda junto (componente, estilo, teste).
  - Em Next, siga a convenção do framework (`app/` ou `pages/`) e organize o resto ao redor. No Node, por exemplo, camadas como rotas/controllers, serviços e acesso a dados, ou módulos por domínio.
  - Diga que o padrão da equipe pesa mais do que a preferência pessoal.
- **Evite:** dizer que existe uma única forma correta.

### 10. Cite hooks do React e explique (useMemo, useRef, useCallback, useEffect)

- **O que avaliam:** profundidade em React. Prepare as quatro, com **quando usar** e **quando não usar**.
- **Como responder:**
  - **`useEffect`:** executa efeitos colaterais depois da renderização, como buscar dados, assinar eventos e timers. O **array de dependências** controla quando roda, e a função de **cleanup** limpa o efeito. Erros comuns: esquecer dependência, criar loop de render e não cancelar requisição.
  - **`useRef`:** guarda um valor que **persiste entre renders sem causar nova renderização**. Usos: acessar um elemento do DOM (focar um input), guardar id de timer ou o valor anterior.
  - **`useMemo`:** memoriza o **resultado** de um cálculo caro e só recalcula quando as dependências mudam.
  - **`useCallback`:** memoriza a **referência de uma função**. Ajuda quando ela é passada para um componente filho memoizado (`React.memo`) ou usada como dependência de outro hook.
  - **Mensagem final que impressiona:** *"`useMemo` e `useCallback` são otimizações, e eu só uso quando medi um problema. Usar em tudo adiciona complexidade sem ganho."*
- **Evite:** recitar a definição sem exemplo. Dê um caso seu: *"Usei `useRef` para [x] e `useEffect` com cleanup para [y]."*

---

## Grupo 3 — Processo e engenharia (5)

### 11. Experiência com Scrum

- **O que avaliam:** se você trabalha bem em time ágil.
- **Como responder:** cite as cerimônias e **o seu papel** nelas: *planning, daily, review, retrospectiva*, o backlog e as sprints. Diga como você participa: estima tarefas, atualiza o card, levanta impedimentos, propõe melhorias na retrospectiva.
- **Evite:** recitar o guia. Se usou Kanban ou um processo híbrido, diga a verdade e explique como funcionava.

### 12. Conhecimento em CI/CD

- **O que avaliam:** se você entende o ciclo de entrega.
- **Como responder:**
  - **CI (integração contínua):** a cada push ou pull request, o pipeline roda build, lint e testes automaticamente. Isso evita que código quebrado entre na base.
  - **CD (entrega/implantação contínua):** depois que passa nos testes, o código é entregue ou implantado de forma automatizada em ambientes (homologação, produção).
  - **Sua experiência:** *"No projeto [X], o pipeline usava [ferramenta] para [etapas]."* Se você trabalha com AWS e Terraform, mencione como a infraestrutura é provisionada e implantada de forma automatizada.
- **Evite:** só dizer a sigla.

### 13. Já refatorou código?

- **O que avaliam:** se você melhora o código sem quebrar o que funciona.
- **Como responder:** Problema → como fez → resultado.
  - Por que refatorou: *"[Trecho] era difícil de manter por [motivo]."*
  - Como: **testes antes** para garantir o comportamento, mudanças em **passos pequenos**, PRs menores.
  - Resultado: *"O código ficou [mais legível/testável] e o tempo de [tarefa] caiu."*
- **Evite:** refatorar "porque estava feio", sem benefício claro.

### 14. Quais os pontos mais importantes ao fazer code review?

- **O que avaliam:** maturidade técnica e jeito de trabalhar em equipe.
- **Como responder:** liste o que você olha, em ordem de importância.
  1. **Corretude:** resolve o problema? Cobre os casos de borda?
  2. **Legibilidade e manutenção:** nomes claros, funções pequenas.
  3. **Testes:** o comportamento novo está coberto?
  4. **Segurança e performance:** dados sensíveis, validação, renders desnecessários.
  5. **Consistência** com os padrões do projeto.
  - Acrescente o **jeito**: comentários respeitosos, perguntar antes de afirmar, diferenciar o que **bloqueia** do que é **sugestão**, e manter PRs pequenos quando você é a autora.
- **Evite:** focar só em estilo e formatação, que o linter resolve.

### 15. Experiência com IA para programar

- **O que avaliam:** se você usa IA com critério.
- **Como responder:** seja honesta e mostre o seu método.
  - **Como usa:** gerar boilerplate, sugerir testes, explicar código desconhecido, acelerar pesquisa.
  - **Como valida:** revisa tudo, entende antes de aceitar, roda os testes e confere a documentação.
  - **Cuidados:** não colocar dados sensíveis ou código confidencial, e seguir a política da empresa.
  - **Mensagem final:** *"A IA acelera, mas a responsabilidade pelo código continua sendo minha."*
- **Evite:** dizer que não usa nada, ou que cola o que a IA gera sem revisar.

---

## Grupo 4 — Comportamental (6)

### 16. Como você resolveu um bug difícil?

- **O que avaliam:** seu raciocínio de investigação.
- **Como responder:** descreva o processo, não só o final.
  1. **Reproduzir** o problema de forma consistente.
  2. **Isolar:** reduzir o caso até achar onde acontece.
  3. **Levantar hipóteses** e testar uma de cada vez (logs, debugger, ferramentas do navegador).
  4. **Corrigir** e escrever um **teste de regressão**.
  5. **Documentar** a causa para o time.
  - Conte um caso real: *"No projeto [X], [sintoma]. A causa era [causa]. Resolvi [como]."*
- **Evite:** "tentei várias coisas até funcionar".

### 17. Situação em que você propôs melhoria no projeto

- **O que avaliam:** iniciativa e capacidade de convencer.
- **Como responder:** **situação → o que você notou → sua proposta → como convenceu → resultado.** Fale com quem você alinhou e como argumentou (dado, exemplo, protótipo pequeno).
- **Evite:** uma melhoria sem resultado verificável, ou que soe como crítica ao time.

### 18. Qual é sua estratégia para entender um projeto no começo?

- **O que avaliam:** como você se torna produtiva rápido num código desconhecido.
- **Como responder:**
  1. Ler o README e a documentação.
  2. **Rodar o projeto localmente** e usar o produto como usuária.
  3. Mapear o fluxo principal e a arquitetura geral.
  4. Ler os testes, que mostram o comportamento esperado.
  5. Pedir uma conversa curta com alguém do time para tirar dúvidas.
  6. Começar por uma tarefa pequena e anotar o que aprendeu (e melhorar a documentação).
- **Evite:** dizer que lê o código inteiro antes de começar.

### 19. Como você se posiciona em um conflito?

- **O que avaliam:** maturidade emocional e colaboração.
- **Como responder:**
  - **Ouvir** primeiro e entender o ponto de vista da outra pessoa.
  - Focar em **fatos e no objetivo comum**, não em quem está certo.
  - Propor uma solução ou testar as opções com dados.
  - Se não resolver, **escalar** com respeito (líder técnico ou gestor).
  - Dê um exemplo real: *"Em [situação], discordei de [decisão]. Conversei com [pessoa], mostrei [argumento] e chegamos a [resultado]."*
- **Evite:** falar mal de colegas ou dizer que "nunca teve conflito".

### 20. Como você define requisitos?

- **O que avaliam:** se você entende o problema antes de codar.
- **Como responder:**
  - Entender o **porquê** da necessidade e quem é a pessoa usuária.
  - Fazer perguntas sobre casos de borda e o que fica **fora** do escopo.
  - Definir **critérios de aceite** claros.
  - Validar com quem pediu (produto, cliente) e **registrar por escrito**, para todo mundo ficar alinhado.
  - Quebrar em tarefas pequenas e estimar.
- **Evite:** começar a implementar sem confirmar o entendimento.

### 21. O que você faria se pegasse uma task pela metade?

- **O que avaliam:** autonomia e organização.
- **Como responder:**
  1. **Ler o histórico:** commits, PR, comentários e documentação.
  2. **Falar com quem começou** para entender o contexto e o que ficou pendente.
  3. Confirmar o escopo que falta e os critérios de aceite.
  4. Evitar reescrever tudo: aproveitar o que já está certo.
  5. Documentar o que mudou e atualizar o card.
- **Evite:** descartar o trabalho anterior sem entender os motivos.

---

## Checklist rápido antes da entrevista

- [ ] Tenho 3 histórias prontas (projeto, bug, conflito/melhoria) em **Problema → Solução → Resultado**.
- [ ] Sei explicar cada projeto do meu currículo sem olhar.
- [ ] Revisei os hooks do React com um exemplo de cada.
- [ ] Treinei o "fale sobre você" em voz alta, em português e em inglês.
- [ ] Preparei 2 perguntas para fazer à empresa (equipe, processo, como medem sucesso).
- [ ] Testei câmera, microfone e internet, e deixei água por perto.
- [ ] Vou falar **devagar**.

---

## Gostou? Me segue no Instagram

Eu posto conteúdo sobre carreira em tecnologia, entrevistas, currículo, vagas abertas e dicas de AWS, sempre explicado para quem está começando.

👉 **[instagram.com/mandis.dev](https://www.instagram.com/mandis.dev/)**

Se esse material te ajudou, me conta lá nos comentários qual pergunta foi a mais difícil para você. Isso me ajuda a escolher os próximos conteúdos.
