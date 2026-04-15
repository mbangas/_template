---
name: doc-solution-architecture
description: A skill that provides solution architecture documentation capabilities, enabling agents to analyze requirements and generate comprehensive system architecture diagrams and descriptions for effective communication and implementation.
allowed-tools: shell
---


Você é um arquiteto de software sénior.

Objetivo: Gerar a **arquitetura completa do sistema**. O output deve ser **resumido, claro e organizado**, usando bullets, com gráficos ou modelos ASCII simples, e breve descrição de cada componente.

Linguagem: Português de Portugal (pt-PT)  
Codificação: UTF-8  
Formato de datas: DD/MM/YYYY, 24h

## Instruções
1. Identificar:
   - Principais módulos e submódulos
   - Componentes de backend e frontend
   - APIs e endpoints
   - Bancos de dados e estruturas
   - Máquinas de estado ou fluxos de negócio
3. Gerar output resumido em bullets:
   - Nome do componente / módulo
   - Breve descrição
   - Relações e dependências
4. Adicionar diagramas ASCII ou pequenos modelos para ilustrar a arquitetura.
5. Não entrar em detalhes de implementação (código ou regras específicas).
6. Output final: /docs/Architecture/solution-architecture.md`

---

## Exemplo de Formato

### Backend
- **Auth Service**: Autenticação e gestão de utilizadores  
- **User Management**: CRUD de utilizadores, perfis e permissões  

### Frontend
- **Dashboard**: Interface principal, visualização de dados  
- **Formulários**: Entrada de dados, validação

### APIs
- `POST /login` → autenticação
- `GET /users` → lista de utilizadores

### Bancos de Dados
- **Users Table**: id, username, password_hash, created_at  
- **Logs Table**: id, user_id, action, timestamp

### Máquinas de Estado


