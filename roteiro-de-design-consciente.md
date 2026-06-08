# Roteiro de Design Consciente
### Sistema de Apoio à Decisão (SAD) para o Desenvolvimento de Jogos Psicologicamente Seguros

Isaac Wanderson de Pontes Xavier — Orientador: Prof. Fabricio Carneiro Costa
Centro Universitário Paraíso (UniFAP) — Sistemas de Informação — Juazeiro do Norte, 2026

---

## Apresentação

O Roteiro de Design Consciente é um Sistema de Apoio à Decisão (SAD) metodológico desenvolvido para auxiliar criadores de jogos digitais, iniciantes ou experientes, a tomar decisões de design que priorizem o bem-estar e a segurança psicológica dos jogadores. Ele não substitui a criatividade do desenvolvedor: instrumentaliza essa criatividade com consciência ética fundamentada em psicologia científica.

O roteiro está organizado em quatro fases sequenciais, cada uma correspondendo a um momento distinto do processo de criação de um jogo. Em cada fase, o desenvolvedor encontrará perguntas reflexivas para guiar suas decisões, diretrizes práticas baseadas nos Padrões Radiantes e alertas sobre Dark Patterns a evitar. O processo é linear — a Fase 1 deve ser concluída antes da Fase 2, e assim por diante —, mas cada fase pode ser revisitada sempre que uma nova decisão de design precisar ser avaliada.

### Visão geral das quatro fases

| Fase | Nome | Foco | Necessidade TAD acionada |
|------|------|------|--------------------------|
| 1 | Conceito e intenção ética | Definir o norte psicológico do projeto antes de qualquer decisão técnica | Autonomia (todas) |
| 2 | Mecânicas e sistemas | Traduzir a intenção ética em sistemas concretos de jogo | Competência + Flow |
| 3 | Narrativa e personagens | Construir conexões emocionais genuínas e seguras | Relacionamento |
| 4 | Interface e UX | Garantir que a interface seja honesta, clara e acessível | Autonomia + Competência + Flow |

---

## FASE 1 — CONCEITO E INTENÇÃO ÉTICA

**Objetivo:** antes de qualquer decisão técnica — antes de escolher engine, mecânicas ou estética — definir com clareza qual experiência emocional o jogo pretende criar e como ele respeitará a Autonomia do jogador. Esta fase garante que o design consciente comece na intenção, e não seja adicionado como correção no final.

### 1.1 Perguntas reflexivas

| # | Pergunta | Necessidade TAD |
|---|----------|-----------------|
| P1 | Qual é a emoção central que você deseja que o jogador sinta ao encerrar uma sessão? (Ex: realização, tranquilidade, curiosidade, conexão) | Autonomia — intenção do design |
| P2 | Quem é o seu jogador? Que necessidades psicológicas ele tem que este jogo pode atender de forma genuína? | Autonomia + Relacionamento |
| P3 | O jogador pode sair, pausar e retornar exatamente de onde parou, sem qualquer penalidade ou perda de progresso? | Autonomia Temporal |
| P4 | Existe algum conteúdo que expira, desaparece ou se torna inacessível pela simples ausência do jogador? | Autonomia — FOMO (Dark Pattern) |
| P5 | O jogo exige que o jogador retorne em horários específicos para não perder recompensas? | Autonomia — Daily Login (Dark Pattern) |
| P6 | Existe alguma mecânica de monetização planejada? Como ela evita a exploração do jogador? | Autonomia + Competência |
| P7 | O jogo foi projetado para ter um fim natural ou para reter o jogador indefinidamente por dependência? | Autonomia — retenção compulsória |
| P8 | Há algum elemento que possa gerar ansiedade, vergonha pública ou medo de perder? Como será tratado? | Autonomia + Relacionamento |

### 1.2 Diretrizes (Padrões Radiantes)

| # | Diretriz | Dark Pattern substituído | Referência |
|---|----------|--------------------------|------------|
| D1 | O jogador pode pausar e salvar a qualquer momento, em qualquer estado do jogo, sem exceção. | Can't Pause / Can't Save | Miranda e Darin (2022) |
| D2 | Nenhum conteúdo expira por calendário real. Eventos sazonais retornam ciclicamente; itens não desaparecem pela ausência. | FOMO | Zagal et al. (2013) |
| D3 | Elimine qualquer recompensa condicionada à presença diária (Daily Login). O retorno deve ser intrínseco. | Daily Login Reward | darkpattern.games |
| D4 | Inclua ao menos uma escolha expressiva de identidade (nome, pronome, aparência) reconhecida ao longo de toda a experiência. | Identidade forçada | Ryan e Deci (2000) |
| D5 | Se houver monetização, adote compra única ou assinatura transparente. Todo conteúdo relevante acessível sem pagamento adicional. | Pay-to-Win / Moeda Premium | Zagal et al. (2013) |
| D6 | O jogo pode ser encerrado a qualquer momento sem que o jogador sinta que está perdendo algo. | Wait to Play | darkpattern.games |

> **Alerta da Fase 1:** se o conceito depende de que o jogador "não consiga parar de jogar" como proposta de valor central, ou se a retenção se baseia em medo de perda em vez de desejo genuíno, o projeto apresenta risco de design manipulativo. Revisar antes de avançar.

### 1.3 Checklist de encerramento (todos devem estar "Sim")

- [ ] A intenção emocional do jogo está documentada explicitamente.
- [ ] O jogador pode pausar e sair a qualquer momento sem penalidade.
- [ ] Nenhum conteúdo expira por ausência do jogador.
- [ ] Não há recompensa diária condicionada ao retorno.
- [ ] A monetização (se houver) não cria vantagem injusta.
- [ ] O jogo tem fim natural ou progressão significativa; não retém por dependência.
- [ ] Há ao menos uma escolha de identidade expressiva para o jogador.

---

## FASE 2 — MECÂNICAS E SISTEMAS

**Objetivo:** avaliar cada mecânica planejada pelo seu impacto nas necessidades de Competência e Flow. Esta fase impede que decisões técnicas aparentemente neutras introduzam Dark Patterns no sistema, especialmente os mais sutis, como recompensas variáveis e grinding disfarçado.

### 2.1 Perguntas reflexivas

| # | Pergunta | Necessidade TAD |
|---|----------|-----------------|
| P1 | Para cada mecânica principal: ela satisfaz qual necessidade da TAD? | Competência + Autonomia |
| P2 | O sistema de recompensas é 100% previsível? | Competência — Variable Reward |
| P3 | Existe recompensa gerada por aleatoriedade paga (loot box, gacha)? Como será eliminada? | Competência — Variable Reward |
| P4 | A curva de dificuldade foi mapeada? Onde fica fácil demais (tédio) e difícil demais (ansiedade)? | Flow |
| P5 | O que acontece quando o jogador falha? A falha é recuperável, instrutiva e clara? | Competência — punição irreversível |
| P6 | O feedback visual e sonoro é honesto? Nenhum efeito estético embeleza um resultado negativo? | Competência — manipulação estética |
| P7 | Há mecânicas que exijam repetição forçada sem significado (grinding)? Como redesenhá-las? | Competência — Grinding |
| P8 | O jogo tem objetivos claros de curto prazo em cada sessão? | Flow — objetivos claros |

### 2.2 Diretrizes (Padrões Radiantes)

| # | Diretriz | Dark Pattern substituído | Referência |
|---|----------|--------------------------|------------|
| D1 | Recompensas 100% previsíveis: o jogador sabe o que vai ganhar antes de agir. Proibida recompensa variável aleatória paga. | Variable Reward / Loot Boxes | Zagal et al. (2013); ICC (2024) |
| D2 | A dificuldade cresce organicamente; cada camada emerge do domínio da anterior. Proibido muro artificial que induz pagamento. | Grinding / Pay-to-Skip | darkpattern.games |
| D3 | Feedback honesto: ação positiva → feedback positivo; ação neutra → feedback neutro. Nenhum efeito mascara resultado negativo. | Manipulação estética | Zagal et al. (2013) |
| D4 | Falhas não permanentes nem com reinício de progresso longo. O erro é instrutivo, antecipado e reversível. | Punição irreversível | Miranda e Darin (2022) |
| D5 | Toda progressão é consequência exclusiva do esforço e do aprendizado. Proibida vantagem comercializável. | Pay-to-Win | Zagal et al. (2013) |
| D6 | Cada sessão tem objetivos claros e alcançáveis de curto prazo. | Objetivos ambíguos | Csikszentmihalyi (1990) |

### 2.3 Checklist de encerramento

- [ ] Todas as mecânicas principais foram avaliadas.
- [ ] Nenhuma recompensa é gerada por aleatoriedade paga.
- [ ] A curva de dificuldade foi mapeada e não tem picos punitivos.
- [ ] Falhas são recuperáveis e comunicadas com antecedência.
- [ ] Feedback visual/sonoro é honesto com o resultado real da ação.
- [ ] Não há grinding forçado sem sentido narrativo ou mecânico.
- [ ] Cada sessão tem objetivos claros de curto prazo.

---

## FASE 3 — NARRATIVA E PERSONAGENS

**Objetivo:** narrativa e personagens são os principais vetores de satisfação do Relacionamento. Esta fase garante que as conexões emocionais sejam baseadas em empatia genuína, nunca em obrigação social, vergonha ou medo de perder vínculos.

### 3.1 Perguntas reflexivas

| # | Pergunta | Necessidade TAD |
|---|----------|-----------------|
| P1 | Qual é a jornada emocional do jogador? Há equilíbrio entre tensão, alívio, conquista e conexão? | Relacionamento + Competência |
| P2 | Os personagens têm motivações compreensíveis, falhas humanizantes e vulnerabilidades visíveis? | Relacionamento |
| P3 | As escolhas narrativas têm impacto real ou são meramente estéticas? | Autonomia Decisória |
| P4 | As interações com NPCs ou outros jogadores são completamente opcionais para a progressão? | Relacionamento — Social Obligation |
| P5 | Há temas sensíveis (luto, trauma, doença mental)? Há aviso de conteúdo antes de cenas impactantes? | Segurança psicológica |
| P6 | A representatividade é inclusiva? Diferentes identidades se veem representadas? | Relacionamento — pertencimento |
| P7 | Há rankings públicos ou sistemas que exponham o jogador negativamente? | Relacionamento — Rankings |
| P8 | Ao menos um momento narrativo estimula a empatia genuína? | Relacionamento |

### 3.2 Diretrizes (Padrões Radiantes)

| # | Diretriz | Dark Pattern substituído | Referência |
|---|----------|--------------------------|------------|
| D1 | Cada NPC principal tem ao menos uma vulnerabilidade emocional visível; não é mero dispensador de missões. | NPCs rasos | Miranda e Darin (2022) |
| D2 | Decisões narrativas têm ao menos duas consequências distintas e perceptíveis. Proibidas escolhas ilusórias. | Escolhas ilusórias | Ryan e Deci (2000) |
| D3 | Interações sociais são sempre opcionais; nenhuma é pré-requisito para a progressão principal. | Social Obligation | Zagal et al. (2013) |
| D4 | Proibidos rankings públicos ou comparação negativa. Elemento competitivo, se houver, é opcional. | Rankings ansiogênicos | Zagal et al. (2013) |
| D5 | Temas sensíveis têm tela de aviso de conteúdo antes da cena e link para recursos de apoio. | Conteúdo não sinalizado | Safe Messaging Guidelines (AFSP) |
| D6 | Representatividade desde o conceito: ao menos opções de pronome e diversidade visual de personagens. | Exclusão de identidades | Ryan e Deci (2000) |

### 3.3 Checklist de encerramento

- [ ] Todos os NPCs principais têm vulnerabilidade e arco emocional definidos.
- [ ] Ao menos uma escolha narrativa tem impacto real e perceptível.
- [ ] Todas as interações sociais são opcionais para a progressão principal.
- [ ] Não há rankings públicos ou comparação negativa entre jogadores.
- [ ] Temas sensíveis têm aviso de conteúdo antes da cena.
- [ ] Há representatividade de identidades (pronome, diversidade visual).
- [ ] Ao menos um momento narrativo estimula a empatia genuína.

---

## FASE 4 — INTERFACE E UX

**Objetivo:** a interface é a camada de confiança entre o jogo e o jogador. Um bom UX garante comportamento previsível e honesto, sem manipulações estéticas. Esta fase aplica os princípios de Nielsen (1994) filtrados pelo critério da segurança psicológica.

### 4.1 Perguntas reflexivas

| # | Pergunta | Necessidade TAD |
|---|----------|-----------------|
| P1 | A interface deixa claro o que cada botão faz antes do clique? Há feedback imediato? | Flow — clareza |
| P2 | Há confirmação de dois passos antes de ações irreversíveis (apagar save, gastar moeda)? | Autonomia — compra acidental |
| P3 | O feedback visual/sonoro representa fielmente o resultado real da ação? | Competência — manipulação estética |
| P4 | Quantos elementos de HUD ficam visíveis ao mesmo tempo? Cada um é imprescindível? | Flow — sobrecarga cognitiva |
| P5 | O menu de pausa é acessível em qualquer estado do jogo, sem exceção? | Autonomia Temporal |
| P6 | As notificações push (se houver) são úteis ou só servem para trazer o jogador de volta? | Autonomia — agendamento |
| P7 | Há configurações de acessibilidade (fonte, contraste, subtítulos, modo daltônico)? | Autonomia — inclusão |
| P8 | O preço em moeda real está sempre visível antes da compra? Sem moeda fictícia que obscureça o valor? | Autonomia — Moeda Premium |

### 4.2 Diretrizes (Padrões Radiantes)

| # | Diretriz | Dark Pattern substituído | Referência |
|---|----------|--------------------------|------------|
| D1 | HUD minimalista: apenas o imprescindível para a ação atual; o resto acessível por demanda. | Sobrecarga de HUD | Nielsen (1994); Csikszentmihalyi (1990) |
| D2 | Ações irreversíveis exigem confirmação de dois passos. Botões de compra nunca próximos a botões de gameplay. | Compras acidentais | Zagal et al. (2013) |
| D3 | Eliminar sons de urgência (alarmes, contagens, jingles de evento expirando). | Urgência artificial | darkpattern.games |
| D4 | Implementar volume separado, modo daltônico, subtítulos e tamanho de fonte ajustável. | Exclusão por acessibilidade | Nielsen (1994) |
| D5 | Notificações push proibidas como mecanismo de retorno. Se existirem, são opt-in, úteis e fáceis de desativar. | Push coercitiva | darkpattern.games |

### 4.3 Checklist de UX consciente (objetivo: zero "Revisar")

- [ ] Toda ação irreversível tem confirmação de dois passos.
- [ ] Feedback visual/sonoro honesto com o resultado real.
- [ ] Botão de pausa acessível em qualquer estado do jogo.
- [ ] Texto/ícones com tamanho mínimo de 14pt; área de toque 44×44px.
- [ ] Contraste de texto ≥ 4,5:1 (WCAG AA).
- [ ] Modo para daltônicos disponível.
- [ ] Notificações push opcionais e desativáveis dentro do jogo.
- [ ] Nenhum botão de compra próximo a botões de gameplay.
- [ ] Preço em moeda real sempre visível antes da compra.
- [ ] Salvamento automático ao fechar (sem perda de progresso).
- [ ] Menu de configurações acessível de qualquer tela.
- [ ] Subtítulos para todos os diálogos com áudio.
- [ ] HUD com no máximo 3 métricas simultâneas durante o gameplay.
- [ ] Nenhum elemento pisca ou anima de forma intrusiva.
- [ ] Sons de urgência ausentes do jogo.

### 4.4 Checklist de encerramento

- [ ] O Checklist de UX consciente foi aplicado a todas as telas principais.
- [ ] HUD com no máximo 3 métricas simultâneas.
- [ ] Nenhum som de urgência ou elemento piscante.
- [ ] Ações irreversíveis com confirmação de dois passos.
- [ ] Acessibilidade básica implementada.
- [ ] Notificações push opt-in e úteis.
- [ ] Preço em moeda real visível antes de qualquer compra.

---

Para os 8 critérios de validação heurística aplicados ao final do roteiro, veja [`checklist-heuristico.md`](checklist-heuristico.md).
