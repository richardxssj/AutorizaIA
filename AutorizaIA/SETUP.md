# Como executar o AutorizaIA

## 1. Pré-requisitos

- conta/instância do n8n;
- credencial de IA compatível com os nós do chatbot (no projeto original foi utilizado Groq);
- Google Sheets;
- Google Drive para os comprovantes opcionais.

## 2. Criar a planilha

Crie uma planilha com duas abas.

### `Página1`

Use os cabeçalhos descritos em `data/README.md`.

### `Solicitações`

Use os cabeçalhos descritos em `data/README.md`.

## 3. Importar os workflows

Importe os JSONs de:

- `workflows/chatbot/`
- `workflows/site/`

Os JSONs públicos foram sanitizados. Após importar:

1. reconecte as credenciais do Groq/IA;
2. reconecte o Google Sheets;
3. selecione a sua planilha em todos os nós do Sheets;
4. reconecte o Google Drive;
5. selecione a pasta de comprovantes no workflow `02-Solicitacoes-Familia`;
6. publique/ative os webhooks.

Os placeholders abaixo aparecem propositalmente no repositório público:

```text
SEU_GOOGLE_SHEET_ID
SEU_GOOGLE_DRIVE_FOLDER_ID
SEU_SUBDOMINIO
```

## 4. Configurar o frontend

Abra `frontend/index.html` e `frontend/familia.html` e substitua:

```text
https://SEU_SUBDOMINIO.app.n8n.cloud
```

pelo endereço da sua instância.

## 5. Testar

Use `examples/prompts-teste.txt` para validar o chatbot.

Teste também:

- registro de autorização pelo painel;
- solicitação da família com e sem comprovante;
- aprovação e recusa;
- dashboard;
- histórico;
- saídas de hoje.

## Observação

Este é um protótipo acadêmico. Para produção, adicione autenticação, autorização por perfil, políticas de privacidade, proteção dos webhooks e controles de acesso aos arquivos do Drive.
