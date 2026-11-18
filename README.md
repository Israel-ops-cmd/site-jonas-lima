# Site Jonas Lima | Espaço JL Terapias Manuais

Site estático, sem etapa de build. HTML, CSS e JS ficam no `index.html`; GSAP 3.12.5, ScrollTrigger e Lenis 1.1.13 ficam em `/vendor` (versões fixas, servidas pelo próprio site).

## Rodar localmente

```bash
npx serve .
# ou
python3 -m http.server 8080
```

Abra http://localhost:3000 (serve) ou http://localhost:8080 (python). Abrir o arquivo direto (file://) não funciona porque os caminhos começam com `/`.

## Estrutura

- `index.html`: página única
- `img/`: fotos em .webp (800 e 1600px; recortes em 700 e 1200px)
- `vendor/`: gsap.min.js, ScrollTrigger.min.js, lenis.min.js
- `favicon.svg`, `apple-touch-icon.png`, `og-image.jpg` (1200x630, preview no WhatsApp)
- `vercel.json`: cleanUrls e cache longo para /img e /vendor

## Publicar

1. GitHub: crie o repositório `site-jonas-lima` e faça push na branch `main`.
2. Vercel: Add New > Project > importe o repositório. Framework Preset: Other. Build Command: vazio. Output Directory: `./`.
3. Cada push em `main` publica sozinho.
4. URL atual: https://site-jonas-lima.vercel.app/ (já usada no canonical, nas tags og:/twitter: e no JSON-LD). Ao ligar um domínio próprio, troque essa URL nesses três lugares.

## Trocar fotos

Substitua os arquivos em `img/` mantendo os mesmos nomes (`01-hero-700.webp`, `01-hero-1200.webp` etc.).
