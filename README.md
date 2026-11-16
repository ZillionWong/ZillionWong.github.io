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
- `assets/cv.pdf`: downloadable curriculum vitae.
- `assets/fonts/`: locally hosted Inter font and its SIL Open Font License.
- `assets/favicon.svg`: site icon.

Earlier publications use native HTML disclosure elements. The page does not require JavaScript or external font services.

## Publishing

GitHub Pages publishes the root of the `main` branch in <https://github.com/ZillionWong/ZillionWong.github.io>. Push changes to `main` to update the website. The `.nojekyll` file enables serving the static files directly.

The CV source and compiled PDF are maintained separately in `../cv/`. After updating `../cv/cv.pdf`, copy it to `assets/cv.pdf` to update the downloadable version on the website. From this directory in PowerShell:

```powershell
Copy-Item -LiteralPath '../cv/cv.pdf' -Destination 'assets/cv.pdf'
```

When replacing the photograph, update its dimensions in `index.html` and adjust its framing in `assets/site.css` as needed.

Local archives are excluded from version control.
