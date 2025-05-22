
# Gamefica - Backend API

Este repositório contém o backend simples em Node.js para a aplicação **Gamefica** — o primeiro site de gamificação para vendas, transformando funis de vendas em jogos.

---

## Tecnologias

- Node.js
- Express
- SQLite (banco leve, arquivo `gamefica.db` local)
- CORS para comunicação com o frontend

---

## Como rodar localmente

### 1. Clone o repositório

```bash
git clone https://github.com/seu-usuario/gamefica-backend.git
cd gamefica-backend
```

### 2. Instale as dependências

```bash
npm install
```

### 3. Rode o servidor

```bash
node server.js
```

O backend ficará disponível em: `http://localhost:4000`

---

## Endpoints disponíveis

### POST `/api/login`

Autentica usuário.

**Request body JSON:**

```json
{
  "email": "usuario@gamefica.com",
  "senha": "123456789"
}
```

**Response:**

```json
{
  "userId": 1,
  "nome": "Usuário Teste"
}
```

---

### GET `/api/dashboard/:userId`

Retorna dados do dashboard para o usuário.

---

### POST `/api/funil`

Cria um novo funil para o usuário.

**Request body JSON:**

```json
{
  "userId": 1,
  "nome": "Jornada do Herói",
  "etapas": ["Captação", "Nutrição", "Conversão", "Pós-venda"]
}
```

---

## Usuário padrão para teste

- Email: `usuario@gamefica.com`  
- Senha: `123456789`

---

## Detalhes da implementação

- Banco SQLite salva em arquivo `gamefica.db`.
- Criação automática das tabelas.
- Usuário padrão criado se não existir.
- Funis salvos com etapas em JSON.

---

## Próximos passos

- Integrar com frontend React.
- Adicionar autenticação com JWT.
- Persistir dados do funil dinamicamente.

---

## Autor

Criado por [Seu Nome]

---

## Licença

MIT License
