# ERMOS · Catálogo Arara

Catálogo interativo feito pela **Achilles Media** para a ERMOS: a coleção pendurada numa arara de verdade, peça por peça, com pedido direto pelo WhatsApp.

No ar: **https://ermos.achillesmedia.com.br**

## O que tem
- **Arara interativa**: arraste, role ou use as setas. As peças balançam no cabide e se abrem quando o mouse passa.
- **Peça em 3D**: um clique traz a camiseta de frente, e arrastando ela gira para mostrar estampa e outro lado.
- **Tamanhos, ficha técnica e fotos "na rua"** de cada peça.
- **Sacola com "Compre 3, Pague 2"** calculado sozinho, fechando o pedido inteiro numa mensagem de WhatsApp.
- **Link por peça** (`/#p=rule-2`) para mandar no Direct ou no Status.
- **Painel da loja** (`/#admin`): cadastrar, editar, ordenar e esgotar peças. A foto da camiseta tirada em fundo liso tem o fundo removido sozinho.
- **Sua marca aqui**: o botão no canto (ou o clique no logo) mostra o catálogo com o nome, logo, cor, promoção e WhatsApp de qualquer loja, sem enviar nada para servidor.

## Estrutura
```
dist/
  index.html      site completo (HTML, CSS e JS)
  data.js         as peças (nome, preço, coleção, fotos, tamanhos)
  assets/tees/    <peça>-a.webp estampa, -b.webp outro lado, -l1/-l2 fotos na rua
  _headers        cache e segurança (Cloudflare Pages e Netlify)
netlify.toml      para quando o site for para o Netlify
```

Sem build: o que está em `dist/` é o que vai para o ar.

## Rodar local
```
python -m http.server 5251 --directory dist
```
Abra http://localhost:5251

## Protótipo x versão final
Hoje o painel salva no navegador de quem usa (demonstração). Na versão contratada os dados vão para um banco na nuvem com login do lojista, e as fotos para armazenamento próprio.

---
Achilles Media · achillesmedia.com.br
