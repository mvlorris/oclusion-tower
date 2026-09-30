# Vision Tower — reconstrução estática

Reconstrução independente do painel Vision Tower feita em **HTML, CSS e JavaScript puro**, sem frameworks e sem backend. O objetivo é fornecer uma base visual e interativa que possa ser publicada no GitHub Pages.

## Executar localmente

Abra `index.html` diretamente no navegador ou, preferencialmente, rode um servidor estático:

```bash
python3 -m http.server 8000
```

Depois acesse `http://127.0.0.1:8000`.

No login local, qualquer usuário e senha não vazios entram no modo demonstrativo. Nenhuma senha real foi incluída no projeto.

## Publicar no GitHub Pages

1. Crie um repositório no GitHub.
2. Envie estes quatro arquivos: `index.html`, `styles.css`, `app.js` e `data.js`.
3. No repositório, abra **Settings → Pages**.
4. Em **Build and deployment**, selecione **Deploy from a branch**.
5. Escolha a branch `main` e a pasta `/root`.
6. Salve e aguarde a URL do GitHub Pages.

Também é possível publicar pela linha de comando:

```bash
git init
git add .
git commit -m "Reconstrução estática do Vision Tower"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git
git push -u origin main
```

## O que está implementado

A interface inclui tela de acesso local, cabeçalho com navegação, métricas, distribuição operacional, busca, filtros por unidade/movimento/situação, paginação, lista de veículos, alertas, relatórios demonstrativos, preferências de densidade/tema e persistência local do usuário e preferências.

## Limites

Esta reconstrução não acessa o backend original, não atualiza posições em tempo real, não replica autenticação real nem grava alterações no servidor. Os veículos em `data.js` são um recorte dos dados renderizados no momento da inspeção e servem como dados demonstrativos. Para dados reais, substitua `data.js` por uma API própria autorizada.
