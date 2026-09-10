# 🐲 Wyverns Dodgeball — Sito Web

Sito ufficiale della **ASD Wyverns Dodgeball** — Dodgeball a Roma (San Paolo).  
Affiliati FIGeST · Allenamenti per adulti, principianti e bambini.

🌐 **https://wyvernsdodgeball.it**

> Il sito è basato sul lavoro dei [Ravenna Grizzlies](https://dodgeballravenna.it)
> ([repo originale](https://github.com/dynamogrizzly-creator/dynamogrizzly-creator.github.io)), usato con autorizzazione.

---

## 📋 Indice

- [Come aggiungere una news](#-news)
- [Come aggiungere un album fotografico](#-album-fotografici)
- [Cose da completare](DA-COMPLETARE.md)
- [Struttura del progetto](#-struttura-del-progetto)
- [Come funziona il sito](#-come-funziona-il-sito)
- [Per gli sviluppatori](#-per-gli-sviluppatori)

---

## 📰 News

Guida completa: **[COME-AGGIUNGERE-NEWS.md](COME-AGGIUNGERE-NEWS.md)** · Template: **[_templates/TEMPLATE-news.md](_templates/TEMPLATE-news.md)**

**In breve:**
1. Carica l'immagine in `assets/images/` (opzionale)
2. Crea un file in `_posts/` con nome `ANNO-MESE-GIORNO-titolo.md`
3. Copia il template, compila i campi, scrivi il testo
4. Commit → il sito si aggiorna in 2-3 minuti

---

## 📸 Album Fotografici

Guida completa: **[COME-AGGIUNGERE-ALBUM.md](COME-AGGIUNGERE-ALBUM.md)** · Template: **[_templates/TEMPLATE-album.md](_templates/TEMPLATE-album.md)**

**In breve:**
1. Carica le foto su [Cloudinary](https://cloudinary.com) in una cartella `ANNO/nome-evento`
2. Crea un file in `_pages/` con nome `album-ANNO-MESE-GIORNO-nome.md`
3. Copia il template e compila i campi
4. Commit → vai su **Actions → Sync Cloudinary Photos → Run workflow**
5. Aspetta 2-3 minuti → le foto appaiono sul sito

> ⚠️ Se è il primo album di un anno nuovo (es. 2027), crea `album/2027/index.html`
> copiando quello del 2026 e cambiando l'anno.

---

## 📁 Struttura del progetto

```
├── _layouts/              # Template HTML delle pagine
├── _includes/             # Navbar, footer, box contatti, dati schema.org
├── _pages/                # Pagine del sito (squadra, unisciti, dodgeball, dodgeball-roma, news, album, privacy)
├── _posts/                # News: ANNO-MESE-GIORNO-titolo.md
├── _templates/            # TEMPLATE-news.md, TEMPLATE-album.md
├── album/2026/index.html  # Pagina indice album per anno
├── assets/css|images|fonts|js
├── .github/workflows/sync-cloudinary.yml   # Sync foto da Cloudinary
├── .github/scripts/sync_cloudinary.py
├── _config.yml            # Configurazione (titolo, url, contatti, social)
├── COME-AGGIUNGERE-NEWS.md / COME-AGGIUNGERE-ALBUM.md
└── DA-COMPLETARE.md       # Elenco delle cose ancora da verificare/inserire
```

---

## ⚙️ Come funziona il sito

| Tecnologia | Uso |
|-----------|-----|
| **Jekyll** | Generatore di siti statici (lo esegue GitHub) |
| **GitHub Pages** | Hosting gratuito |
| **Cloudinary** | Storage e CDN per le foto degli album |
| **GitHub Actions** | Sync automatico foto da Cloudinary |

---

## 🛠 Per gli sviluppatori

### Avvio locale (opzionale)

```bash
bundle install
bundle exec jekyll serve --watch
```

Sito disponibile su `http://localhost:4000`

### Deploy

Automatico ad ogni push su `main` tramite GitHub Pages (Settings → Pages → Deploy from a branch → main).

### Secrets da impostare (Settings → Secrets and variables → Actions)

| Secret | Descrizione |
|--------|-------------|
| `CLOUDINARY_CLOUD_NAME` | Cloud name Cloudinary |
| `CLOUDINARY_API_KEY` | API Key Cloudinary |
| `CLOUDINARY_API_SECRET` | API Secret Cloudinary |

Ricorda anche: **Settings → Actions → General → Workflow permissions → Read and write**.

---

## 📬 Contatti

**ASD Wyverns Dodgeball**  
📧 wyvernsdodgeballasd@gmail.com · 📱 333 169 6568  
C.F. 96629020585 · Sede legale: Via Baldassarre Orero 55, 00159 Roma
