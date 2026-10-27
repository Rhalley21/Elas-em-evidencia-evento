# Elas em Evidência — página do evento

Página única (HTML puro, sem instalação) do evento **Elas em Evidência**, 5 de dezembro de 2026.

## Arquivos
- `index.html`: a página completa (textos, estilo e logo já estão dentro do arquivo)
- `capa.jpg`: imagem que aparece quando o link é compartilhado (WhatsApp, Instagram etc.)
- `.nojekyll`: arquivo vazio que garante que o GitHub Pages publique tudo sem alterações

## Publicar no GitHub Pages
1. No GitHub, clique em **New repository**. Dê um nome (ex.: `elas-em-evidencia`) e deixe como **Public**.
2. Clique em **uploading an existing file** e envie os 4 itens desta pasta: `index.html`, `capa.jpg`, `.nojekyll` e `README.md`. Confirme com **Commit changes**.
3. Vá em **Settings > Pages**. Em **Build and deployment**, escolha **Deploy from a branch**, branch **main** e pasta **/(root)**, e clique em **Save**.
4. Em 1 a 2 minutos o endereço aparece nessa mesma tela, no formato `https://SEU-USUARIO.github.io/NOME-DO-REPOSITORIO/`.

## Ajustes depois de publicar
Abra `index.html` no GitHub (ícone de lápis para editar) e troque:

1. **Prévia do link** (no começo do arquivo): substitua `SEU-USUARIO` e `NOME-DO-REPOSITORIO` pelos seus, nas linhas `og:image` e `og:url`.
2. **Link de pagamento** (perto do fim do arquivo): procure `const TICKET_URL = "";` e cole o link entre as aspas. Enquanto estiver vazio, os botões mostram "Ingressos em breve".
3. **Local do evento:** procure por "Será divulgado em breve" e troque pelo endereço quando estiver confirmado.

Depois de editar, clique em **Commit changes**. A página atualiza sozinha em cerca de 1 minuto.

## Observações
- O WhatsApp guarda a prévia do link por um tempo. Se mudar a imagem de capa, teste o link em uma conversa nova ou aguarde.
- A página de **entrada** (conferência dos QR Codes no evento) não fica no GitHub. Veja o documento de explicação.
