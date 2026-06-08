# Como configurar o SAD no Google Gemini

O Roteiro de Design Consciente funciona como um **Gem** — um assistente personalizado do Gemini com instruções permanentes. A configuração leva poucos minutos e não exige conhecimento de programação.

## Passo a passo

1. **Acesse o Gemini.** Abra [gemini.google.com](https://gemini.google.com) e faça login com sua conta Google.

2. **Abra a seção de Gems.** No menu lateral esquerdo, procure por *Gerenciar Gems* (ou *Meus Gems*). Se não aparecer diretamente, clique em *Explorar Gems*. Em seguida, clique em **Novo Gem**.

3. **Dê nome e descrição.**
   - **Nome:** `Roteiro de Design Consciente — SAD`
   - **Descrição:** `Sistema de apoio à decisão para o design ético de jogos digitais.`

4. **Cole o prompt — passo mais importante.** Abra o arquivo [`prompt-sistema.md`](prompt-sistema.md), selecione todo o conteúdo (Ctrl+A) e copie (Ctrl+C). No Gem, localize o campo **Instruções** (o campo grande de texto) e cole (Ctrl+V). O texto deve preencher o campo por completo.

5. **Salve o Gem.** Clique em **Salvar**. Ele aparecerá na sua lista de Gems.

6. **Teste.** Abra o Gem e escreva, por exemplo:
   > "Olá, quero usar o Roteiro de Design Consciente para analisar meu jogo."

   O SAD deve responder com a mensagem de boas-vindas e as cinco perguntas de briefing do projeto. Se isso acontecer, está configurado corretamente.

## Dica

Quanto mais detalhes você fornecer no briefing (gênero, plataforma, público, mecânicas), mais personalizadas serão as análises. Ao final de cada fase, o sistema gera um relatório que você pode salvar e incluir no Game Design Document (GDD) do seu projeto.
