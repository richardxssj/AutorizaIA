# Segurança e privacidade

Este repositório é uma versão pública sanitizada do AutorizaIA.

## O que foi removido

- IDs reais de planilhas e pastas do Google Drive;
- referências de credenciais do n8n;
- identificadores da instância n8n;
- URL real da instância n8n;
- planilha original com dados de desenvolvimento;
- comprovantes originais/de teste;
- arquivos de mídia grandes.

## Antes de publicar uma implantação real

- proteja os webhooks contra chamadas não autorizadas;
- não exponha dados de estudantes/responsáveis em repositórios públicos;
- configure permissões adequadas no Google Drive e Sheets;
- não inclua tokens, chaves de API ou arquivos de credenciais no Git;
- avalie autenticação e controle de acesso por perfil;
- revise o uso de serviços externos para geração de QR Code caso contenha dados pessoais.

Se um segredo for publicado por engano, considere-o comprometido e faça a rotação/revogação imediatamente.
