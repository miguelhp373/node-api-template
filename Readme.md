# Node.js API's - Template

 ## Configuração do Projeto
 ```powershell
    npm init -y
 ```

&nbsp;

 ## Instalar Express.js
 ```powershell
    npm install express
 ```

&nbsp;

## Start Server
```powershell
npm run start
```


## Requisições da API

### 1. **GET /api/items**
Retorna uma lista de itens.

**Exemplo de Requisição:**
```http
GET /api/tarefas HTTP/1.1
Host: localhost:3000
```

**Exemplo de Resposta:**
```json
[
   {
    "id": 1,
    "descricao": "Estudar Node.js e Express.js"
    },
    {
    "id": 2,
    "descricao": "Estudar Node.js e Express.js"
    },
    {
    "id": 3,
    "descricao": "Estudar Node.js e Express.js"
    }
]
```

---

### 2. **POST /api/items**
Cria um novo item.

**Exemplo de Requisição:**
```http
POST /api/tarefas HTTP/1.1
Host: localhost:3000
Content-Type: application/json

{
    "name": "Novo Item",
    "description": "Descrição do novo item"
}
```

**Exemplo de Resposta:**
```json
{
    "id": 3,
    "name": "Novo Item",
    "description": "Descrição do novo item"
}
```

---

### 3. **PUT /api/items/:id**
Atualiza um item existente.

**Exemplo de Requisição:**
```http
PUT /api/items/1 HTTP/1.1
Host: localhost:3000
Content-Type: application/json

{
    "name": "Item Atualizado",
    "description": "Descrição atualizada"
}
```

**Exemplo de Resposta:**
```json
{
    "id": 1,
    "name": "Item Atualizado",
    "description": "Descrição atualizada"
}
```

---

### 4. **DELETE /api/items/:id**
Remove um item existente.

**Exemplo de Requisição:**
```http
DELETE /api/items/1 HTTP/1.1
Host: localhost:3000
```

**Exemplo de Resposta:**
```json
{
    "message": "Item removido com sucesso"
}
```