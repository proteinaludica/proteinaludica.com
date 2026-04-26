# Proteína Lúdica — Registo de Decisões v2.2

> Memória viva do projecto. Anexar a novos chats para arranque sem ruído.
> **Última actualização:** 21 Abril 2026 — sessão de regeneração dos 3 HTMLs alinhados com v2.1 e definição do fluxo de trabalho no Claude (arquivar vs apagar, convenção de nomes, rotina de sessão).
>
> **Este ficheiro substitui o `decisoes-proteina-ludica.md` anterior.**

---

## Contexto

**Empresa:** Proteína Lúdica, Lda.
**Sede:** Seixal, Região Autónoma da Madeira.
**Fundador:** Roberto Gouveia, médico.
**Domínio:** `proteinaludica.com`.

**Natureza:** healthtech madeirense. Secretários digitais IA **não-clínicos**, para profissionais. Preferência declarada: poucos produtos bem feitos.

---

## Regras absolutas (intocáveis)

1. **Nunca misturar a DRC do Roberto com a marca Proteína Lúdica.** A história pessoal não entra na narrativa pública da empresa.
2. **Nunca identificar a Dra. Mónica Armas.** O caso dela é privado. Pode ser usado como prova social apenas de forma anónima ("radiologista sénior especializada em patologia da mama"), nunca com o nome.
3. **Posicionamento legal:** não-clínico, não-dispositivo médico. Não substitui avaliação médica, diagnóstico ou prescrição.
4. **RGPD EU-only.** DPA com todos os subcontratantes. Consentimento explícito. Zero-retention nos LLMs.

---

## Vocabulário público — CRÍTICO

Testes com médicos amigos em Abril 2026 mostraram que vocabulário técnico **não passa**. Regra fundamental:

**Usar SEMPRE:** "secretário digital"
**Nunca usar em público:** "agente IA", "assistente digital IA", "LLM", "plataforma", "system instructions", "prompt"

| Antes (técnico) | Depois (público) |
|---|---|
| "agente IA" | **"secretário digital"** (metáfora central) |
| "onde vive o agente" | "que ferramenta vai usar" |
| "LLM / plataforma" | "ferramenta" (raramente mencionado) |
| "system instructions" | "configuração" |
| "17 secções" | "17 perguntas" |
| "template" | "modelo pronto" |

**Tom público:** explicação a alguém de 70 anos. Frases curtas. Tratamento por **"você"** e **"o senhor"**. Palavras de rua. Metáforas concretas.

**Tagline central:** *"Um secretário digital que escreve por si."*

O termo "agente IA" só existe no vocabulário técnico interno (backoffice, documentação para devs, conversas Roberto-Claude).

---

## Arquitectura de negócio

Três segmentos distintos.

### A — Saúde · Produtos prontos (catálogo)

Secretários digitais estandardizados por especialidade. Nomes públicos simplificados.

| Secretário | Público | Estado |
|---|---|---|
| **Dr. Escriba** | Médicos de família + urgência | Disponível (1€/dia) |
| **Dr. Escriba · Internato** | Internos de especialidade | Em breve — produto distinto, não variante |
| **Assistente de Clínica** | Clínicas privadas pequenas | Piloto no Funchal |
| **RehabAssist** | Fisiatras + doentes em casa | A ser construído |
| **Assistente de Saúde** | Pessoas com doenças crónicas | Em breve |

**Modelo de preço do catálogo:** ainda não decidido. Decisão adiada até haver dados de 3-5 pilotos reais.

### B — Secretários digitais à medida

**Estrutura confirmada em Abril 2026 — duas pirâmides paralelas:**

#### B.1 · Individual (um profissional, um secretário)

| Nível | Preço | O que inclui | Para quem |
|---|---|---|---|
| **Grátis** | 0€ | System prompt gerado · sem instruções de instalação · captura email | Curiosos, marketing |
| **Básico** | 19€ | System prompt + guia de instalação manual na plataforma | Quem já percebe de computadores |
| **Premium** | 49€ | Tudo do Básico + IA conversa para ajudar a preencher as 17 perguntas | Quem não é técnico mas prefere self-service |
| **Assistido** | 290€ (Madeira) / 490€ (normal) | Roberto 1h de chamada + ficha preenchida + 14d suporte email | Quem quer ajuda humana |

**Preço Madeira introdutório** (tier Assistido): para os primeiros 10 clientes locais. Depois volta ao preço normal.

#### B.2 · Equipa (empresa ou grupo de profissionais)

| Nível | Preço | O que inclui | Para quem |
|---|---|---|---|
| **Equipa** | 990€ *(provisório)* | Secretário "mãe" com regras comuns + versões por papel (ex: médico, enfermeira, recepção). Qualquer profissão — não é só saúde. | Clínicas, escritórios, gabinetes |

**IMPORTANTE — preço 990€ é provisório.** A arquitectura "mãe + papéis" é tecnicamente mais complexa que um secretário individual. Esforço real pode justificar 1.990€ a 2.990€. **Decisão final adiada até ter o primeiro cliente-piloto real** para calibrar tempo de trabalho.

**Questões em aberto do tier Equipa:**
- Número de pessoas que cabem no pacote base (ainda não definido)
- Número de papéis incluídos vs cobrados à parte
- Modelo de actualização quando o "mãe" muda (quem paga manutenção?)
- Adaptação a plataformas multi-utilizador (Copilot M365 vs Claude Projects vs Gemini Gems)

**Questão em aberto comum a individual e equipa:** distinguir ou não o **número de secções** entre tiers. Hipótese em cima da mesa: 19€ usa versão reduzida de 7-9 secções core, 49€ usa as 17 completas. Decisão adiada — *decidimos depois de ver o protótipo do wizard actualizado*.

### C — Alojamento local (segmento secundário)

**C.1 — Casa da Albertina** (Seixal / Porto Moniz). Não central. Página discreta no footer do site.
**C.2 — Vertical futuro** (agentes IA para outros donos de AL). Lançamento previsto Q4 2026 / 2027.

### D — Rede não-saúde (teaser 2027)

Advogados, arquitectos, engenheiros, contabilistas, notários. **Roberto tem contactos reais** em algumas destas áreas (engenharia civil, arquitectura, herdeiros). Decisão pendente: teaser vago ("em breve 2027") **ou** anunciar parcerias já em negociação.

**Decisão em Abril 2026:** manter teaser vago por agora. Parcerias reais acelerariam o timeline para 2026 e não é prioridade.

---

## Wizard /criar — arquitectura

### Entrada
- URL: `proteinaludica.com/criar` (dentro do site principal, não subdomínio)
- Aberto a qualquer visitante sem login
- Serve segmento B.1 (individual). O segmento B.2 (equipa) usa contacto directo, não wizard.

### Fluxo do wizard (a refazer após auditoria de Abril 2026)

**O wizard `/criar` serve o segmento B.1 (individual).** O segmento B.2 (Equipa, 990€ provisório) **não usa o wizard self-service** — é sempre um processo humano liderado pelo Roberto, dada a complexidade da arquitectura "mãe + papéis".

**Passo 0 (a criar):** página tradutor — explica em 60 segundos o que é um secretário digital, com linguagem acessível. Ponte de entrada para quem chega sem saber. No fim oferece dois caminhos: "Para si" (continua no wizard) ou "Para a sua equipa/clínica" (vai directo para contacto B.2).

**Passo 1:** escolha de plataforma — 7 cards (Claude Projects · ChatGPT Custom GPTs · Google Gemini Gems · Microsoft Copilot Agents · Perplexity Spaces · Mistral Le Chat · Outro). Botão "Responder a 3 perguntas e receber recomendação" abre quiz.

**Passo 2:** ponto de partida — clonar do catálogo OU template em branco de 17 secções.

**Passo 3:** preenchimento — 17 secções, uma por ecrã, barra de progresso, exemplo real anonimizado ao lado, detector RGPD inline, save state localStorage.

**Passo 4 (Grátis 0€):** apenas o system prompt gerado em caixa de código + botão *Copiar*. **Sem guia de instalação.** Banner de upgrade para 19€ (Básico) e 49€ (Premium).

**Passo 5 (Básico 19€):** paywall. Adiciona guia de instalação específico da plataforma + PDF formatado + checklist RGPD + template consentimento doentes.

**Passo 6 (Premium 49€):** alternativo ao 19€. IA conversacional ajuda a preencher as 17 secções durante o Passo 3. Output igual ao Básico mas com preenchimento guiado.

**Ponte para humano (Assistido 290€):** botão permanente em todos os passos — "Prefere que façamos por si?" — redirecciona para formulário de contacto.

### Saída do agente ("agente completo")

Para cada plataforma, a saída inclui **todos os componentes necessários** para criar o agente, não apenas o prompt:

| Componente | Gemini Gems | Custom GPT | Claude Projects | Copilot Agents |
|---|---|---|---|---|
| Título / Nome | ✓ | ✓ | ✓ | ✓ |
| Descrição curta | ✓ | ✓ | — | ✓ |
| System prompt (Instructions) | ✓ | ✓ | ✓ (Project Instructions) | ✓ |
| Ficheiros a anexar | ✓ | ✓ (Knowledge) | ✓ (Knowledge) | ✓ |
| Conversation Starters | — | ✓ | — | — |
| Topics | — | — | — | ✓ |
| Prompts de teste | ✓ (gerados) | ✓ (gerados) | ✓ (gerados) | ✓ (gerados) |

### Pagamento
- **Stripe** para cartão (activação imediata)
- **MB WAY via IfthenPay** (activação quando contrato estiver aprovado, 1-2 semanas)
- Reembolso 7 dias sem perguntas

---

## 17 secções da estrutura do agente

Organizadas em 4 blocos:

**Bloco 1 — Identidade:** 1. Nome e propósito · 2. Missão · 3. Público-alvo · 4. Contexto local
**Bloco 2 — Personalidade:** 5. Voz e tom · 6. Linguagem · 7. Estilo de resposta
**Bloco 3 — Funcionamento:** 8. Onboarding · 9. Protocolo de reconhecimento · 10. Tarefas específicas · 11. Fontes oficiais · 12. Conhecimento técnico
**Bloco 4 — Segurança e fecho:** 13. Red lines · 14. Alertas de emergência · 15. Tratamento de dados · 16. Fecho dinâmico · 17. Continuidade

**5 obrigatórias mínimas:** 1 (nome), 2 (missão), 13 (red lines), 14 (emergências), 16 (fecho).

**Exemplo completo preenchido** existe no ficheiro `17-seccoes-exemplo.html` (Dr. Roberto IA).

**Questão em aberto:** confirmação de que 17 é o número certo vs reduzir para 7-9 core. Frameworks consagradas de Gems/GPTs usam 6-9 componentes. Decisão a tomar após protótipo.

---

## Stack técnica (decidida)

**Frontend:** Next.js 15 (App Router) + TypeScript + Tailwind v4.
**Deploy:** Vercel.
**Backend/DB:** Supabase EU.
**CDN:** Cloudflare.
**Pagamentos:** Stripe + IfthenPay (MB WAY/Multibanco PT).
**LLM Gateway:** Gemini (Vertex EU) / Claude / GPT, zero-retention.
**Processamento:** stateless. PDF in → PDF out. Link 24h.

**Domínios:**
- `proteinaludica.com` — home institucional
- `proteinaludica.com/criar` — wizard (dentro do site principal)
- `drescribaai.proteinaludica.com` — ficha Dr. Escriba (existente)
- `drescriba-internato.proteinaludica.com` — ficha Internato (pendente)
- `rehabassist.proteinaludica.com` — ficha RehabAssist (pendente)
- `gestordesaude.proteinaludica.com` — ficha Assistente de Saúde (pendente)
- `ajuda.proteinaludica.com` — ficha Assistente de Clínica (pendente)
- `app.proteinaludica.com` — reservado futuro (auth/dashboard)

**Identidade visual:**
- Direcção: Clínico-Tech (híbrido)
- Paleta Laurissilva Digital: verde musgo `#8FAA6B` + ocre `#C8A86B` sobre `#0B0E0C`
- Tipografia: Fraunces (serifa) + Geist (sans) + Geist Mono
- Logotipo e símbolo próprio: pendente

---

## Ficheiros já gerados

| Ficheiro | Estado (21 Abril 2026) | Notas |
|---|---|---|
| `index.html` | **Alinhado v2.1** | Vocabulário "secretário digital", pirâmide dupla (Individual 0/19/49/290€ + Equipa 990€), paleta Laurissilva, FAQ 6 perguntas, Rede 2027 |
| `wizard-criar.html` | **Alinhado v2.1** | 7 passos navegáveis (0-6), tradutor inicial, escolha de plataforma com quiz, detector RGPD, paywall diferenciado por tier, floating help para Assistido 290€ |
| `17-seccoes-exemplo.html` | **Alinhado** | Exemplo completo Dr. Roberto IA (Ponta Delgada, código `med46316`, 8 etapas onboarding, red lines), TOC sticky, componentes do "agente completo" |

**Pendente de produzir:** ficheiro de demonstração da saída do wizard (agente completo para o Dr. Roberto IA em cada plataforma: Gemini Gems, Custom GPT, Claude Projects, Copilot Agents) — ver item 2 dos próximos passos.

---

## Fluxo de trabalho no Claude (meta)

Como organizar o trabalho entre chats e manter este ficheiro como única fonte de verdade.

### Três camadas de memória

1. **Ficheiros do projecto** (`decisoes-proteina-ludica.md`, `Dr_Robert_IA_Google_Gemini.pdf`) — acompanham todos os chats automaticamente. Verdade oficial.
2. **Chats** — sessões descartáveis. Não partilham contexto entre si.
3. **`conversation_search`** — procura cruzada em chats antigos (mesmo arquivados). Por isso arquivar é quase sempre melhor que apagar.

### Rotina por sessão (obrigatória)

1. Abrir chat novo
2. Primeira mensagem: objectivo em 2-3 linhas (o `decisoes.md` já está anexo)
3. Trabalhar
4. No fim: pedir actualização do `decisoes.md` com nova versão no changelog
5. Descarregar ficheiro actualizado e fazer upload ao projecto (substitui o anterior)
6. Arquivar o chat

### Convenção de nomes dos chats

Prefixo por categoria para tornar a lista lateral legível:

- `[DEC]` — chats de decisão (preços, posicionamento, regras). Output: actualização do `decisoes.md`
- `[PROD]` — chats de produção (HTMLs, contratos, emails, scripts). Output: ficheiros descarregáveis
- `[EXP]` — chats de exploração sem compromisso. Descartáveis
- `[DRESC]`, `[REHAB]`, `[SAUDE]`, etc. — chats específicos de um produto do catálogo

### Arquivar vs apagar

- **Arquivar por defeito.** Tira da lista principal, mantém `conversation_search` activo, recuperável.
- **Apagar** só depois de confirmar que qualquer artefacto útil está descarregado localmente e que a decisão relevante já está no `decisoes.md`.

### Backup local recomendado

Pasta `~/proteinaludica/` no computador do Roberto com subpastas:
- `html/` — versões dos 3 HTMLs por data
- `decisoes/` — histórico de versões do `decisoes.md` (v1.0, v2.0, v2.1, v2.2…)
- `contratos/`, `pdf/`, `scripts/` — à medida que aparecerem

Os chats no Claude podem desaparecer por qualquer motivo técnico; a pasta local é o único seguro verdadeiro.

---

---

## Próximos passos imediatos (ordem)

1. ~~Actualizar `index.html` com estrutura de 5 níveis de preço na secção #medida.~~ ✅ **Feito (21 Abril 2026).**
2. **Criar ficheiro de demonstração** da saída completa do wizard (título + descrição + system prompt + ficheiros + prompts de teste) para o Dr. Roberto IA em cada plataforma (Gemini Gems, Custom GPT, Claude Projects, Copilot Agents), para validar antes de codificar.
3. ~~Refazer `wizard-criar.html` com nova linguagem ("secretário digital"), 5 níveis de preço, paywall com 3 saídas distintas.~~ ✅ **Feito (21 Abril 2026).**
4. **Decidir número final de secções** (17 vs 7-9 core) após ver o wizard actualizado e o ficheiro de demonstração.
5. **Testar wizard actualizado** com 3-5 médicos amigos que não perceberam a V1 (preferencialmente os mesmos, para comparar).
6. **Produção de vídeo/áudio/imagens** (pausada, retomar quando homepage e wizard estiverem validados com utilizadores reais).
7. **Desenvolvimento Next.js** do wizard real (só depois da validação HTML com médicos).

---

## Divisão de trabalho Roberto / Claude

**Roberto faz:**
- Responder em 24h a quem contactar
- Assinar contratos
- Cara pública da empresa
- Conversa de 1h no Assistido individual (290€)
- Projectos de Equipa (990€ provisório): negociação, descoberta das regras comuns, definição de papéis, instalação na clínica/escritório

**Pitch de 1 frase (decorar):**
> *"Faço secretários digitais para profissionais. Escrevem as notas por eles. Eu faço a parte difícil, eles só usam. Trabalho com médicos, advogados, clínicas — qualquer profissão com muita papelada."*

**Claude faz (através do Roberto):**
- Toda a parte técnica (estrutura das 17 secções, blocos de configuração, setup)
- Toda a parte comercial escrita (landing, emails, FAQ, scripts, contratos)
- Preparação de respostas a objecções
- Apoio em conversas do Assistido (redacção pós-chamada)
- Arquitectura "mãe + papéis" para tier Equipa (desenho e geração dos múltiplos secretários)

---

## Princípios transversais do produto

- Não-clínico, não-dispositivo médico
- Stateless. PDF in → PDF out. Link 24h
- Zero dados clínicos no servidor
- EU-only. DPA com subcontratantes
- Pseudonimização obrigatória (iniciais + idade)
- Nunca aceita: nome completo, nº utente, nº processo, data nascimento, morada
- RGPD aplicado desde o design

---

## Decisões expressamente rejeitadas (não voltar a propor)

- "Família Sombra" como naming unificador dos secretários — rejeitada
- "Método Sombra" como produto — rejeitada
- Preço único para secretários do catálogo — incompatível com stack
- História fundacional da DRC na narrativa pública — proibida por regra absoluta
- Identificação da Dra. Mónica em materiais comerciais — proibida por regra absoluta
- Vocabulário "agente IA" em comunicação pública — rejeitada após testes (Abril 2026)
- Narração de vídeo com actores humanos reais gerados por IA — rejeitada (uncanny valley, mata confiança)
- Guia de instalação gratuita — rejeitada, fica a partir do 19€

---

## Pendentes (em aberto)

1. Confirmar número de secções (17 vs 7-9 core) após protótipo
2. Tagline final (actual: "Um secretário digital que escreve por si.")
3. Logo e símbolo próprio
4. Landing page finalizada com pirâmide dupla (individual + equipa)
5. Deploy Vercel apontado a `proteinaludica.com`
6. Script do vídeo-guia de 10 min (incluído no tier Básico 19€ — reavaliar formato)
7. Contrato de subcontratante RGPD para Assistido (290€) e Equipa (990€)
8. Validação com TOC do modelo de facturação
9. Autorização da Dra. Mónica para caso anónimo
10. Email de resposta automática para leads
11. FAQ final com 10 perguntas (já temos 6 no index v2)
12. Decisão sobre Casa da Albertina: quando contar publicamente
13. Activação IfthenPay para MB WAY (1-2 semanas de setup)
14. Escolha final de LLM para a IA que ajuda no wizard (Premium 49€)
15. Produção do kit vídeo/áudio/imagens (pausada)
16. Teste do wizard actualizado com médicos amigos
17. Definição de ficheiros sugeridos e prompts de teste por especialidade
18. **Preço final do tier Equipa** — após primeiro cliente real
19. **Arquitectura técnica mãe + papéis** — como se implementa em cada plataforma (Copilot, Claude, Gemini)
20. **Modelo de manutenção do tier Equipa** — quem paga actualizações quando a clínica muda regras?

---

## Changelog

**v2.2 · 21 Abril 2026:**
- 3 HTMLs regenerados e **alinhados com v2.1** após auditoria (vocabulário "secretário digital" confirmado por grep: 0 ocorrências de "agente IA" em ficheiros públicos)
- Itens 1 e 3 dos próximos passos marcados como concluídos (homepage actualizada, wizard refeito)
- Nova secção **Fluxo de trabalho no Claude (meta)** — três camadas de memória, rotina obrigatória por sessão, convenção de nomes `[DEC]`/`[PROD]`/`[EXP]`/`[DRESC]`, regra arquivar-por-defeito, estrutura de backup local `~/proteinaludica/`
- Decisão: arquivar chats antigos em vez de apagar (mantém `conversation_search` funcional)

**v2.1 · Abril 2026 (depois da v2.0 da mesma sessão):**
- Tier 990€ passou de "Completo individual" para **"Equipa"** (qualquer profissão, não só saúde)
- Arquitectura 990€: secretário "mãe" com regras comuns + versões por papel (médico/enfermeira/recepção, advogado/associado/secretária, etc.)
- Preço 990€ marcado como **provisório** — decisão final após primeiro cliente real (pode subir para 1.990€-2.990€)
- Estrutura passa de 5 níveis lineares para **duas pirâmides paralelas**: Individual (0€/19€/49€/290€) e Equipa (990€)
- Wizard self-service serve apenas segmento individual. Equipa usa contacto directo.
- Segmento B deixa de ser "Saúde · à medida" — passa a "Secretários à medida" para qualquer profissão

**v2.0 · Abril 2026:**
- Vocabulário público fixo em "secretário digital"
- Estrutura de preços expandida (antes 3 tiers, passou a 5 níveis antes da v2.1)
- Gratuito inclui system prompt sem guia de instalação
- Saída do wizard passa a ser "agente completo" (título + descrição + prompt + ficheiros + testes)
- Linguagem pública adaptada para "alguém de 70 anos" / tratamento por "você"
- IA a ajudar preencher passa a ser do tier 49€ (Premium)
- Dr. Escriba Internato confirmado como produto distinto, não variante

**v1.0 · anterior:**
- 3 tiers (0€/290€/990€)
- Vocabulário "agente IA" em todo o lado
- Apenas system prompt como saída
