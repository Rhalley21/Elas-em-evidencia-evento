# Elas em Evidência — site do evento

Dois endereços no mesmo repositório (HTML puro, sem instalação):

- **Página do evento** (pública): `index.html`
- **Página de entrada** (equipe, protegida por PIN): `entrada/index.html`

## Arquivos
- `index.html`: a página do evento
- `logo.jpg`: logo usada na página
- `leilane.jpg`: foto da Leilane Mendes (seção de idealizadora)
- `pix-individual.png` e `pix-grupo.png`: QR Codes do Pix (R$ 229,90 e R$ 197,50), mostrados na janela de pagamento
- `capa.jpg`: imagem da prévia do link (WhatsApp, Instagram)
- `logo-email.jpg`: logo usada no e-mail de convite (o e-mail busca a imagem neste endereço)
- `entrada/index.html` e `entrada/sw.js`: página de entrada e o arquivo que a faz abrir sem internet

## Publicar no GitHub Pages
1. No GitHub, clique em **New repository**, dê um nome (ex.: `elas-em-evidencia`) e deixe **Public**.
2. Envie **toda a pasta**, mantendo a subpasta `entrada`. Para criar a subpasta pelo site do GitHub, use **Add file > Upload files** e arraste a pasta `entrada` inteira.
3. Em **Settings > Pages**, escolha **Deploy from a branch**, branch **main** e pasta **/(root)**, e clique em **Save**.
4. Em 1 a 2 minutos o endereço aparece nessa tela.

## Ajustes depois de publicar
Para editar um arquivo no GitHub, abra-o e clique no ícone de lápis. Depois clique em **Commit changes**. A página atualiza em cerca de 1 minuto.

**Em `index.html`:**
1. **Prévia do link:** as linhas `og:image` e `og:url` já vêm com o endereço `https://rhalley21.github.io/Elas-em-evidencia-evento/`. Só mude se o repositório mudar de nome.
2. **Pagamento:** os endereços da API, dos links de cartão da InfinitePay e os códigos Pix ficam no bloco `EDITE AQUI` do final do arquivo (`API_URL`, `LINK_CARTAO`, `LINK_CARTAO_GRUPO`, `PIX_CODIGO`). Já vêm preenchidos. Se trocar um valor ou uma chave Pix, gere um novo QR Code e troque também as imagens `pix-*.png`.
3. **Local do evento:** procure "Será divulgado em breve" e troque pelo endereço quando estiver confirmado.

**Em `entrada/index.html`:**
1. Procure `const API_URL = "COLE-AQUI-O-ENDERECO-DA-IMPLANTACAO";` e cole o endereço gerado na instalação da automação (veja o LEIA-ME da pasta `automacao`).

## Observações
- Este repositório é público. **Nunca suba planilhas, listas de nomes, convites pessoais nem o arquivo `Code.gs`.**
- A página de entrada não mostra nenhum dado sem o PIN. O PIN fica só no script do Google Planilhas, não neste repositório.
- O WhatsApp guarda a prévia do link por um tempo. Se trocar a imagem de capa, teste em uma conversa nova.
