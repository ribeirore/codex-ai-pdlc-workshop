# Arquitetura e dados

Leia antes de alterar código, contratos da API, regras de negócio ou armazenamento.

## Onde trabalhar

| Caminho | Responsabilidade |
| --- | --- |
| `src/app/` | Páginas, layout, estilos e endpoints Next.js |
| `src/components/` | Interface React do quadro, formulários e detalhes |
| `src/domain/` | Tipos, validações, regras e conversão monetária |
| `src/server/` | Contrato HTTP e armazenamento JSON |
| `data/seed.json` | Exemplos versionados |
| `.local/` | Dados de trabalho do participante |
| `tests/` | Testes de regras, API, armazenamento e navegador |

Leia [docs/architecture.md](../docs/architecture.md) para contratos, concorrência e persistência. Confirme o comportamento no código da branch atual antes de alterá-lo.

## Regras de implementação

- Valide dados, permissões e transições no backend. Controles visuais não substituem essa validação.
- Faça mutações pela transação do armazenamento existente. Preserve travas, gravação atômica e proteção contra versões desatualizadas.
- Preserve dados e histórico ao introduzir campos ou mudar o esquema; defina a compatibilidade com os arquivos existentes.
- Mantenha a seed como fonte de exemplos, sem gravar nela durante o uso normal.
- Perfis e o cabeçalho `x-demo-user` são recursos de demonstração, não autenticação real.
- Não adicione banco de dados, Docker ou serviços externos ao exercício.
- Antes de escrever código Next.js, leia o guia pertinente em `node_modules/next/dist/docs/`, conforme o aviso do AGENTS.md. Se as dependências não estiverem instaladas, siga o [guia de execução](validacao.md).

Após implementar, siga as verificações do [guia de validação](validacao.md).
