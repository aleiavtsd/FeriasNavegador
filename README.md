# Passagem de Carteira

Ferramenta para passagem de carteira nas férias dos navegadores. Site estático: um único `index.html`, sem build e sem dependências.

## Subir na Vercel

**Opção 1: arrastar a pasta**
1. Crie uma pasta com o `index.html`.
2. No painel da Vercel: Add New → Project, ou rode `npx vercel` dentro da pasta.
3. Framework Preset: **Other**. Build Command e Output Directory ficam vazios.

**Opção 2: via GitHub**
1. Crie um repositório com o `index.html` na raiz.
2. Importe o repositório na Vercel (Framework: Other) e faça o deploy.

## Como os dados são salvos

Tudo fica no `localStorage` do navegador de quem usa. Isso significa:

- Nada é enviado para servidor nenhum.
- O navegador e a volante **não veem a mesma cópia** automaticamente. Use **Exportar JSON** (navegador) e **Importar JSON** (volante) para passar a ficha, e o mesmo caminho de volta com o Diário preenchido.
- Limpar os dados do site apaga as passagens. Exporte antes.

Se quiser compartilhamento em tempo real entre navegador e volante, o próximo passo é ligar um banco (Vercel KV, Supabase ou similar) com login.

## O que tem

Visão geral com alertas e linha do tempo (D-15 a D+1, datas calculadas pelas férias) · Mapa da carteira com semáforo · Fichas geradas automaticamente (completa para vermelho, curta para amarelo) · Black, desafios e entregáveis · Detratores (com opção "nenhum") · Agenda com cobertura · Mensagens prontas com nome preenchido · Checklists dos três momentos · Diário com filtro "precisa de ação" · Impressão/PDF.
