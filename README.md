# Roteiro de Design Consciente — SAD

**Sistema de Apoio à Decisão (SAD) para o desenvolvimento ético de jogos digitais.**

O Roteiro de Design Consciente é uma metodologia, operacionalizada como assistente de IA, que guia desenvolvedores de jogos por um processo reflexivo estruturado, ajudando-os a tomar decisões de design que priorizem o **bem-estar** e a **segurança psicológica** dos jogadores. Ele não substitui a criatividade do desenvolvedor — instrumentaliza essa criatividade com consciência ética fundamentada em psicologia científica.

> Produto técnico do Trabalho de Conclusão de Curso (TCC II) — Sistemas de Informação
> Centro Universitário Paraíso (UniFAP) — Juazeiro do Norte, CE, 2026
> **Autor:** Isaac Wanderson de Pontes Xavier
> **Orientador:** Prof. Fabricio Carneiro Costa

---

## Sobre o projeto

A ferramenta traduz teorias da psicologia do bem-estar em um processo prático de quatro fases. Em cada fase, o desenvolvedor encontra perguntas reflexivas, diretrizes baseadas nos Padrões Radiantes e alertas sobre Dark Patterns a evitar. Ao final, o sistema gera um relatório de síntese e um checklist heurístico que indica o grau de conformidade do projeto com os princípios do bem-estar psicológico.

O SAD é operacionalizado gratuitamente como um **Gem** (assistente personalizado) na plataforma **Google Gemini**, acessível pelo navegador, sem instalação nem necessidade de programação.

## Fundamentação teórica

- **Teoria da Autodeterminação (TAD/SDT)** — Ryan e Deci (2000): autonomia, competência e relacionamento
- **Teoria do Fluxo (Flow)** — Csikszentmihalyi (1990): equilíbrio entre desafio e habilidade
- **Padrões Radiantes** — Miranda e Darin (2022): antídotos éticos aos Dark Patterns
- **Dark Patterns** — Zagal, Björk e Lewis (2013): padrões manipulativos a detectar
- **Usabilidade** — Nielsen (1994): clareza, feedback e prevenção de erros
- **Segurança Psicológica** — Edmondson (1999): ambiente seguro para errar e aprender

## Estrutura do repositório

```
roteiro-design-consciente/
├── README.md                          Este arquivo
├── LICENSE                            Licença de uso (CC BY 4.0)
├── prompt-sistema.md                  Prompt de sistema para configurar o Gem no Gemini
├── roteiro-de-design-consciente.md    O roteiro completo (4 fases + diretrizes + checklists)
├── checklist-heuristico.md            Os 8 critérios de validação heurística
└── COMO-CONFIGURAR.md                 Passo a passo para criar o Gem no Gemini
```

## Como usar

A configuração leva poucos minutos e está detalhada em [`COMO-CONFIGURAR.md`](COMO-CONFIGURAR.md). Em resumo:

1. Acesse [gemini.google.com](https://gemini.google.com) e faça login com uma conta Google.
2. Crie um novo Gem (em *Gerenciar Gems* → *Novo Gem*).
3. Dê o nome **Roteiro de Design Consciente — SAD**.
4. Copie todo o conteúdo de [`prompt-sistema.md`](prompt-sistema.md) e cole no campo de **Instruções**.
5. Salve e inicie a conversa. O assistente responderá com o briefing do projeto.

## Como citar

> XAVIER, Isaac Wanderson de Pontes. *Sistema de Apoio à Decisão para a criação de jogos psicologicamente seguros.* Trabalho de Conclusão de Curso (Sistemas de Informação) — Centro Universitário Paraíso (UniFAP), Juazeiro do Norte, 2026.

## Licença

Distribuído sob a licença **Creative Commons Atribuição 4.0 Internacional (CC BY 4.0)**. Você pode usar, adaptar e redistribuir, inclusive para fins comerciais, desde que dê o crédito apropriado. Veja [`LICENSE`](LICENSE).
