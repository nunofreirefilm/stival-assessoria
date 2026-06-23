# Layout e Especificação Visual: STIVAL Assessoria e Consultoria Empresarial

Este documento contém a especificação exaustiva de cada seção da landing page da STIVAL Assessoria, traduzindo o design aprovado e a copy em instruções precisas de layout, animação e interatividade. 

**Identidade Visual Fixa:**
- **Fontes:** Plus Jakarta Sans (Headings) + Inter (Body) - *Vibe: Premium geometric*
- **Cores Oficiais:**
  - Blue: `#0A192F`
  - Blue Light: `#112B52`
  - Blue Text: `#1C3661`
  - Yellow: `#FFC700`
  - Yellow Hover: `#E5B300`
  - White: `#FFFFFF`
  - Off-White (BG): `#FAFAFA`
  - Gray Text: `#4A5568`

---

## Seção 1: Hero

### Arquétipo e Constraints
- **Arquétipo:** Single Focus
- **Constraints:** Imagem Blur Background, Dark Mode, Mixed Weights (200 + 700)
- **Justificativa:** Cria uma introdução imersiva, limpa e com autoridade imediata sem distrações. A imagem borrada ao fundo sugere contexto sem roubar atenção da tipografia.

### Conteúdo
- **Headline:** Transformamos oportunidades tributárias em economia e segurança.
- **Subheadline:** Reduza custos, recupere créditos e organize sua gestão tributária com inteligência, transparência e embasamento técnico.
- **CTA:** Quero solicitar uma análise

### Layout
- **Estrutura:** `min-height: 100vh`, `display: flex`, `align-items: center`.
- **Espaçamento:** Padding `4rem 10%` em desktop. 
- **Z-Index:** Background `z-index: 1`, Overlay `z-index: 2`, Content `z-index: 3`. Max-width do conteúdo: `900px`.

### Tipografia
- **Headline:** Plus Jakarta Sans, `clamp(2.5rem, 5vw, 4.5rem)`, linha `1.1`, tracking `-0.02em`. Mix de pesos: "Transformamos" (200), "oportunidades tributárias" (700), "em economia e segurança." (200).
- **Subheadline:** Inter, `clamp(1.1rem, 2vw, 1.3rem)`, weight `300`, max-width `600px`, margin-bottom `3.5rem`.

### Cores
- **Fundo:** `#0A192F` com Overlay em Linear Gradient 135deg de `rgba(10, 25, 47, 0.95)` para `rgba(10, 25, 47, 0.8)`.
- **Textos:** Brancos `#FFFFFF`, destaque em Amarelo `#FFC700`.

### Elementos Visuais
- Logo da marca (`width: 180px`) no topo do container.
- Imagem de fundo tratada com `filter: blur(8px) grayscale(50%)` e `opacity: 0.3`. Carregamento `eager`.

### Animações
- **NENHUMA ANIMAÇÃO DE ENTRADA.** O Hero deve carregar e estar imediatamente visível para não prejudicar o LCP e evitar CLS.

### Interatividade
- **CTA Hover:** Fundo muda para `#E5B300`, `transform: translateY(-4px)`, `box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2)`, transition de `0.3s ease`.

### Responsividade
- **Mobile (<900px):** Padding reduzido para `4rem 5%`. Títulos escalam automaticamente com `clamp()`.

---

## Seção 2: O Problema

### Arquétipo e Constraints
- **Arquétipo:** Split Assimétrico (1.2fr / 0.8fr)
- **Constraints:** Fade Up, High Contrast Highlight, Absolute Positioning (decoração).
- **Justificativa:** O formato split concentra a mensagem pesada à esquerda enquanto ilustra simbolicamente à direita, mantendo o dinamismo na transição de conteúdos.

### Conteúdo
- **Título:** Sua empresa pode estar perdendo dinheiro agora
- **Conteúdo:** Toda empresa possui desafios fiscais e operacionais. Muitas vezes, esses desafios geram custos desnecessários, riscos tributários e perda de oportunidades de recuperação de valores cruciais para o seu fluxo de caixa.

### Layout
- **Estrutura:** CSS Grid com `grid-template-columns: 1.2fr 0.8fr` e `gap: 6rem`.
- **Espaçamento:** Padding de `8rem 10%`. Fundo com a cor secundária clara `#FAFAFA`.

### Tipografia
- **Título:** Plus Jakarta Sans, `clamp(2rem, 4vw, 3.5rem)`, weight `700`, line-height `1.2`.
- **Corpo:** Inter, `1.2rem`, weight `300`, cor `#4A5568`.

### Cores
- Fundo principal: `#FAFAFA`
- Título principal: `#1C3661` (Blue Text) com destaque "perdendo dinheiro" em `#0A192F` (Blue).
- Card visual: `#FFFFFF` com borda esquerda `#FFC700`.

### Elementos Visuais
- Um "Visual Card" à direita com o símbolo `R$` gigante (`5rem`, fontWeight 700, `#0A192F`).
- Pseudo-elemento `::before` quadrado decorativo (100x100px) em Absolute Positioning fora do card superior direito com `opacity: 0.05` na cor `#0A192F`.

### Animações
- Trigger `IntersectionObserver` disparado a 10% de viewport.
- Fade-up clássico: `opacity: 0` a `1`, `transform: translateY(30px)` a `0` em `0.8s ease`. Delay de `0.2s` para o bloco da direita. (Usar `disableMutationObserver: true` na inicialização do AOS, se aplicado).

### Responsividade
- **Mobile (<900px):** O Grid se torna `1fr`, empilhando com o texto acima do card. Gap reduz para `3rem`, padding para `5rem 5%`.

---

## Seção 3: A Solução

### Arquétipo e Constraints
- **Arquétipo:** Contained Center
- **Constraints:** Texto com Sombra Colorida, Floating Elements, Dark Mode.
- **Justificativa:** Uma pausa visual centralizada, servindo como respiro depois da carga informacional assimétrica. O Dark Mode retoma a autoridade institucional.

### Conteúdo
- **Título:** Crescimento com controle e segurança
- **Conteúdo:** Auxiliamos empresas a melhorarem suas gestões e minimizarem desperdícios. Nossa atuação combina análise técnica rigorosa com visão estratégica para criar caminhos seguros na sua tomada de decisão.

### Layout
- **Estrutura:** Flexbox Column, centralizado (`align-items: center`, `text-align: center`).
- **Dimensões:** `max-width: 800px` internamente, section com padding `10rem 10%`.

### Tipografia
- **Título:** Plus Jakarta Sans, `3rem`, weight `700`. Text Shadow sutil amarela `0 4px 20px rgba(255, 199, 0, 0.15)`.
- **Corpo:** Inter, `1.25rem`, weight `400`, line-height `1.8`.

### Cores
- **Fundo:** `#0A192F`.
- **Textos:** Título `#FFFFFF`, Corpo rgba branco (0.8).

### Elementos Visuais
- **Decoração:** Duas esferas com gradientes esvanecidos em `absolute positioning` flutuando nas extremidades como "lens flares" muito sutis, na cor `#112B52`.

### Animações
- **Reveal:** Textos surgem com um `fade-up` macio (duração 1000ms).
- **Ambient Motion:** As esferas de fundo possuem `Float Loop` (subindo e descendo `20px` ao longo de 6 segundos de forma orgânica).

### Interatividade
- Nenhuma específica. Leitura limpa.

### Responsividade
- Textos ajustam por `clamp()`. As esferas somem em mobile para não poluir o fundo.

---

## Seção 4: Nossos Serviços

### Arquétipo e Constraints
- **Arquétipo:** Bento Box (Grid Complexo)
- **Constraints:** Glassmorphism, Hover Lift, Hover Glow, Mixed Card Sizes.
- **Justificativa:** 7 serviços listados no modo tradicional (3 colunas iguais) geram cansaço. Um bento box com cartas de pesos e tamanhos diferentes hierarquiza a importância e engaja o clique.

### Conteúdo
- **Título:** O que fazemos pela sua empresa
- **Card 1 (Grande):** Planejamento Tributário / Pague apenas o que é devido, evite riscos e torne sua operação mais eficiente.
- **Card 2 (Grande):** Recuperação de Tributos / Resgate seguro de créditos pagos indevidamente, gerando recursos para o caixa.
- **Card 3 (Médio):** Consultoria Tributária / Revisão detalhada de processos e correção de inconsistências fiscais.
- **Card 4 (Médio):** Assessoria Empresarial / Apoio na organização financeira, fluxo de caixa e aumento de produtividade.
- **Card 5 (Pequeno):** Assessoria no Agronegócio / Otimização tributária e recuperação de créditos focada no produtor rural.
- **Card 6 (Pequeno):** Compra e Venda de Créditos / Viabilidade e segurança jurídica na negociação de créditos tributários.
- **Card 7 (Longo):** Registro de Marcas e Patentes / Proteção do seu patrimônio intelectual, marcas e softwares junto ao INPI.

### Layout
- **Estrutura:** CSS Grid. Desktop: 4 colunas (`1fr` cada) x 3 linhas.
  - Card 1: `grid-column: span 2` / `grid-row: span 2`
  - Card 2: `grid-column: span 2` / `grid-row: span 1`
  - Card 3: `grid-column: span 1` / `grid-row: span 1`
  - Card 4: `grid-column: span 1` / `grid-row: span 1`
  - Card 5: `grid-column: span 1` / `grid-row: span 1`
  - Card 6: `grid-column: span 1` / `grid-row: span 1`
  - Card 7: `grid-column: span 2` / `grid-row: span 1`
- **Gap:** `1.5rem`.
- **Padding da Seção:** `8rem 5%`.

### Tipografia
- **Título da Seção:** Plus Jakarta Sans, `3rem`, color `#1C3661`.
- **Títulos dos Cards:** Plus Jakarta Sans, `1.5rem` (Grandes) e `1.2rem` (Médios/Pequenos), weight `700`.
- **Textos dos Cards:** Inter, `1rem`, color `#4A5568`.

### Cores
- Fundo da seção: `#FAFAFA`.
- Cards: Background `#FFFFFF`, bordas sutis `1px solid rgba(0,0,0,0.05)`.
- Cards com destaque (1 e 2): Fundo leve `#F5F7FA` e borda bottom amarela `3px solid #FFC700`.

### Elementos Visuais
- Ícones vetoriais sutis, no topo superior direito de cada card (com opacidade 0.2 e tamanho `32px`).

### Animações
- **Stagger:** Cada card entra no grid com `Fade Up` e delay progressivo (`+100ms` por card) ao scroll chegar na área.

### Interatividade
- **Hover:** Nos cards: `transform: translateY(-8px) scale(1.01)`, com `box-shadow: 0 20px 40px rgba(10,25,47,0.08)`. Transição longa de `400ms cubic-bezier(0.16, 1, 0.3, 1)`.

### Responsividade
- **Tablet (<1024px):** Grid ajustado para 2 colunas uniformes.
- **Mobile (<768px):** Grid em 1 coluna. Todos os elementos ganham alturas flexíveis sem spans.

---

## Seção 5: Frentes de Atuação

### Arquétipo e Constraints
- **Arquétipo:** Sticky Element + Scroll Horizontal Simulado
- **Constraints:** Typography Hero (Texto com Stroke), Wave Stagger, Sticky Header.
- **Justificativa:** O termo "Soluções" fica travado (sticky) na lateral enquanto a lista escrola independentemente. Usa muito espaço negativo e sofistica o visual de lista de bullets.

### Conteúdo
- **Título:** Soluções completas e especializadas
- **Bullets:** Revisão fiscal e reforma tributária / Auditoria de folha focada no eSocial / Planejamento e proteção patrimonial / Recuperação de INSS, PIS, COFINS e ICMS / Subvenção de investimentos e Lei do Bem / BPO financeiro e revisão de processos / Soluções exclusivas para construção civil e agronegócio

### Layout
- **Estrutura:** Flexbox Row. Esquerda (40% largura): Titulo `position: sticky; top: 20vh`. Direita (60% largura): Lista com grande margin-bottom entre itens.
- **Espaçamento:** Padding `10rem 10%`. Min-height alto para forçar o scroll da coluna da direita.

### Tipografia
- **Título:** Plus Jakarta Sans, Texto muito grande: `clamp(3rem, 6vw, 5rem)`, text-transform `uppercase`, line-height `1`. A palavra "Especializadas" vazada (Apenas Stroke).
- **Lista:** Inter, `1.8rem`, weight `400`. Letras amplas e arejadas.

### Cores
- **Fundo:** `#FFFFFF`.
- **Textos:** Título sólido `#0A192F`. Título Stroke: `-webkit-text-stroke: 2px #0A192F`, `color: transparent`. Letras da lista: `#1C3661`.

### Elementos Visuais
- Custom checkmark (SVG em `#FFC700`) alinhado à esquerda de cada item.

### Animações
- **Scroll Speed:** O título se move mais devagar, a lista mais rápido.
- **Wave Stagger:** Os bullets surgem de lado (`TranslateX(30px)`) com fade conforme entram no viewport.

### Interatividade
- Hover no bullet list: Cor do texto muda de `#1C3661` para `#FFC700`, adicionando um recuo de `10px` para a direita com `transition: 0.3s`.

### Responsividade
- **Mobile (<900px):** Desliga o Sticky. A seção vira uma coluna única padrão. Títulos reduzem e a lista desce para o tamanho padrão de `1.2rem`.

---

## Seção 6: Prova Social (Números)

### Arquétipo e Constraints
- **Arquétipo:** Rule of Thirds Assymmetric
- **Constraints:** Counter Animation, Monocromático com Yellow Accents, Overlap Elements.
- **Justificativa:** Números transmitem credibilidade instantânea. Fundo escuro dá um peso institucional fortíssimo.

### Conteúdo
- **Título:** Por que confiar na STIVAL?
- **N1:** +5 anos (atuação prática)
- **N2:** +1.000 projetos (entregues com sucesso)
- **N3:** Centenas (clientes atendidos)
- **N4:** Milhões (recuperados)
- **Diferenciais:** Equipe técnica especializada e transparência absoluta.

### Layout
- **Estrutura:** Grid `30% 70%`. Esquerda: Título principal. Direita: Grid de 2x2 para os números.
- **Espaçamento:** `Padding: 8rem 10%`.

### Tipografia
- **Números Grandes:** Plus Jakarta Sans, `4.5rem`, weight `700`, `letter-spacing: -2px`.
- **Legendas:** Inter, `1.1rem`, color `rgba(255,255,255,0.7)`.

### Cores
- **Fundo:** `#0A192F`.
- **Números:** `#FFC700` vibrante.
- **Textos:** `#FFFFFF`.

### Animações
- **Counter Animation:** Os números devem rolar de 0 até o seu alvo final (0 a 5, 0 a 1000) usando um script que é ativado quando o bloco entra no viewport.
- Duração da contagem: `2.5s cubic-bezier`.

### Interatividade
- Linhas sutis divisórias animam o seu `width` do `0` a `100%` com o scroll.

### Responsividade
- Grid de 2x2 vira 1x4 no mobile. Tamanho das fontes dos números vai para `3.5rem`.

---

## Seção 7: Como Funciona

### Arquétipo e Constraints
- **Arquétipo:** Scroll Storytelling (Vertical Timeline)
- **Constraints:** Path Animation, Fade Left/Right alternado.
- **Justificativa:** Explica o processo passo a passo, segurando a atenção do usuário com uma linha conectiva que cresce a medida que rola a página para baixo.

### Conteúdo
- **Título:** Processo prático e focado em resultados
- **Passo 1:** Diagnóstico inicial (Compreendemos sua realidade e desafios fiscais).
- **Passo 2:** Análise técnica (Avaliamos documentos e oportunidades de economia).
- **Passo 3:** Apresentação das oportunidades (Mostramos caminhos claros e benefícios esperados).
- **Passo 4:** Execução do projeto (Conduzimos todas as etapas técnicas e jurídicas).
- **Passo 5:** Acompanhamento (Garantimos suporte e transparência contínua).

### Layout
- **Estrutura:** Timeline vertical central. Uma linha fina passa no meio (`width: 2px`).
- **Cards Alternados:** Passo 1 (esquerda), Passo 2 (direita), Passo 3 (esquerda), etc.
- **Dimensões:** Bolinhas numéricas com `width/height: 50px` ancoradas no centro.

### Tipografia
- **Títulos dos passos:** Plus Jakarta Sans, `1.4rem`, weight `700`.
- **Conteúdo dos passos:** Inter, `1.1rem`.

### Cores
- Fundo: `#FAFAFA`.
- Linha timeline: `#E2E8F0` fixa, com a linha ativa (preenchida) sobreposta em `#FFC700`.
- Bolinhas: Fundo `#0A192F`, números em `#FFFFFF`.

### Animações
- **Draw SVG/Line:** O `height` da linha amarela ativa aumenta conforme a rolagem do usuário.
- Ao alcançar a bolinha, ela ilumina (Sombra `0 0 15px rgba(255,199,0, 0.5)`).
- Os cards entram com `fade-left` ou `fade-right`.

### Interatividade
- Hover no card gera pequeno salto de `scale(1.02)`.

### Responsividade
- **Mobile (<768px):** Timeline não fica no centro. Ela vai para a margem esquerda (`left: 20px`), todos os cards ficam à direita (`width: 100%`).

---

## Seção 8: Onde Estamos

### Arquétipo e Constraints
- **Arquétipo:** Split com Overlap (Conteúdo que transborda)
- **Constraints:** Duotone Image (Map), Float Loop, Asymmetric Padding.
- **Justificativa:** Dá solidez geográfica. A imagem (mapa) na direita sem margens cria um aspecto limpo.

### Conteúdo
- **Título:** Atendimento em todo o Brasil
- **Conteúdo:** Contamos com unidades próprias em São Luís (Maranhão) e Curitiba (Paraná), além de uma rede de escritórios parceiros para levar soluções estratégicas a empresas de todas as regiões do país.

### Layout
- **Estrutura:** CSS Grid `40% 60%`. Bloco esquerdo de texto com padding normal (`8rem 10% 8rem 10%`). Bloco direito encostado na direita total (`margin-right: -10%` ou absoluto).
- **Caixa Flutuante:** O bloco de texto está posicionado em uma div branca sobrepondo levemente a imagem/mapa.

### Tipografia
- Título: Plus Jakarta Sans `2.5rem`, color `#0A192F`.
- Corpo: Inter `1.2rem`.

### Cores
- Caixa de texto: `#FFFFFF`.
- Mapa de fundo: Em duotone com opacidade mapeando as cores `Blue` e `Blue-Light`.

### Elementos Visuais
- Imagem estilizada do Brasil (SVG ou PNG em `#112B52`).
- Três Pins geolocalizados pulsando sobre São Luís, Curitiba e outro genérico.

### Animações
- **Pulse Loop:** Pins com borda expandindo infinitamente `box-shadow` e desaparecendo.

### Responsividade
- Torna-se empilhado, o bloco flutuante encaixa logo abaixo do texto no mobile.

---

## Seção 9: CTA Final

### Arquétipo e Constraints
- **Arquétipo:** Spotlight Hero
- **Constraints:** Radial Gradient Background, Text Reveal, Botão com Ripple Effect.
- **Justificativa:** Conclui a narrativa como no topo: forte e direto ao ponto, com um convite irrecusável à ação.

### Conteúdo
- **Título:** Descubra como sua empresa pode economizar com segurança
- **Conteúdo:** Quer saber se a sua empresa possui créditos a recuperar ou oportunidades reais de redução de custos? Solicite uma análise da nossa equipe técnica.
- **CTA:** Falar com um consultor

### Layout
- **Estrutura:** `Flexbox Column`, completamente centralizado, padding `8rem 5%`.
- **Espaço:** Content `max-width: 700px`.

### Tipografia
- **Título:** Plus Jakarta Sans, `3rem`, text-align center.
- **Subtexto:** Inter, `1.2rem`, text-align center.

### Cores
- **Fundo:** `#0A192F` com Spotlight. Um `Radial Gradient` saindo do centro (`rgba(255, 199, 0, 0.08)`) esvanecendo nas pontas.
- **Textos:** Brancos `#FFFFFF`.
- **Botão:** `#FFC700`, texto em `#0A192F`.

### Animações
- **Reveal no Scroll:** Entrada macia `scale(0.95)` to `scale(1)` e opacidade.
- **Botão pulse:** Chama a atenção pulando a cada 5 segundos levemente.

### Interatividade
- O mesmo efeito de elevação (`transform: translateY(-4px)`) do CTA do Header principal.

### Responsividade
- Títulos flexíveis com `clamp()`. Redução de padding horizontal no mobile.
