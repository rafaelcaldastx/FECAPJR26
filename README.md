<p float="left">
  <img src="https://github.com/user-attachments/assets/9bd3241b-89a8-48cf-98f4-6454f5856bf9" width="150" align="left"/>
  <img loading="lazy" src="https://img.shields.io/badge/Processo_Seletivo-2026-24?style=for-the-badge&color=GREEN" align="right"/>
</p>
<br/>
<p>
  <h1 align="center">Processo seletivo - Programador - FECAP 2026 - Etapa Prática</h1>
</p>

<p>
  Prezado candidato, este teste tem duas partes: teórica e prática.<br/><br/>
  É permitido consultar internet, documentação e fóruns livremente. O uso de IA é permitido desde que você entenda e seja capaz de explicar cada linha do código entregue. Código copiado sem compreensão pode levar à desclassificação na entrevista técnica.
</p>

<p>
  Não esperamos perfeição. Queremos entender seu raciocínio, sua organização e como você documenta decisões.<br/>
  Saber seus limites também é importante — conte o que você domina e o que ainda está aprendendo.
</p>

<p>
  Você deve criar um repositório com a estrutura abaixo e responder a parte teórica no README.md, junto com o código da parte prática.
</p>

<p>
  <b>Frontend e backend são projetos separados</b> (pastas distintas) e se comunicam via API HTTP.
</p>

<p>
  ➡️ O código deve ser entregue em um repositório Git público (GitHub, GitLab ou Bitbucket)<br/>
  ➡️ Inclua um README.md com instruções claras para configurar e executar o projeto<br/>
  ➡️ <b>Prazo de entrega:</b> até dia 28/06/2026
</p>

<p><b>💎 Dica!</b> Não perca tempo com estilização. Foque na funcionalidade.</p>
<p><b>💎 Dica!</b> Simplicidade funcional > conceitos complexos e código inchado.</p>
<p><b>💎 Dica!</b> Código comentado explicando decisões técnicas vale mais que código "perfeito".</p>

---

## Stack Obrigatória

| Camada | Tecnologia |
|---|---|
| **Backend** | TypeScript + Express |
| **Frontend** | TypeScript + React |
| **Comunicação** | API REST (JSON) |
| **Banco de dados** | Não é obrigatório. Use array em memória. Vale ponto extra se usar DB (relacional). |

---

## 1. Parte Teórica

Responda de forma breve (máx. 5 linhas cada), com suas próprias palavras.

📄 1. Explique a diferença entre tipos explícitos e inferência de tipos no TypeScript. Dê um exemplo de cada.

📄 2. O que é `async/await` e como ele facilita o trabalho com código assíncrono?

📄 3. Explique o fluxo de uma requisição HTTP do frontend ao backend e de volta ao frontend.

📄 4. Qual a diferença entre os métodos HTTP `GET` e `POST`? Em qual situação você usaria cada um?

📄 5. Dado o cenário: o frontend faz uma requisição ao backend e a resposta demora mais de 10 segundos. Como você trataria isso no código para informar o usuário?

---

## 2. Parte Prática

Desenvolver uma página de **gerenciamento de alunos** com as seguintes funcionalidades:

- **Listagem:** exibir todos os alunos cadastrados em uma tabela
- **Cadastro:** formulário para cadastrar novo aluno (nome, idade, curso)
- **Edição:** permitir editar os dados de um aluno já cadastrado
- **Exclusão:** permitir excluir um aluno cadastrado

### 2.1 Estrutura esperada do projeto

```
alunos-crud/
├── frontend/           # React + Vite + TypeScript
│   ├── src/
│   │   ├── components/ # Componentes da interface
│   │   ├── services/   # Chamadas HTTP para o backend
│   │   ├── types/      # Interfaces e tipos
│   │   ├── App.tsx
│   │   └── main.tsx
│   ├── package.json
│   ├── tsconfig.json
│   └── vite.config.ts
│
├── backend/            # Express + TypeScript
│   ├── src/
│   │   ├── routes/     # Definição de rotas
│   │   ├── index.ts    # Entry point do servidor
│   │   └── ...
│   ├── package.json
│   └── tsconfig.json
│
└── README.md           # Respostas teóricas + instruções
```

> Os campos `components/`, `services/`, `routes/` e `types/` são sugestões. Você pode organizar como preferir — o importante é que esteja separado por responsabilidade e claro.

### 2.2 Especificações da API

O backend deve expor os seguintes endpoints:

| Método | Rota | Descrição |
|---|---|---|
| `GET` | `/api/alunos` | Retorna a lista de alunos |
| `GET` | `/api/alunos/:id` | Retorna um aluno pelo ID |
| `POST` | `/api/alunos` | Cria um novo aluno |
| `PUT` | `/api/alunos/:id` | Atualiza os dados de um aluno |
| `DELETE` | `/api/alunos/:id` | Remove um aluno |

Modelo do aluno:

```typescript
{
  id: number;
  nome: string;
  idade: number;
  curso: string;
}
```

### 2.3 Regras de negócio

- O `id` deve ser gerado automaticamente pelo backend
- Nenhum campo pode ficar vazio no cadastro (valide no frontend e no backend)
- A idade mínima é 16 anos (valide no backend)

### 2.4 Frontend

- Deve consumir a API do backend 
- A tabela de listagem deve mostrar todos os alunos cadastrados
- O formulário de cadastro/edição pode ser na mesma página ou em modal — como preferir
- Trate os estados: carregando, erro e vazio (nenhum aluno cadastrado)
- Ao excluir, peça confirmação antes de enviar a requisição

---

## Critérios Avaliativos

| Critério | Peso |
|---|---|
| Organização do código e separação de responsabilidades | Alto |
| Funcionalidade completa (CRUD operacional) | Alto |
| Clareza nas respostas teóricas | Médio |
| Uso adequado do Git (commits descritivos, histórico limpo) | Médio |
| Tratamento de erros e estados (loading, erro, vazio) | Médio |
| README com instruções claras de execução | Baixo |
| Diferenciais (SQLite, testes, validações extras) | Bônus |

---

## Como executar (instruções que esperamos no README)

O candidato deve documentar no README.md algo como:

```bash
# Terminal 1 - Backend
cd backend
npm install
npm run dev

# Terminal 2 - Frontend
cd frontend
npm install
npm run dev
```

E informar as portas: backend em `http://localhost:3001`, frontend em `http://localhost:5173`, com proxy configurado para `/api`.

---

<b>Prazo: 28/06/2026 </b>

<h3>Boa sorte! 🚀</h3>
