# Deploy · ERMOS Catálogo Arara

Protótipo: GitHub → **Cloudflare Pages** (grátis, sem crédito de build).
Quando vender: GitHub → **Netlify** → Cloudflare DNS. O `netlify.toml` já está pronto.

Repositório: https://github.com/arthurxavierz/ermos-arara
Domínio: `ermos.achillesmedia.com.br`

## Cloudflare Pages
1. Workers & Pages → Create → Pages → Connect to Git → `ermos-arara`.
2. Framework preset **None**, build command vazio, output **`dist`**.
3. Project name `ermos-arara` (fica `ermos-arara.pages.dev`).
4. Custom domains → `ermos.achillesmedia.com.br`. O CNAME é criado sozinho e o proxy laranja pode ficar ligado.

Cada push na `main` publica sozinho.

## Trocar uma foto
Arquivos em `assets/` têm cache de 1 ano. Para trocar uma foto, salve com outro nome e atualize o `data.js`.
