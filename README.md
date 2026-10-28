# Horváth György – weboldal

Egyoldalas (landing page) bemutatkozó weboldal Horváth György ICD‑ és integrált kranioszakrális terapeuta részére. A menüpontok az oldal szekcióihoz görgetnek.

## Felépítés

```
index.html        – a teljes oldal (szekciók: Bemutatkozás, Szemlélet, ICD, Kranioszakrális, Történetem, Kapcsolat)
css/style.css     – stílusok (türkiz + természetes színek, reszponzív)
js/main.js        – mobil menü, aktív menüpont, görgetési animáció
images/           – fotók (portré + kezelésképek)
CNAME             – egyedi domain (GitHub Pages)
.github/workflows/pages.yml – automatikus közzététel GitHub Pages‑re
```

Nincs build lépés: az oldal statikus fájlokból áll, helyben is megnyitható dupla kattintással.

## Közzététel – GitHub Pages, https://terapiaazerdoszelen.hu

A `main` ágra érkező minden push után a `.github/workflows/pages.yml` workflow kiteszi az oldalt (csak az `index.html`, `CNAME`, `css/`, `js/`, `images/` kerül ki). Kézzel is indítható az Actions fülön.

Egyszeri beállítás:

1. **GitHub → Settings → Pages → Build and deployment → Source:** `GitHub Actions`.
2. **DNS a domainregisztrátornál** (`terapiaazerdoszelen.hu`):

   | Típus | Név | Érték |
   |-------|-----|-------|
   | A     | @   | 185.199.108.153 |
   | A     | @   | 185.199.109.153 |
   | A     | @   | 185.199.110.153 |
   | A     | @   | 185.199.111.153 |
   | AAAA  | @   | 2606:50c0:8000::153 |
   | AAAA  | @   | 2606:50c0:8001::153 |
   | AAAA  | @   | 2606:50c0:8002::153 |
   | AAAA  | @   | 2606:50c0:8003::153 |
   | CNAME | www | hdomos.github.io |

   Az @ alatti esetleges régi A/AAAA/ALIAS rekordokat (pl. a regisztrátor parkolóoldalát) törölni kell.
3. **Settings → Pages → Custom domain:** `terapiaazerdoszelen.hu` → Save. (Actions‑alapú közzétételnél ez a beállítás számít, a `CNAME` fájl csak a domain rögzítésére van a repóban.)
4. Amikor a DNS‑ellenőrzés zöld és a tanúsítvány elkészült (pár perc – max. 24 óra): **Enforce HTTPS** bekapcsolása.
5. Ajánlott: **GitHub profil → Settings → Pages → Add a domain** – a domain ellenőrzése, hogy más repó ne foglalhassa el.

A `www.terapiaazerdoszelen.hu` automatikusan átirányít a fő címre.

## Hátralévő teendők a végleges változathoz

1. a Facebook/Instagram linkek bekötése a láblécbe,
2. az adatkezelési tájékoztató és az impresszum elkészítése (a láblécben most `#`‑re mutatnak),
3. a „Történetem” szekció végleges szövege.
