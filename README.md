# Lazzarella Ristorante

Website institucional em Next.js 16, React 19, TypeScript, Tailwind CSS 4 e Motion. Abertura com a foto real do sal?o, se??es editoriais e card?pios oficiais.

## Executar

```powershell
npm.cmd install
npm.cmd run dev
```

Abra http://localhost:3000. Para visualizar a vers?o de produ??o:

```powershell
npm.cmd run build
npm.cmd start
```

O build est?tico ? gerado em `out/`. O comando `start` usa Python para servi-lo na porta 3000. Use apenas um servidor por porta e encerre com Ctrl+C.

## Organiza??o

- `app/`: p?gina, metadados e estilos responsivos.
- `components/`: navega??o acess?vel, links e anima??es.
- `lib/content.ts`: destinos externos e categorias oficiais.
- `public/`: imagens e fontes locais com suas licen?as.
- `Imagens lazzarella/`: acervo original preservado.
- `~/.codex/skills/frontend-design/`: refer?ncia de design fornecida pelo usu?rio.
- `docs/`: invent?rio, curadoria, pesquisa e relat?rios de valida??o.
- `scripts/`: invent?rio e verifica??es reutiliz?veis.

Os quinze acessos por categoria abrem o card?pio completo do DGuests, conforme indicado na interface. N?o foram identificados links p?blicos individuais de categorias. Reservas s?o encaminhadas ao DGuests; contato ao WhatsApp e Instagram.

## Verificar

```powershell
npm.cmd run typecheck
npm.cmd run build
python scripts/validate.py
python scripts/check-links.py
```

Para os testes de navegador, sirva a exporta??o em outro terminal:

```powershell
python -m http.server 3010 --bind 127.0.0.1 --directory out
```

Depois execute `node scripts/qa.cjs`. O teste usa Microsoft Edge local via Playwright, percorre cinco larguras e verifica carregamento, overflow, menu mobile e categorias. `qa-interactions.cjs` verifica teclado e abertura real do DGuests; `qa-salon.cjs` captura a abertura. Relat?rios e capturas s?o gerados em `docs/qa/`.

A ?ltima revis?o visual e funcional passou em desktop e mobile. Capturas antigas, arquivos brutos de pesquisa, backups intermedi?rios e scripts de edi??o descart?veis foram removidos. Os testes podem recriar as capturas quando necess?rio.

## Publica??o

O projeto permanece local. `.openai/hosting.json` preserva o identificador do registro privado criado anteriormente, ainda n?o publicado. O dom?nio definitivo n?o foi informado; canonical e sitemap devem ser configurados quando ele for definido.
