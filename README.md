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
- `assets/cv_en.pdf` and `assets/cv_zh.pdf` contain the English and Chinese editions of the general CV.
- `assets/fonts/`: locally hosted Inter font and its SIL Open Font License.
- `assets/favicon.svg`: site icon.

Earlier publications use native HTML disclosure elements. The page does not require JavaScript or external font services.

## Publishing

GitHub Pages publishes the root of the `main` branch in <https://github.com/ZillionWong/ZillionWong.github.io>. Push changes to `main` to update the website. The `.nojekyll` file enables serving the static files directly.

The homepage serves the general CV. Compile `cv_en.tex` and `cv_zh.tex` with XeLaTeX from `../cv/general/` and check both PDFs. Update any matching publication or research details in `index.html`. From the homepage directory, copy the two general editions into the site before publishing.

```powershell
Copy-Item -LiteralPath '../cv/general/cv_en.pdf' -Destination 'assets/cv_en.pdf'
Copy-Item -LiteralPath '../cv/general/cv_zh.pdf' -Destination 'assets/cv_zh.pdf'
```

When replacing the photograph, update its dimensions in `index.html` and adjust its framing in `assets/site.css` as needed.

Local archives are excluded from version control.
