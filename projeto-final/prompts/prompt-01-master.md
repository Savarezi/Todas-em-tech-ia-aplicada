# PROMPT 01 — PROMPT MASTER DE DESENVOLVIMENTO FULL-STACK

## 1. PAPEL E OBJETIVO
Atue como um engenheiro de software sênior, arquiteto de soluções full-stack, especialista em Supabase, PostgreSQL, segurança de aplicações, UX/UI e integração de Inteligência Artificial.

Desenvolva um aplicativo web responsivo chamado **Brechó Delas**, uma plataforma digital exclusiva para mulheres, voltada à troca e à doação gratuita de itens em bom estado de conservação.

O objetivo é construir um MVP REAL, com frontend, backend, banco de dados, autenticação, armazenamento de imagens, regras de segurança e funcionalidades integradas.

**ATENÇÃO: NÃO QUERO APENAS UM PROTÓTIPO VISUAL.** Quero uma aplicação funcional, com arquitetura preparada para evolução e integração real com Supabase.

---

## 2. IDENTIDADE E PROPÓSITO DO PRODUTO
- **Nome:** Brechó Delas (posteriormente atualizado para Garimpo Delas)
- **Slogan:** Compartilhe o que você não usa. Descubra o que outra mulher pode oferecer.

### REGRA FUNDAMENTAL
É expressamente proibido implementar funcionalidades de venda. Não implementar preços, carrinho, checkout, pagamentos, comissões ou carteira digital. Todas as publicações devem ter a modalidade de troca ou doação gratuita.

---

## 3. IDENTIDADE VISUAL E DESIGN
Crie uma interface moderna, elegante, feminina e acolhedora.
- **Roxo profundo:** `#56356F`
- **Roxo principal:** `#76509A`
- **Lilás suave:** `#EEE7F4`
- **Fundo claro:** `#FAF9FB`
- **Branco:** `#FFFFFF`
- **Verde sustentável:** `#54866B`

---

## 4. FUNCIONALIDADES ESSENCIAIS DO MVP
1. **Autenticação (Supabase Auth):** Cadastro completo, login, logout e recuperação de senha.
2. **Feed de Publicações:** Listagem de itens reais, filtros por categoria, modalidade, cidade e busca.
3. **Perfil da Usuária:** Gerenciamento de dados pessoais, foto, visualização de itens próprios e favoritos.
4. **Publicação de Itens:** Upload de fotos (Supabase Storage), título, descrição, categoria, estado de conservação e modalidade.
5. **Interações:** Curtidas, favoritos e botão de interesse integrado ao WhatsApp (`wa.me`).
6. **Histórico:** Organização de itens por status (disponíveis, reservados, trocados, doados).
7. **Assistente de IA:** Sugestão de categoria, título e descrição a partir da imagem do produto.
8. **Segurança (RLS):** Ativação rigorosa de Row Level Security em todas as tabelas do PostgreSQL.
