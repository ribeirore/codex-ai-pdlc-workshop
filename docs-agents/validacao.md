# Execução e validação

Leia ao preparar o ambiente, rodar a aplicação ou verificar mudanças.

Use Node.js 24 (`>=24 <25`). Execute os comandos na raiz do projeto; [package.json](../package.json) é a fonte dos scripts disponíveis.

| Comando | Uso |
| --- | --- |
| `npm ci` | Instalar as versões do lockfile |
| `npm run doctor` | Conferir os pré-requisitos locais |
| `npm run dev` | Abrir o servidor local em `http://127.0.0.1:3000` |
| `npm run validate` | Verificar tipos, lint, testes e build |
| `npm run test:e2e` | Verificar fluxos no Chromium com Playwright |

## Verificação de mudanças

- Para mudanças de código, execute `npm run validate`.
- Após mudanças de interface ou fluxo, execute também `npm run test:e2e` quando Chromium estiver disponível.
- Pare o servidor de desenvolvimento antes da validação completa e dos testes de navegador. O E2E inicia seu próprio servidor na porta 3100.
- Testes de regras e API usam dados temporários; os de navegador usam `.local/e2e/`. Preserve essa separação dos dados do participante.
- Em mudanças somente de documentação, confira os links locais, a coerência das instruções e o diff; não é necessário executar o build.
- Relate apenas verificações realmente executadas. Se algo não puder ser verificado, indique a limitação.

Consulte [docs/preparation.md](../docs/preparation.md) para instalação do Chromium e solução de problemas. Não restaure dados como etapa rotineira de validação: `npm run data:reset` altera os dados de trabalho e deve corresponder a uma solicitação de restauração.
