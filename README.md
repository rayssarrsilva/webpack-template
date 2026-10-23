# Webpack template

**English** · [Português](#português)

The starting point I use for vanilla JavaScript projects. I set it up in July 2026, during The Odin Project, so each new project starts from the same build instead of copying configs by hand.

## What it includes

- **Webpack 5** with three config files: `webpack.common.js` (shared), `webpack.dev.js` and `webpack.prod.js`, joined with `webpack-merge`.
- **Development:** dev server with live reload, CSS injected by `style-loader`, `eval-source-map` for readable stack traces.
- **Production:** CSS extracted to its own file and minified, JavaScript minified, source maps, `dist/` cleaned on every build.
- **Assets:** images, video and fonts imported from JavaScript or CSS (`asset/resource`); fonts go to `asset/fonts/`.
- **HTML:** `src/index.html` is the template; the script and style tags are added for you.
- **Deploy:** one command publishes `dist/` to GitHub Pages.

## Use it

On GitHub, click **Use this template** → **Create a new repository**, then:

```bash
npm install
npm start          # dev server at http://localhost:8080
npm run build      # production build in dist/
npm run deploy     # build and publish dist/ to the gh-pages branch
```

Requires Node.js 22.15 or newer (webpack-dev-server 6).

## Structure

```
src/
├── index.html     HTML template
├── index.js       entry point
└── style.css      imported by index.js
webpack.common.js  entry, output, HTML plugin, assets
webpack.dev.js     dev server and CSS in the page
webpack.prod.js    CSS extracted and minified
```

## License

[MIT](./LICENSE)

---

## Português

O ponto de partida que uso em projetos de JavaScript puro. Montei em julho de 2026, durante o The Odin Project, para que cada projeto novo comece com o mesmo build, sem copiar configuração à mão.

**O que tem:** Webpack 5 com configuração comum, de desenvolvimento e de produção (unidas com `webpack-merge`); servidor de desenvolvimento com recarga automática; CSS extraído e minificado em produção; imagens, vídeos e fontes importados pelo JavaScript ou CSS; `src/index.html` como modelo; publicação no GitHub Pages com um comando.

**Como usar:** no GitHub, clique em **Use this template** → **Create a new repository** e rode `npm install`, depois `npm start` (desenvolvimento), `npm run build` (produção) ou `npm run deploy` (publica no GitHub Pages). Precisa do Node.js 22.15 ou mais novo (webpack-dev-server 6).
