# Nexo — instruções para agentes

Portal local de demandas internas para um workshop, com Next.js, React, TypeScript e persistência JSON. Preserve a stack existente deste projeto.

## Regras essenciais

- Mantenha a comunicação e a interface em português (pt-BR), usando o glossário em [CONTEXT.md](CONTEXT.md).
- Preserve alterações existentes e dados do participante. Mutações passam pela transação do armazenamento; regras são validadas no backend.
- Não acrescente banco de dados, Docker, autenticação real ou serviços externos ao exercício.
- Antes de implementar a nova história, confirme o PRD e a especificação da branch de trabalho.
- Informe o que mudou, quais verificações executou e o que ficou pendente.

## Consulte conforme a tarefa

Use Progressive Disclosure: comece por este arquivo e leia apenas os guias pertinentes à tarefa, antes de agir. Abra as referências adicionais quando forem necessárias; não carregue toda a documentação por padrão.

| Quando precisar | Leia |
| --- | --- |
| Entender o produto, o vocabulário e o escopo | [Contexto do projeto](docs-agents/contexto.md) |
| Alterar código, API, regras ou persistência | [Arquitetura e dados](docs-agents/arquitetura.md) |
| Preparar o ambiente, executar ou validar mudanças | [Execução e validação](docs-agents/validacao.md) |
| Implementar a aprovação de orçamento ou retomar o exercício | [Evolução do workshop](docs-agents/workshop.md) |

Ao atualizar estas instruções, mantenha aqui apenas regras transversais e o índice. Coloque detalhes no guia correspondente e prefira links às fontes existentes a cópias de seu conteúdo.

Este arquivo orienta o trabalho; não substitui as permissões configuradas no agente.

<!-- BEGIN:nextjs-agent-rules -->

# This is NOT the Next.js you know

This version has breaking changes — APIs, conventions, and file structure may all differ from your training data. Read the relevant guide in `node_modules/next/dist/docs/` (resolved from this file's directory; in monorepos the `next` package may not be visible from the repo root) before writing any code. Heed deprecation notices.

This block is written and re-added by `next dev` — verify at `node_modules/next/dist/server/lib/generate-agent-files.js`. Removing it from a diff only re-creates the uncommitted change; committing it with your work keeps the tree clean.

<!-- END:nextjs-agent-rules -->
