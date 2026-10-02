# Osebna domača stran – Goran

Statična stran brez odvisnosti (HTML + CSS + JS). Datoteke:

- `index.html` – struktura strani
- `style.css` – temen, odziven dizajn
- `links.js` – seznam podstrani (kartic)

## Dodajanje nove podstrani

Odprite `links.js` in v seznam `window.LINKS` dodajte nov vnos:

```js
{
  title: "Moja podstran",
  description: "Kratek opis podstrani.",
  url: "https://nekaj.moja-domena.si",
  icon: "🚀"
},
```

- Vnose ločite z vejico.
- Polje `placeholder: true` prikaže oznako »Nadomestni vnos« – pri pravih vnosih ga izpustite.
- Nadomestne vnose (`*.example.si`) zamenjajte ali izbrišite.
- Ime, opis in besedilo noge uredite v `index.html`.

## Lokalni predogled

```bash
cd homepage
python3 -m http.server 8080
```

Nato odprite http://localhost:8080.

## Objava

Stran je povsem statična, zato jo lahko objavite kjerkoli:

**GitHub Pages**
1. Datoteke naložite v GitHub repozitorij.
2. Settings → Pages → Source: izberite vejo (`main`) in mapo (`/` ali `/homepage`).
3. Lastno domeno nastavite pod »Custom domain« in v DNS dodajte zapis CNAME.

**Netlify**
1. Prijavite se na netlify.com → »Add new site« → »Deploy manually« in povlecite mapo `homepage`,
   ali povežite repozitorij (Build command: prazno, Publish directory: `homepage` ali `.`).
2. Domeno dodajte pod »Domain management«.

**Cloudflare Pages**
1. Dashboard → Workers & Pages → Create → Pages → povežite repozitorij ali naložite mapo.
2. Build command: prazno, Output directory: `homepage` (ali `/`).
3. Domeno dodajte pod »Custom domains«.
