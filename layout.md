# Especificação de Layout - MV Gestão Web

**Diretriz Visual:** Premium Swiss-Tech
**Font Play:** Space Grotesk (Display) + Inter (Body)
**Cores Primárias:** Navy (#0F172A), Royal Blue (#2563EB), White (#FFFFFF), Slate Light (#F8FAFC)
**Cores Secundárias:** Text Muted (#64748B), Border (#E2E8F0)

---

## Seção 1: Hero - "O Painel de Controle"

### Arquetipo e Constraints
- **Arquetipo:** Hero Dominante com Camadas (Layered)
- **Constraints:** Glassmorphism + Scroll Parallax + Data Visualization
- **Justificativa:** Atende ao pedido de "Dashboard minimalista" e "Métricas animadas". O vidro (glass) confere modernidade, e os dados flutuantes passam a sensação de controle estratégico.

### Conteúdo
- **Tag:** Consultoria Estratégica v4.0
- **Headline:** Domine o Mercado de Maringá com uma Estrutura Digital de Verdade
- **Subheadline:** Pare de depender da sorte. Implemente o método de crescimento previsível que coloca sua empresa na frente dos clientes que já estão procurando por você.
- **CTA Principal:** Quero Agendar meu Diagnóstico Estratégico
- **CTA Secundário:** Conhecer o Método

### Layout
- **Estrutura:** Grid de 2 colunas (45% Texto / 55% Visual).
- **Alinhamento:** Verticalmente centralizado.
- **Altura Mínima:** 90vh (Full Height visual, mas com conteúdo seguro).
- **Conteúdo (Esquerda):** Alinhado à esquerda. Margem direita de 4rem.
- **Visual (Direita):**
    - Um "Main Card" (Dashboard) centralizado no container da direita.
    - 2 "Floating Cards" menores orbitando o principal (um atrás com blur, um na frente com shadow).
    - Elementos conectados por linhas finas (1px) com opacidade reduzida.

### Tipografia
- **Headline:** Space Grotesk, Weight 700, Tamanho clamp(3.5rem, 5vw, 5rem), Line-height 1.1, Letter-spacing -0.03em.
- **Subheadline:** Inter, Weight 400, Tamanho 1.125rem, Line-height 1.6, Cor #64748B.
- **Tag:** Inter, Weight 600, Tamanho 0.875rem, Uppercase, Tracking 0.1em, Cor #2563EB.

### Cores
- **Background:** Radial Gradient (#F1F5F9 0%, #FFFFFF 60%) centered on the visual side.
- **Cards do Dashboard:** White (#FFFFFF) com 90% opacity (Glass). Border: 1px solid rgba(255,255,255, 0.5).
- **Gráficos/Linhas:** Royal Blue (#2563EB) para dados positivos, Slate 300 (#CBD5E1) para grid lines.

### Elementos Visuais (Data Viz)
- **Main Card:** Gráfico de linha (SVG) mostrando curva de crescimento suave. Área abaixo da linha com preenchimento gradiente (Blue to Transparent).
- **Floating Card 1 (Top Right):** Indicador de "ROAS" com círculo de progresso 75% preenchido. Texto: "+124%".
- **Floating Card 2 (Bottom Left):** Lista compacta de "Leads Recentes" (3 linhas abstratas com avatares minimalistas).

### Animações
- **Entrada (Load):**
    - Texto: Stagger Fade Up (50px -> 0px) em 800ms, delay 200ms.
    - Dashboard Main Card: Fade In + Scale (0.95 -> 1.0) em 1000ms, ease-out-quart.
    - Floating Cards: Fade In + TranslateY (20px -> 0) em 1200ms, delay 400ms.
    - Linhas do Gráfico: "Draw SVG" animation (path drawing) em 1.5s ease-in-out.
- **Scroll:** Parallax suave (speed 0.05) nos Floating Cards (eles sobem um pouco mais rápido que o fundo).

### Interatividade
- **Hover no Dashboard:** Leve tilt 3D (perspective 1000px, rotateX/Y ~2deg). Sombra aumenta (box-shadow: 0 30px 60px rgba(0,0,0,0.1)).

### Responsividade
- **Mobile (<768px):** Stack vertical. Visual vai para baixo do texto. Floating Cards reposicionados para não vazar a tela. Tamanho da Headline reduz para 2.5rem.

---

## Seção 2: A Realidade (Scrollytelling Leve)

### Arquetipo e Constraints
- **Arquetipo:** Split Assimetrico (Texto Fixo + Visual Scrollavel/Interativo)
- **Constraints:** Scroll Triggered + Minimal + High Contrast (Light)
- **Justificativa:** Para contar a história da "demanda invisível", usamos um layout onde o texto provoca e o visual demonstra os números subindo conforme o usuário desce.

### Conteúdo
- **Título:** Seu Cliente Está Procurando Por Você Agora. A Pergunta É: Ele Te Encontra?
- **Texto:** Maringá vive um momento de alta demanda digital. Todos os dias, milhares de pessoas buscam pelos seus serviços no Google e nas redes sociais. Mas atenção: estar na internet não é o suficiente. Se sua empresa não transmite autoridade imediata e não possui um sistema de captação ativo, você está deixando dinheiro na mesa e entregando clientes de bandeja para a concorrência. Não é sobre "postar todo dia". É sobre ser a escolha óbvia.

### Layout
- **Estrutura:** Container largo. Esquerda (40%) para o título impactante. Direita (60%) para o texto e uma representação visual de "Buscas em Tempo Real".
- **Padding:** 8rem 0 (Espaço generoso).

### Tipografia
- **Título:** Space Grotesk, Weight 600, 2.5rem.
- **Texto Destaque:** "Não é sobre postar todo dia" em Negrito (#0F172A).

### Cores
- **Fundo:** #FFFFFF (White).
- **Barra de Progresso (Visual):** #2563EB.

### Elementos Visuais
- **Visual:** Uma barra de busca estilizada do Google (minimalista) flutuando. Abaixo dela, contadores numéricos que incrementam rapidinho quando a seção entra na tela (ex: "Buscas Hoje: 0" -> "4.532").

### Animações
- **Ao Entrar (Scroll Trigger):**
    - Contador numérico roda de 0 até o valor final em 2s.
    - Barra de busca faz uma animação de "digitando..." (simulado com CSS steps).
    - Título: Fade Up.

---

## Seção 3: O Erro (Diagnóstico)

### Arquetipo e Constraints
- **Arquetipo:** Broken Grid / Isolated Elements
- **Constraints:** Dark Mode parcial (Card Destacado) + Red/Warning Accents (Sutil)
- **Justificativa:** Diferenciar o "erro" da "solução". O Grid quebrado representa a fragmentação do marketing atual.

### Conteúdo
- **Título:** Por Que A Maioria Dos Negócios Locais Estagna?
- **Subtítulo:** O erro mais comum é tratar o digital como um jogo de sorte.
- **Lista de Erros:**
    1. Site lento e amador que afasta clientes.
    2. Perfil no Google (GBP) desatualizado e sem avaliações respondidas.
    3. Tráfego pago feito sem estratégia, queimando verba com cliques curiosos.
    4. Falta de um funil de vendas claro.
- **Conclusão:** Resultado: muito esforço, pouco retorno e uma operação que não escala.

### Layout
- **Grid:** 2x2 irregular.
- **Card do Erro:** Cada erro é um card com ícone minimalista (ex: um raio quebrado, uma moeda caindo).
- **Disposição:** Os cards não estão perfeitamente alinhados, têm margens topo diferentes para criar ritmo visual ("quebrado").

### Tipografia
- **Lista:** Inter, 1rem, com ícone de "X" ou "Alert" sutil antes.

### Cores
- **Fundo Seção:** #F8FAFC (Slate muito claro).
- **Cards:** Branco com borda sutil (#E2E8F0).
- **Ícones de Erro:** Tom de alerta suave (ex: #EF4444) mas desaturado para não ficar agressivo demais, ou manter monocromático (#64748B) para elegância. Vamos usar #64748B para manter o "Premium".

### Animações
- **Cards:** Fade In individualmente com delay (100ms, 200ms, 300ms, 400ms).
- **Hover:** Ao passar o mouse, o card fica levemente opaco (0.8) como se estivesse "desligando" ou falhando, reforçando a ideia de erro.

---

## Seção 4: Os 4 Pilares (A Solução - Bento Grid)

### Arquetipo e Constraints
- **Arquetipo:** Bento Grid (Box Layout)
- **Constraints:** Hover Reveal + Glassmorphism Details + Linear Icons
- **Justificativa:** Pedido explícito. Organiza a solução complexa em blocos digeríveis e modernos.

### Conteúdo
- **Título:** O Método MV de Dominação Local
- **Intro:** Nossa consultoria implementa uma estrutura completa...
- **Card 1 (Grande - 2 colunas):** Pilar 1: Posicionamento Local. (Texto...)
- **Card 2 (Quadrado):** Pilar 2: Site Estratégico. (Texto...)
- **Card 3 (Quadrado):** Pilar 3: Google Perfil. (Texto...)
- **Card 4 (Retangular Vertical ou Horizontal):** Pilar 4: Tráfego Pago. (Texto...)

### Layout
- **Grid:** CSS Grid.
    - Desktop: 3 colunas.
    - Row 1: Card 1 (span 2), Card 2 (span 1).
    - Row 2: Card 3 (span 1), Card 4 (span 2).
- **Gap:** 1.5rem (24px).
- **Cards:** Padding 2.5rem. Altura mínima 300px.

### Elementos Visuais
- **Ícones:** Ícones lineares ultrafinos (Stroke 1px) em tamanho grande (48px) no canto superior esquerdo de cada card.
- **Números:** "01", "02", "03", "04" em fonte Display enorme (Space Grotesk), opacidade 0.05, no fundo do card.

### Cores
- **Cards Fundo:** #FFFFFF.
- **Card Destaque (Pilar 1 ou Tráfego):** Pode ter um fundo sutilmente diferente (#F1F5F9) ou uma borda ativa (#2563EB).
- **Shadow:** Sombra difusa e suave (box-shadow: 0 10px 40px -10px rgba(0,0,0,0.05)).

### Interatividade
- **Hover:**
    - O Card "acende" (borda fica #2563EB).
    - Ícone muda de cor (Slate -> Blue).
    - Leve Scale (1.01).

---

## Seção 5: Cases de Sucesso (Relatório Executivo)

### Arquetipo e Constraints
- **Arquetipo:** Data Table / Dashboard Panels
- **Constraints:** Monochromatic + Data Dense (Visualmente)
- **Justificativa:** Pedido explícito: "Layout tipo Relatório Executivo", "Nada de carrossel".

### Conteúdo
- **Parceiros:** Dr. Ricardo S., Ana Paula M., etc.
- **Dados:** Números grandes (+42% Crescimento, -18% CAC).
- **Texto:** Depoimento curto.

### Layout
- **Estrutura:** Lista vertical de "Paineis". Cada case é uma linha horizontal (Row) detalhada.
- **Row Layout:**
    - Coluna 1: Nome/Cargo (Avatar minimalista se houver, ou apenas iniciais).
    - Coluna 2: Big Number (O dado principal do case).
    - Coluna 3: O "Contexto" (Trecho do depoimento).
    - Coluna 4: Link/Seta discreta "Ver Detalhes" (fictício, apenas visual).

### Elementos Visuais
- **Divisores:** Linhas horizontais finas (#E2E8F0) separando cada case.
- **Tipografia de Dados:** Space Grotesk, Bold, cores variadas (Verde para crescimento, Azul para otimização).

### Animações
- **Entrada:** As linhas desenham da esquerda para direita (width 0 -> 100%). O conteúdo aparece depois (Fade In).

---

## Seção 6: Quem é a MV (Manifesto)

### Arquetipo e Constraints
- **Arquetipo:** Editorial / Split Minimal
- **Constraints:** Justified Typography + Signature
- **Justificativa:** Passar autoridade e seriedade.

### Conteúdo
- **Título:** Estrategistas, Não Apenas Executores.
- **Texto:** Manifesto sobre não ser agência de post.

### Layout
- **Fundo:** #0F172A (Navy Dark - Inversão total para dar peso).
- **Texto:** Branco (#FFFFFF) e Cinza Claro (#94A3B8).
- **Coluna Única (Narrow):** Texto centralizado ou alinhado à esquerda com margem generosa, focado na leitura.

### Tipografia
- **Highlight:** Frase "Design sem venda é arte" em destaque (Tamanho maior, itálico).

---

## Seção 7: Para Quem É (Filtro)

### Arquetipo e Constraints
- **Arquetipo:** Comparison / Split Vertical
- **Constraints:** Positive/Negative Reinforcement (Green/Red accents - sutis)

### Conteúdo
- **Título:** Este Diagnóstico É Para Você?
- **Colunas:** "É para você" vs "NÃO é para você".

### Layout
- **Grid:** 2 Colunas.
- **Coluna Sim (Esquerda):** Fundo Branco, Checkmarks Azuis/Verdes.
- **Coluna Não (Direita):** Fundo #F8FAFC (leveeemente cinza), ícones de "X" ou "Alert".

### Visual
- **Lista:** Itens com bom espaçamento (1.5rem entre itens).
- **Checks:** Ícones customizados, não padrão do browser.

---

## Seção 8: FAQ & CTA Final

### Arquetipo e Constraints
- **Arquetipo:** Accordion (FAQ) + Contained Center (CTA)
- **Constraints:** Clean Lines

### Layout
- **FAQ:** Centralizado, largura max 800px. Itens com borda apenas embaixo. Ao abrir, o ícone (+) vira (-).
- **CTA Final:**
    - Bloco destacado ao final.
    - Fundo Royal Blue (#2563EB).
    - Texto Branco.
    - Botão Branco (Invertido).
    - Título: "Pronto para escalar?"
    - Botão: "Solicitar Diagnóstico Estratégico".

---

## Seção 9: Rodapé

### Arquetipo
- **Arquetipo:** Grid Modular (4 colunas: Logo/Intro, Serviços, Contato, Copyright).
- **Estilo:** Minimalista, fundo branco ou slate muito claro. Texto pequeno e discreto.

---

## Resumo dos Assets Necessários (Gerar via CSS/SVG)
- Ícones Lineares (4 Pilares, Erros, Checks).
- Gráficos SVG para o Hero (Linha de crescimento, Círculo de ROAS).
- Blobs/Gradientes de fundo (CSS puro).

---

**Observação Final:** Todo o layout deve priorizar o "WhiteSpace" (Respiro). As margens verticais entre seções devem ser de no mínimo 8rem (128px) em desktop para garantir a sensação premium.
