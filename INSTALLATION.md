# Instruções de Instalação e Configuração

## Pré-requisitos

- Node.js 18+ instalado
- npm ou yarn
- MongoDB (local ou Atlas)
- Conta Cloudinary (para upload de imagens)

## Passos de Instalação

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

Crie um arquivo `.env.local` na raiz do projeto com as seguintes variáveis:

```env
# MongoDB
MONGODB_URI=mongodb://localhost:27017/instrumentos-musicais
# ou para MongoDB Atlas:
# MONGODB_URI=mongodb+srv://usuario:senha@cluster.mongodb.net/instrumentos-musicais

# NextAuth
NEXTAUTH_SECRET=sua-chave-secreta-aqui
NEXTAUTH_URL=http://localhost:3000

# Cloudinary (para upload de imagens)
NEXT_PUBLIC_CLOUDINARY_CLOUD_NAME=seu-cloud-name
NEXT_PUBLIC_CLOUDINARY_API_KEY=sua-api-key
CLOUDINARY_SECRET=seu-secret

# Opcional: Para integração com API real de PIX em produção
# PIX_API_KEY=sua-chave-pix
# PIX_API_URL=https://api-pix.seu-banco.com
```

### 4. Executar Migrations de Banco de Dados (se necessário)

```bash
npm run seed
```

## Executando o Projeto

### Desenvolvimento

```bash
npm run dev
```

Acesse `http://localhost:3000` no seu navegador.

### Build para Produção

```bash
npm run build
npm start
```

## Estrutura de Imagens

As imagens dos produtos devem ser colocadas em `/public/images/`:

```
public/
└── images/
    ├── violao1.jpg
    ├── guitarra1.jpg
    ├── teclado1.png
    ├── bateria1.jpg
    ├── saxofone1.jpg
    ├── baixo1.jpg
    ├── banner1.jpg
    └── banner2.jpg
```

## Usuários Padrão

Após executar o seed, os seguintes usuários estarão disponíveis:

**Admin:**
- Email: `admin@example.com`
- Senha: `123456`

**Usuário Normal:**
- Email: `tati@example.com`
- Senha: `123456`

## Fluxo de Teste

1. Acesse `http://localhost:3000`
2. Navegue pelos produtos
3. Adicione itens ao carrinho
4. Proceda ao checkout
5. Selecione "PIX" como método de pagamento
6. Confirme o pedido
7. Na página de detalhes do pedido, clique em "Gerar QR Code PIX"
8. Escaneie o QR Code (simulado)
9. Clique em "Confirmar Pagamento"

## Painel Administrativo

Acesse `/admin` para:
- Gerenciar produtos
- Visualizar pedidos
- Gerenciar usuários
- Ver relatórios de vendas

## Troubleshooting

### Erro de Conexão MongoDB

Certifique-se de que:
- MongoDB está rodando localmente (`mongod`)
- A string de conexão está correta em `.env.local`
- Firewall não está bloqueando a porta 27017

### Erro de Cloudinary

- Verifique suas credenciais do Cloudinary
- Certifique-se de que a API Key está ativa

### Erro de Build

```bash
# Limpar cache
rm -rf .next node_modules
npm install --legacy-peer-deps
npm run build
```

## Deploy

### Vercel (Recomendado)

1. Faça push do código para GitHub
2. Conecte o repositório no Vercel
3. Configure as variáveis de ambiente
4. Deploy automático

### Outras Plataformas

Siga a documentação do Next.js para deploy em outras plataformas.

## Suporte

Para dúvidas ou problemas, abra uma issue no repositório.
