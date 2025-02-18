# FastHub+ Front-end

## Descrição do Projeto

FastHub+ é a interface web para o sistema de reservas de eventos. Esta aplicação foi desenvolvida utilizando **Next.js** e consome a API RESTful do back-end para permitir que os usuários cadastrem-se, visualizem eventos e realizem reservas.

## Tecnologias Utilizadas

- **Next.js**: Framework para aplicações React com renderização no servidor (SSR) e geração estática (SSG)
- **TypeScript**: Para tipagem e melhor manutenção do código
- **Tailwind CSS**: Para estilização responsiva e moderna
- **React Query**: Para gerenciamento de estado assíncrono e cache de requisições
- **Zod**: Para validação de formulários e dados
- **Axios**: Para consumo da API do back-end
- **NextAuth.js**: Para autenticação com JWT

## Funcionalidades

- Cadastro e login de usuários
- Listagem de eventos disponíveis
- Detalhes de um evento
- Reserva de ingressos
- Cancelamento de reservas
- Gerenciamento de perfil

## Estrutura de Pastas

```
fast-hub-frontend/
├── components/        # Componentes reutilizáveis
├── pages/             # Rotas do Next.js
│   ├── index.tsx      # Página inicial com listagem de eventos
│   ├── evento/[id].tsx # Página de detalhes do evento
│   ├── reservas.tsx   # Página de reservas do usuário
│   ├── perfil.tsx     # Página de gerenciamento de perfil
├── services/          # Funções para consumir a API
├── hooks/             # Hooks customizados
├── styles/            # Estilos globais
├── utils/             # Funções auxiliares
├── public/            # Assets públicos
├── .env               # Configuração de variáveis de ambiente
└── next.config.js     # Configuração do Next.js
```

## Configuração do Projeto

### 1. Clonar o repositório
```bash
git clone https://github.com/seu-usuario/fast-hub-frontend.git
cd fast-hub-frontend
```

### 2. Instalar dependências
```bash
npm install
```

### 3. Configurar variáveis de ambiente
Crie um arquivo `.env.local` na raiz do projeto e adicione as credenciais da API:
```env
NEXT_PUBLIC_API_URL=http://localhost:5000
NEXTAUTH_SECRET=sua_chave_secreta
```

### 4. Iniciar o servidor de desenvolvimento
```bash
npm run dev
```
A aplicação estará disponível em `http://localhost:3000`

## Consumo da API

### Autenticação
- Login: `POST /usuarios/login`
- Registro: `POST /usuarios/registro`
- Perfil: `GET /usuarios/perfil`
- Atualizar perfil: `PUT /usuarios/perfil`

### Eventos
- Listar eventos: `GET /eventos`
- Detalhes do evento: `GET /eventos/:id`

### Reservas
- Criar reserva: `POST /reservas`
- Listar reservas: `GET /reservas`
- Cancelar reserva: `DELETE /reservas/:id`

## Testes

Para garantir a qualidade do código, utilizamos **Jest** e **Testing Library**:
```bash
npm run test
```

## Deploy

O projeto pode ser implantado em plataformas como **Vercel**:

1. Autentique-se na [Vercel](https://vercel.com/)
2. Conecte o repositório do GitHub
3. Configure as variáveis de ambiente na interface da Vercel
4. Clique em **Deploy**

O projeto estará disponível em `https://seu-projeto.vercel.app`

---

Essa documentação garante uma estrutura clara para a equipe desenvolver e manter o projeto de forma eficiente.

