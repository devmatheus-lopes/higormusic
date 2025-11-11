# Loja de Instrumentos Musicais

Uma loja online moderna para venda de instrumentos musicais, construída com Next.js, TypeScript, MongoDB e PIX para pagamentos.

## 🎵 Características

- **Catálogo de Instrumentos**: Violões, Guitarras, Teclados, Baterias, Saxofones e Baixos
- **Sistema de Carrinho**: Adicione e gerencie itens no carrinho
- **Checkout Seguro**: Processo de checkout em múltiplas etapas
- **Pagamento via PIX**: Geração de QR Code aleatório para teste
- **Autenticação**: Registro e login de usuários
- **Painel Administrativo**: Gerenciamento de produtos e pedidos
- **Avaliações**: Sistema de avaliações de produtos
- **Busca**: Funcionalidade de busca de produtos
- **Responsivo**: Design adaptável para todos os dispositivos

## 🛠️ Tecnologias

- **Frontend**: Next.js 14, React 18, TypeScript
- **Estilo**: Tailwind CSS, DaisyUI
- **Backend**: Next.js API Routes
- **Banco de Dados**: MongoDB
- **Autenticação**: NextAuth.js
- **Pagamentos**: PIX (com geração de QR Code)
- **Upload de Imagens**: Cloudinary
- **Gerenciamento de Estado**: Zustand
- **Validação**: React Hook Form

## 📋 Pré-requisitos

- Node.js 18+
- npm ou yarn
- MongoDB
- Conta Cloudinary

## 🚀 Início Rápido

### 1. Clonar o Repositório

```bash
git clone https://github.com/seu-usuario/projeto-instrumentos-musicais.git
cd projeto-instrumentos-musicais
```

### 2. Instalar Dependências

```bash
npm install --legacy-peer-deps
```

### 3. Configurar Variáveis de Ambiente

Crie um arquivo `.env.local`:

```env
MONGODB_URI=mongodb://localhost:27017/instrumentos-musicais
NEXTAUTH_SECRET=sua-chave-secreta
NEXTAUTH_URL=http://localhost:3000
NEXT_PUBLIC_CLOUDINARY_CLOUD_NAME=seu-cloud-name
NEXT_PUBLIC_CLOUDINARY_API_KEY=sua-api-key
CLOUDINARY_SECRET=seu-secret
```

### 4. Executar o Projeto

```bash
npm run dev
```

Acesse `http://localhost:3000`

## 📁 Estrutura do Projeto

```
projeto-instrumentos-musicais/
├── app/
│   ├── (front)/              # Páginas da loja
│   │   ├── page.tsx          # Página inicial
│   │   ├── product/          # Detalhes do produto
│   │   ├── cart/             # Carrinho
│   │   ├── payment/          # Método de pagamento
│   │   ├── place-order/      # Resumo do pedido
│   │   └── order/            # Detalhes do pedido
│   ├── admin/                # Painel administrativo
│   └── api/                  # APIs backend
├── components/               # Componentes React
├── lib/
│   ├── data.ts              # Dados de produtos
│   ├── pix.ts               # Geração de QR Code PIX
│   ├── models/              # Modelos MongoDB
│   └── services/            # Serviços
├── public/                  # Arquivos estáticos
└── types/                   # Tipos TypeScript
```

## 💳 Fluxo de Pagamento PIX

1. Selecione "PIX" como método de pagamento
2. Confirme o pedido
3. Na página de detalhes, clique em "Gerar QR Code PIX"
4. Escaneie o QR Code com seu app bancário
5. Clique em "Confirmar Pagamento"
6. Pedido marcado como pago

## 👤 Usuários Padrão

**Admin:**
- Email: `admin@example.com`
- Senha: `123456`

**Usuário:**
- Email: `tati@example.com`
- Senha: `123456`

## 📝 Alterações da Migração

- ✅ Produtos alterados de lingerie para instrumentos musicais
- ✅ PayPal removido e substituído por PIX
- ✅ QR Code aleatório para teste
- ✅ Nova API de confirmação de pagamento PIX
- ✅ Interface atualizada para PIX

Veja [MIGRATION_SUMMARY.md](./MIGRATION_SUMMARY.md) para detalhes completos.

## 📚 Documentação

- [Instruções de Instalação](./INSTALLATION.md)
- [Resumo da Migração](./MIGRATION_SUMMARY.md)
- [Next.js Documentation](https://nextjs.org/docs)

## 🤝 Contribuindo

Contribuições são bem-vindas! Por favor, abra uma issue ou pull request.

## 📄 Licença

Este projeto está sob a licença MIT.

## 👨‍💻 Autor

Migração realizada em 11 de Novembro de 2025

---

**Nota**: Este é um projeto de demonstração. Em produção, integre com uma API real de PIX.
