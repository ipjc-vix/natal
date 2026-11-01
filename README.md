# Santo pra Sempre · Cantata de Natal 2026 · IPJC

Página publicada em **https://natal.ipjc.org.br** pelo GitHub Pages.

Tudo o que estiver na pasta `site/` vai para o ar sozinho, 1 ou 2 minutos depois de salvo no branch `main`.
Para acompanhar a publicação, abra a aba **Actions** do repositório: verde = no ar, vermelho = deu erro (clique para ver o motivo).

## Como atualizar

**Pelo navegador (sem instalar nada):**
1. Abra a pasta `site/` aqui no GitHub.
2. Para editar a página: clique em `index.html` → ícone do lápis → faça a mudança → **Commit changes**.
3. Para enviar fotos: entre em `site/fotos/` → **Add file → Upload files** → arraste as fotos → **Commit changes**.

Na página, uma foto entra assim: `<img src="fotos/ensaio-01.jpg" alt="Ensaio do coral">`

## Fotos e vídeos

- **Fotos:** JPG com até 1600 px de largura e uns 500 KB cada (dá para reduzir em https://squoosh.app). Nomes sem espaço nem acento: `ensaio-01.jpg`, `apresentacao-jc-03.jpg`.
- **Vídeos: não suba vídeo no repositório.** Publique no YouTube da igreja (https://www.youtube.com/ipbjardimcamburi) e coloque na página só o vídeo incorporado:
  `<iframe src="https://www.youtube.com/embed/CODIGO_DO_VIDEO" allowfullscreen></iframe>`

## Prévia do link (WhatsApp, Instagram)

A imagem que aparece ao compartilhar o link é `site/compartilhar.jpg` (1200×630 px). Se trocar a imagem, mantenha o mesmo nome.

## Configuração (feita uma vez)

- **Publicação:** GitHub Pages, pelo arquivo `.github/workflows/pages.yml`.
  Em **Settings → Pages**: Source = *GitHub Actions*, Custom domain = `natal.ipjc.org.br`, *Enforce HTTPS* marcado.
  O arquivo `site/CNAME` guarda o domínio; não apague.
- **DNS:** gerenciado no **Wix** (Domínios → ipjc.org.br → Gerenciar registros DNS).
  Registro **CNAME** `natal` → `ipjc-vix.github.io`.
- **HTTPS:** automático pelo GitHub Pages.
- **Reserva na Locaweb:** a hospedagem ipjc.org.br (pasta `natal`) tem uma cópia da página.
  Para atualizá-la, rode manualmente **Actions → Publicar na Locaweb (reserva)**. Os dados de acesso ficam nos
  secrets `FTP_HOST`, `FTP_USER` e `FTP_PASS` (Settings → Secrets and variables → Actions).
  Para voltar a servir pela Locaweb, troque no Wix o CNAME `natal` por um registro A apontando para o IP da hospedagem.

## Divulgação

A pasta `divulgacao/` tem os QR Codes, em preto e em vinho (#7A1F1F), em **SVG** (vetor, para a gráfica e o Canva) e **PNG** (2220×2220 px):

| Arquivo | Endereço | Uso |
|---|---|---|
| `qrcode-cartaz-*` | http://natal.ipjc.org.br/?ref=cartaz | cartazes |
| `qrcode-panfleto-*` | http://natal.ipjc.org.br/?ref=panfleto | panfletos |
| `qrcode-natal-*` | http://natal.ipjc.org.br | uso geral (telão, slides, redes) |

O `?ref=` não muda a página; serve para o contador de visitas separar os acessos de cada material.
Para um material novo, gere outro QR com outro `ref` (ex.: `?ref=boletim`).

Esta pasta não é publicada no site. Impressão: no mínimo 2,5 cm de lado no panfleto, 5 cm ou mais no cartaz, sempre com a margem branca em volta. Os QR Codes usam `http://`; o GitHub Pages leva automaticamente para `https://`. Teste com o celular antes de mandar imprimir.

O endereço antigo `natal.ipjc.org.br/natal/` também leva à página (arquivo `site/natal/index.html`).
