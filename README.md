# Horváth György – weboldal

Egyoldalas (landing page) bemutatkozó weboldal Horváth György ICD‑ és integrált kranioszakrális terapeuta részére. A menüpontok az oldal szekcióihoz görgetnek.

## Felépítés

```
index.html        – a teljes oldal (szekciók: Bemutatkozás, Szemlélet, ICD, Kranioszakrális, Történetem, Kapcsolat)
css/style.css     – stílusok (türkiz + természetes színek, reszponzív)
js/main.js        – mobil menü, aktív menüpont, görgetési animáció, jegyzetkapcsoló, űrlap
images/           – fotók (portré + kezelésképek)
```

Nincs build lépés: az `index.html` bármilyen statikus tárhelyre feltölthető (pl. Netlify, GitHub Pages, cPanel). Helyben megnyitható dupla kattintással is.

## Szerkesztői jegyzetek (első változat)

Az oldalon sárga, szaggatott keretes **jegyzetek** jelzik, hol hiányzik még információ Gyuritól (kérdések az adott szövegrésznél). A jobb alsó sarokban lévő gombbal a jegyzetek elrejthetők, így a „tiszta” változat is megnézhető.

A végleges verzióhoz:

1. a `<aside class="note">` és `.note--inline` elemeket töröljük az `index.html`‑ből,
2. a `#notes-toggle` gombot és a hozzá tartozó JS/CSS részt eltávolítjuk,
3. a kapcsolati adatokat (telefon, e‑mail, cím) és az űrlap bekötését (jelenleg `mailto:`) véglegesítjük,
4. elkészítjük az adatkezelési tájékoztatót és az impresszumot.
