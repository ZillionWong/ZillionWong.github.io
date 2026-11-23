# Zilin Wang

Source for my academic homepage: <https://zillionwong.github.io/>.

## Local preview

Open `index.html` directly in a browser, or serve this directory:

```sh
python -m http.server 8000 --bind 127.0.0.1
```

Then visit <http://127.0.0.1:8000>. No build step or package installation is required.

## Files

- `index.html`: biography, research, publications, and service.
- `assets/site.css`: typography and responsive layout.
- `assets/portrait.jpg`: profile photograph.
- `assets/cv.pdf` and `assets/cv-zh.pdf` contain the English and Chinese CVs.
- `assets/fonts/`: locally hosted Inter font and its SIL Open Font License.
- `assets/favicon.svg`: site icon.

Earlier publications use native HTML disclosure elements. The page does not require JavaScript or external font services.

## Publishing

GitHub Pages publishes the root of the `main` branch in <https://github.com/ZillionWong/ZillionWong.github.io>. Push changes to `main` to update the website. The `.nojekyll` file enables serving the static files directly.

Maintain both CVs in `../cv/cv.tex`. The English and Chinese versions share the publication list and dates. Edit both arguments of `\cvtext{English}{中文}` when revising translated text, and update the corresponding homepage entry when it mentions the same information. Compile `cv.tex` (English) and `cv-zh.tex` (Chinese) with XeLaTeX from `../cv/` and verify both PDFs. From this directory, copy both PDFs into the site before publishing.

```powershell
Copy-Item -LiteralPath '../cv/cv.pdf' -Destination 'assets/cv.pdf'
Copy-Item -LiteralPath '../cv/cv-zh.pdf' -Destination 'assets/cv-zh.pdf'
```

When replacing the photograph, update its dimensions in `index.html` and adjust its framing in `assets/site.css` as needed.

Local archives are excluded from version control.
