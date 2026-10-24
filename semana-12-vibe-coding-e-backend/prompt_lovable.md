# 🤖 Prompt Utilizado no Lovable — "Prompt de Lucro"

Aqui está o prompt estruturado e detalhado utilizado para gerar o aplicativo web completo durante as atividades práticas de Vibe Coding:

```text
Crie um aplicativo web completo, responsivo e totalmente funcional chamado "Prompt de Lucro" usando React (Vite/Next.js/Tailwind CSS) e Supabase.

--- DESIGN SYSTEM ---
- Estilo: SaaS Premium 2026 (inspirado em Linear + Notion). Ultra limpo, elegante e moderno.
- Cores: 
  - Fundo principal: #FFFFFF
  - Fundo secundário: #F8F7FF
  - Cor primária: #6C5CE7
  - Texto principal: #1A1A1A
  - Bordas: #E9E5FF
  - Estado de seleção/hover: #F3F0FF
- Tipografia: Inter (Google Fonts).
- Arredondamentos: Botões radius 12px, Cards 16px, Modais/Cards Auth 24px.
- Layout: 100% responsivo e fluido (Mobile-first e Desktop).
- Feedback visual: Toasts e estados de loading para requisições assíncronas.

--- BANCO DE DADOS SUPABASE (ESTRUTURA E RLS) ---
Forneça e execute as rotinas utilizando a estrutura abaixo no Supabase:

1. Tabela `users`:
   - id (uuid, primary key, references auth.users(id) on delete cascade)
   - nome (text)
   - email (text)
   - created_at (timestamp with time zone, default now())

2. Tabela `prompts`:
   - id (uuid, primary key, default gen_random_uuid())
   - user_id (uuid, references auth.users(id) on delete cascade)
   - titulo (text)
   - quem_ia_ser (text)
   - objetivo (text)
   - contexto (text)
   - formato (text)
   - restricoes (text)
   - tom_de_voz (text)
   - exemplo (text)
   - prompt_final (text)
   - favorito (boolean, default false)
   - created_at (timestamp with time zone, default now())

3. Políticas RLS (Row Level Security):
   - Ativar RLS nas tabelas `users` e `prompts`.
   - Garantir que `auth.uid() = user_id` para operações de SELECT, INSERT, UPDATE e DELETE.
   - Criar uma Function + Trigger no Supabase para criar o registro na tabela pública `users` automaticamente após o evento de `auth.signUp`.

--- REGRA CRÍTICA DE AUTENTICAÇÃO ---
- NÃO USE autenticação via Google ou Apple.
- APENAS e-mail e senha tradicionais.
- Trate mensagens de erro amigáveis em português para falhas de login/cadastro.

--- ROTAS E TELAS ---

1. ROTA /login:
   - Fundo: Imagem full-screen (100vw, 100vh, fixed, object-cover) usando Unsplash HD com tema de negócios/mulher trabalhando com gráficos de lucro e IA (ex: [https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?q=80&w=1600&auto=format&fit=crop](https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?q=80&w=1600&auto=format&fit=crop)).
   - Filtro na imagem: `backdrop-filter: blur(8px) brightness(0.8)` e overlay roxo com opacidade 40% (`bg-[#6C5CE7]/40`).
   - Card centralizado: Largura 420px, fundo `#FFFFFF` com 95% de opacidade e `backdrop-blur-md`, sombra `shadow-2xl`, border-radius 24px, padding 40px.
   - Conteúdo do Card:
     - Logo "Prompt de Lucro" com ícone roxo centralizado.
     - Título "Bem-vindo de volta" (bold 24px), subtítulo "Entre com seu e-mail e senha" (cinza).
     - Campo E-mail com ícone de carta e placeholder `seu@email.com`.
     - Campo Senha com ícone de cadeado e botão (olho) para alternar visibilidade da senha.
     - Linha de controle: Checkbox "Lembrar de mim" à esquerda e link "Esqueci minha senha?" à direita (ao clicar, chama `supabase.auth.resetPasswordForEmail`).
     - Botão primário roxo `#6C5CE7` full width "Entrar" com estado de loading ao clicar.
     - Rodapé: "Não tem conta? Criar conta" redirecionando para `/cadastro`.

2. ROTA /cadastro:
   - Fundo idêntico à tela de Login.
   - Card idêntico de 420px.
   - Campos: Nome completo, E-mail, Criar Senha (mínimo 6 caracteres), Confirmar Senha (com validação em tempo real se são iguais).
   - Botão "Criar minha conta" que executa `supabase.auth.signUp`, salva os dados do perfil e redireciona para `/app`.
   - Link "Já tem uma conta? Fazer login" direcionando para `/login`.

3. ROTA /app (Criar Prompt - Protegida por Sessão):
   - Top Nav: Fundo branco, borda inferior `#E9E5FF`. Logo à esquerda, menu central `[Criar Novo]` (ativo) e `[Meus Prompts]`, perfil do usuário e botão `Sair` à direita.
   - Container principal: `max-width: 720px` centralizado.
   - Indicador de Progresso / Passo a Passo elegante com progress bar roxa (25% a 100%).
   - Formulário de Criação de Prompt:
     1. Quem você quer que a IA seja? Input + Chips clicáveis (Advogado, Nutricionista, Copywriter, Vendedor, Professor, Designer). Ao clicar em um chip, preenche o campo.
     2. O que você quer conseguir? Textarea (Ex: "Criar 3 textos para vender meu bolo no Instagram").
     3. Sobre o que é? Textarea grande para contexto detalhado.
     4. Como quer receber? Grid de 4 Cards com ícones (Texto corrido, Lista, Tabela, Roteiro para Reels). Card selecionado ganha borda roxa e fundo `#F3F0FF`.
     5. O que a IA NÃO pode fazer? Input de restrições.
     6. Qual tom de voz? Chips selecionáveis (Direto e Vendedor, Amigável, Profissional, Engraçado, Provocativo).
     7. Tem algum exemplo? Textarea pequeno para referência.
     8. Botão de ação grande roxo: "Gerar meu PROMPT de Lucro 🚀".
   - Resultado em Tela:
     - Ao clicar em gerar, constrói o prompt final usando a estrutura de engenharia de prompt:
       `"Aja como [Campo1]. Seu objetivo é [Campo2]. Contexto: [Campo3]. Formato: [Campo4]. Restrições: [Campo5]. Tom: [Campo6]. Exemplo: [Campo7]. Entregue pronto para gerar lucro."`
     - Salva automaticamente na tabela `prompts` no Supabase com o título extraído das primeiras 5 palavras do Campo 2.
     - Exibe abaixo o Card de Resultado com título, bloco de código estilizado, botão "Copiar Prompt" (com toast de confirmação) e atalho para ir para "Meus Prompts".

4. ROTA /app/meus-prompts (Minha Biblioteca - Protegida):
   - Mesma Top Nav.
   - Barra Superior: Input de busca por palavra-chave + Filtro por abas `[Todos]` `[Favoritos]`.
   - Grid Layout: 2 colunas no Desktop, 1 coluna no Mobile.
   - Card de Prompt:
     - Título em destaque (bold).
     - Data formatada (`dd/mm/aaaa`).
     - Prévia do prompt final (truncada em ~100 caracteres).
     - Ações: Ícone de favoritar (estrela interativa que atualiza no banco), botão Copiar, botão Ver Detalhes e botão Excluir (com confirmação).
   - Modal "Ver Completo":
     - Exibe todo o prompt estruturado.
     - Ações no modal: Copiar, Duplicar (cria uma cópia no banco), Editar (permite alterar e salvar) e Excluir.
   - Empty State: Ilustração/Ícone amigável com mensagem "Nenhum prompt criado ainda" e botão chamativo "Criar meu primeiro prompt".
