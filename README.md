# Template de Projeto — Desenvolvimento Assistido por IA

Template base para projetos de desenvolvimento de software com um ciclo de vida estruturado (SDLC), executado por agentes de IA com skills especializados.

## Conteúdo do Repositório

```
.agents/skills/       ← 19 skills de engenharia (SDLC, documentação, regras)
.github/instructions/ ← Normas de código e convenções (geral + Python)
.github/config/       ← Configuração de localização (pt-PT)
docs/
  APIs/               ← Especificações OpenAPI (geradas automaticamente)
  Architecture/       ← Documentação de arquitetura (gerada automaticamente)
  SDLC/
    requirements/     ← Requisitos do projeto (um ficheiro por requisito)
    artifacts/        ← Artefactos gerados por requisito (plano, design, tarefas, testes)
```

### Skills Disponíveis

| Grupo | Skills |
|---|---|
| Agile | `agile-refinement`, `agile-build`, `agile-review` |
| SDLC | `sdlc-plan`, `sdlc-design`, `sdlc-tasks`, `sdlc-implement`, `sdlc-test`, `sdlc-code-review`, `sdlc-shipping-and-launch` |
| Documentação | `doc-api`, `doc-create-readme-file`, `doc-onboarding`, `doc-solution-architecture` |
| Regras | `rules-api-and-interface-design`, `rules-frontend-ui-engineering`, `rules-debugging-and-error-recovery`, `rules-browser-testing-with-devtools`, `rules-generate-unit-tests` |

### Convenções

- **Idioma:** Português de Portugal (pt-PT) em todos os artefactos
- **Codificação:** UTF-8 sem BOM
- **Datas:** DD/MM/YYYY
- **Python:** PEP 8, Black (88 caracteres), type hints, snake_case
- **Geral:** Nomes descritivos, tratamento de erros, sem credenciais no código, testes unitários obrigatórios

## Processo de Implementação de Issues

O ciclo de desenvolvimento segue três macro-fases sequenciais, cada uma com um skill dedicado:

```
agile-refinement  →  agile-build  →  agile-review
```

### Fase 1 — Refinamento (`agile-refinement`)

> Decompor a issue em plano, design e tarefas.

1. **Criar o requisito** — Copiar `docs/SDLC/requirements/_template.md` para `docs/SDLC/requirements/REQ-XXX.md` e preencher:
   - Descrição, Valor de Negócio, Requisitos Funcionais, Critérios de Aceitação e Restrições
   - Definir `status: draft`

2. **Planear** (`sdlc-plan`) — Gera o plano de implementação com visão geral, arquitetura, componentes, fases e riscos.
   - Saída: `docs/SDLC/artifacts/REQ-XXX/plan.md`
   - Estado do requisito: `draft` → **`planned`**

3. **Desenhar** (`sdlc-design`) — Gera o design técnico com estrutura de módulos, esquema de base de dados, APIs e interações.
   - Saída: `docs/SDLC/artifacts/REQ-XXX/design.md`
   - Estado: **`designed`**

4. **Criar tarefas** (`sdlc-tasks`) — Decompõe o trabalho em tarefas atómicas e identifica as que são testáveis unitariamente.
   - Saída: `docs/SDLC/artifacts/REQ-XXX/tasks.md`
   - Estado: **`tasked`**

### Fase 2 — Construção (`agile-build`)

> Implementar, testar e rever o código.

5. **Implementar** (`sdlc-implement`) — Gera o código em `/src`, seguindo as regras de design de APIs e frontend.
   - Estado: **`implemented`**

6. **Testar** (`sdlc-test`) — Gera e executa testes unitários em `/tests`. Os resultados são guardados em `docs/SDLC/artifacts/REQ-XXX/tests-result.md`.
   - Estado: **`tested`** (apenas se todos os testes passarem)

7. **Rever código** (`sdlc-code-review`) — Revisão automática de segurança, performance, qualidade, arquitetura e testes.
   - Estado: **`reviewed`**

### Fase 3 — Documentação (`agile-review`)

> Documentar a solução, APIs e onboarding.

8. **Arquitetura da solução** (`doc-solution-architecture`) → `docs/Architecture/solution-architecture.md`
9. **Especificação da API** (`doc-api`) → `docs/APIs/<titulo>.md` (OpenAPI 3.0.3)
10. **Guia de onboarding** (`doc-onboarding`) → `docs/Architecture/onboarding.md`
11. **Atualizar README** (`doc-create-readme-file`) → `README.md`
12. Estado final: **`documented`**

### Ciclo de Vida do Requisito

```
draft → planned → designed → tasked → implemented → tested → reviewed → documented
```

Cada transição de estado é feita automaticamente pelo skill correspondente, assegurando rastreabilidade completa.

### Resumo Visual

```
┌─────────────────────────────────────────────────────────────────┐
│                      agile-refinement                           │
│  ┌──────────┐   ┌──────────┐   ┌──────────┐   ┌──────────┐    │
│  │  Criar   │ → │  Planear │ → │ Desenhar │ → │  Tarefas │    │
│  │ Requisito│   │(sdlc-plan│   │(sdlc-    │   │(sdlc-    │    │
│  │          │   │)         │   │design)   │   │tasks)    │    │
│  └──────────┘   └──────────┘   └──────────┘   └──────────┘    │
└─────────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────────┐
│                        agile-build                              │
│  ┌────────────┐   ┌──────────┐   ┌─────────────┐               │
│  │ Implementar│ → │  Testar  │ → │ Rever Código│               │
│  │(sdlc-      │   │(sdlc-    │   │(sdlc-code-  │               │
│  │implement)  │   │test)     │   │review)      │               │
│  └────────────┘   └──────────┘   └─────────────┘               │
└─────────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────────┐
│                       agile-review                              │
│  ┌────────────┐   ┌─────────┐   ┌───────────┐   ┌──────────┐  │
│  │ Arquitetura│ → │   API   │ → │ Onboarding│ → │  README  │  │
│  │  Solução   │   │  Docs   │   │   Guide   │   │          │  │
│  └────────────┘   └─────────┘   └───────────┘   └──────────┘  │
└─────────────────────────────────────────────────────────────────┘
```

## Prompts para Developers

Para facilitar o acesso ao ciclo SDLC diretamente no Copilot Chat, estão disponíveis três prompts reutilizáveis em `.github/prompts/`:

| Prompt | Descrição | Skill invocado |
|---|---|---|
| `refinement` | Inicia o refinamento de um requisito | `agile-refinement` |
| `build` | Executa a fase de construção | `agile-build` |
| `review` | Executa a fase de documentação | `agile-review` |

Para utilizar, abrir o Copilot Chat, selecionar o prompt pretendido e indicar o `REQ_ID` quando solicitado. Os prompts delegam integralmente para os skills correspondentes, garantindo o mesmo comportamento que invocar o skill diretamente.

## Como Começar

1. Clonar este repositório como base para um novo projeto
2. Criar o ficheiro de requisito a partir do template:
   ```bash
   cp docs/SDLC/requirements/_template.md docs/SDLC/requirements/REQ-001.md
   ```
3. Preencher o requisito com a descrição da issue
4. Usar o prompt `refinement` no Copilot Chat (ou invocar o skill `agile-refinement` diretamente) para iniciar o ciclo

## Quem Mantém

Este template é mantido pela equipa de desenvolvimento. Contribuições e melhorias são bem-vindas através de pull requests.
