# Sajt — Boško Tabaković, licencirani medijator

Statički sajt (HTML/CSS/JavaScript). Nema bekenda, nema WordPress-a, nema baze.

## Postavljanje na GitHub Pages

1. U repozitorijumu `mediator-site` obriši stare fajlove.
2. **Add file → Upload files** → prevuci SVE fajlove iz ovog foldera → **Commit changes**.
3. Settings → Pages → Source: `main`, folder `/ (root)`.
4. Za minut-dva sajt je živ na `https://<korisnik>.github.io/mediator-site/`.

## Šta OBAVEZNO treba zameniti pre objave

Podaci su trenutno primeri iz dizajna. Otvori `build.py` nije potreban — menjaj direktno u HTML fajlovima
(Ctrl+H, zameni svuda) ili traži ove nizove:

| Šta | Trenutna vrednost | Gde |
|---|---|---|
| Telefon (prikaz) | `+381 64 123 45 67` | svi fajlovi |
| Telefon (link) | `+381641234567` | svi fajlovi (`tel:`, `viber:`, `wa.me`) |
| E-mail | `info@boskotabakovic.rs` | svi fajlovi |
| Društvene mreže | `href="#"` u futeru | svi fajlovi |

## Slike koje se dodaju kasnije

Samo ubaci fajl sa tačno ovim imenom u isti folder i sajt ga automatski pokupi:

- `hero.jpg` — pozadinska fotografija na početnoj (kancelarija, sto za sastanke). Preporuka: široka, min. 1920px.
- `bosko.jpg` — portret. Prikazuje se na početnoj i na stranici „O meni“.
- `licenca.jpg` — sken dozvole za posredovanje. Prikazuje se u zlatnom ramu na stranici „O meni“.

Dok fajlovi ne postoje, sajt prikazuje elegantnu zamenu — ništa se ne lomi.

## Kontakt forma

Forma otvara e-mail program posetioca (`mailto:`). Ako želiš da poruke stižu direktno u inbox
bez otvaranja e-mail programa, besplatno rešenje je **Formspree** (formspree.io) — registracija,
pa se `<button>` zameni `<form action="https://formspree.io/f/TVOJ_ID" method="POST">`.

## Kalkulator troškova

Obračun je po *Pravilniku o tarifi o nagradama i naknadama u postupku posredovanja*
(„Sl. glasnik RS“, br. 35/2015), vrednost poena 100 din. Ako se tarifa promeni,
brojke se menjaju u `troskovi.html` — u nizu `PROC` (procenjivi predmeti) i u `<select id="tipSpora">`
(neprocenjivi predmeti).

## Fajlovi

- `index.html` — početna
- `o-meni.html`, `o-medijaciji.html`, `usluge.html`
- `porodicna-medijacija.html`, `radna-medijacija.html`, `privredna-medijacija.html`,
  `gradjanska-medijacija.html`, `potrosacka-medijacija.html`, `ostali-sporovi.html`
- `troskovi.html` (kalkulator), `pravni-okvir.html`, `blog.html`, `blog-zasto-medijacija.html`, `kontakt.html`
- `style.css` — sve boje i stilovi na jednom mestu (vrh fajla: `:root`)
- `main.js` — mobilni meni
