# 🍔 Cardápio Digital & Gestão de Fiado

Sistema web completo e leve desenvolvido para pequenos estabelecimentos comerciais (lanchonetes, restaurantes, bares e mercearias). O projeto integra cardápio interativo para clientes com painel administrativo de produtos, gestão de pedidos e controle de consumo fiado com cobrança em um clique pelo WhatsApp.

---

## 🚀 Demonstração

- **Cardápio (Cliente):** [https://tiagossylva.github.io/cardadioVendas/](https://tiagossylva.github.io/cardadioVendas/)
- **Painel Administrativo:** `login.html` (Acesso restrito via usuário e senha)

---

## 🛠️ Tecnologias Utilizadas

- **Front-end:** HTML5, CSS3, JavaScript puro (Vanilla JS)
- **Hospedagem:** GitHub Pages (SSL/HTTPS gratuito)
- **Backend / API:** Google Apps Script (Web App REST)
- **Banco de Dados:** Google Sheets (Planilha ativa com persistência em tempo real)

---

## ✨ Funcionalidades

### 📱 Para o Cliente (Cardápio)
- Visualização de itens com foto, nome e preço atualizados dinamicamente da planilha.
- Seleção de quantidades com botões interativos (`+` e `-`).
- Carrinho fixo com valor total recalculado em tempo real e opção de limpar seleção.
- Coleta de dados essenciais: Nome, WhatsApp (com máscara automática) e Observações do item.

### 🛡️ Para o Administrador (Gestão)
- **Autenticação Segura:** Acesso às páginas gerenciais protegido por tela de login e controle de sessão (`sessionStorage`).
- **Gerenciamento de Cardápio (`admin.html`):** Cadastro de novos produtos com imagem e exclusão direta.
- **Painel de Pedidos (`pedidos.html`):** Visualização dos pedidos com status visível e modal para edição de dados (itens, valor, observações e cliente).
- **Relatório Financeiro & Fiado (`relatorios.html`):**
  - Indicadores no topo com **Total Selecionado**, **Total em Aberto (Fiado)** e **Total Já Pago**.
  - Filtro por status (`Todos`, `Em Aberto/Pendente`, `Pago`) e busca dinâmica por nome ou telefone.
  - Agrupamento inteligente por cliente, consolidando múltiplos pedidos.
  - **Cobrança via WhatsApp:** Gera link direto com mensagem amigável contendo o histórico detalhado de todas as compras daquele cliente e o saldo final a pagar.
  - Baixa rápida de pagamentos (`Marcar como Pago` ou `Cancelar Débito`).

---

## 📁 Estrutura de Abas da Planilha

Para o funcionamento correto do Google Apps Script, a planilha associada utiliza as seguintes abas:

1. **`Pedidos`:** `ID` | `Data/Hora` | `Cliente` | `Telefone` | `Itens` | `Observações` | `Total` | `Status`
2. **`Produtos`:** `ID` | `Nome` | `Preco` | `ImagemURL` | `Ativo`
3. **`Config`:** `Chave` | `Valor` (Suporte a Kill Switch e dados de chave Pix)

---

## 📄 Licença

Projeto desenvolvido para fins comerciais e de portfólio.
