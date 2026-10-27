# Elas em Evidência — site do evento

Dois endereços no mesmo repositório (HTML puro, sem instalação):

- **Página do evento** (pública): `index.html`
- **Página de entrada** (equipe, protegida por PIN): `entrada/index.html`

## Arquivos
- `index.html`: a página do evento
- `logo.jpg`: logo usada na página
- `capa.jpg`: imagem da prévia do link (WhatsApp, Instagram)
- `logo-email.jpg`: logo usada no e-mail de convite (o e-mail busca a imagem neste endereço)
- `entrada/index.html` e `entrada/sw.js`: página de entrada e o arquivo que a faz abrir sem internet

## Publicar no GitHub Pages
1. No GitHub, clique em **New repository**, dê um nome (ex.: `elas-em-evidencia`) e deixe **Public**.
2. Envie **toda a pasta**, mantendo a subpasta `entrada`. Para criar a subpasta pelo site do GitHub, use **Add file > Upload files** e arraste a pasta `entrada` inteira.
3. Em **Settings > Pages**, escolha **Deploy from a branch**, branch **main** e pasta **/(root)**, e clique em **Save**.
4. Em 1 a 2 minutos o endereço aparece nessa tela: `https://SEU-USUARIO.github.io/NOME-DO-REPOSITORIO/`.

## Ajustes depois de publicar
Para editar um arquivo no GitHub, abra-o e clique no ícone de lápis. Depois clique em **Commit changes**. A página atualiza em cerca de 1 minuto.

**Em `index.html`:**
1. **Prévia do link:** troque `SEU-USUARIO` e `NOME-DO-REPOSITORIO` nas linhas `og:image` e `og:url`.
2. **Link de pagamento:** procure `const TICKET_URL = "";` e cole o link entre as aspas. Se o ingresso de grupo tiver um link próprio, cole-o em `TICKET_URL_GRUPO` (se ficar vazio, o grupo usa o link principal). Enquanto `TICKET_URL` estiver vazio, os botões mostram "Quero ser avisada" e levam ao WhatsApp do Instituto, com uma mensagem pronta.
3. **Local do evento:** procure "Será divulgado em breve" e troque pelo endereço quando estiver confirmado.

**Em `entrada/index.html`:**
1. Procure `const API_URL = "COLE-AQUI-O-ENDERECO-DA-IMPLANTACAO";` e cole o endereço gerado na instalação da automação (veja o LEIA-ME da pasta `automacao`).

## Observações
- Este repositório é público. **Nunca suba planilhas, listas de nomes, convites pessoais nem o arquivo `Code.gs`.**
- A página de entrada não mostra nenhum dado sem o PIN. O PIN fica só no script do Google Planilhas, não neste repositório.
- O WhatsApp guarda a prévia do link por um tempo. Se trocar a imagem de capa, teste em uma conversa nova.
