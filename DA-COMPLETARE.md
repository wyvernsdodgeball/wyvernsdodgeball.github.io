# ✅ Cose da completare o verificare

Elenco di quello che nel sito è provvisorio o da confermare. Cancella le righe man mano che le sistemi.

## Prima di pubblicare
- [ ] GitHub → Settings → Secrets: `CLOUDINARY_CLOUD_NAME`, `CLOUDINARY_API_KEY`, `CLOUDINARY_API_SECRET`.
- [ ] GitHub → Settings → Actions → General → Workflow permissions → **Read and write**.
- [ ] `_templates/TEMPLATE-album.md`: sostituire `TUO-CLOUD-NAME` con il cloud name Cloudinary.

## Contenuti da confermare con la squadra
- [ ] **Corso principianti (martedì)** e **corso bambini (mercoledì)**: quando partono davvero, togliere le frasi "parte al raggiungimento delle adesioni" in `index.html`, `_pages/unisciti.md`, `_pages/dodgeball-roma.md` e nella prima news.
- [ ] **Fascia d'età del corso bambini** (es. 8–13 anni): aggiungerla nelle card "Bambini" e nella FAQ.
- [ ] **Età minima per gli adulti** (es. dai 16 anni): aggiungerla nella card "Adulti" in `_pages/unisciti.md`.
- [ ] **Quote di iscrizione / prova gratuita**: oggi il sito dice solo "contattaci per le quote". Se il primo allenamento è gratuito, scriverlo (è un ottimo argomento: Ravenna lo mette ovunque).
- [ ] **Campionato**: ora il sito dice "Campionato Nazionale FIGeST". Se volete, aggiungere categoria/serie e risultati in home e in `_pages/squadra.md`.
- [ ] **Coordinate palestra** in `_includes/schema-org.html` (`latitude`/`longitude`): sono approssimative per Via Antonino Pio; correggile con quelle esatte da Google Maps (tasto destro sul punto → copia coordinate).
- [ ] **Link Facebook**: ho usato l'URL della pagina `facebook.com/p/ASD-Wyverns-Dodgeball-61577622093632/`. Verifica che apra la pagina giusta.

## Foto
- [ ] **Foto hero e sfondi**: oggi `assets/images/wyverns-dodgeball-roma-hero.webp` è un'immagine grafica col logo. Sostituiscila con una vera foto orizzontale della squadra (1920×1080, WebP, < 400 KB), stesso nome file.
- [ ] `_pages/unisciti.md`: le tre righe orari usano la stessa immagine di sfondo (`--row-photo`). Mettere una foto diversa per adulti / principianti / bambini.
- [ ] `_pages/squadra.md`: ho tolto la galleria/carosello di Ravenna perché non ci sono foto. Quando ne hai 10–20, si può riaggiungere (il codice è nel repo originale, sezione `#galleria`).
- [ ] **Immagine anteprima social** (`wyverns-dodgeball-roma-og.jpg`, 1200×630): oggi è il logo su sfondo scuro; una foto di gruppo funziona meglio su WhatsApp/Facebook.
- [ ] Le foto dei bambini richiedono la liberatoria dei genitori.

## Dopo la pubblicazione
- [ ] Google Search Console → codice di verifica in `_config.yml` (`google_site_verification`).
- [ ] Google Business Profile della palestra/associazione.
- [ ] Analytics: lasciato spento. Se lo attivi (`google_analytics` in `_config.yml`) serve un banner cookie.
- [ ] Aggiornare il link nella bio di Instagram, TikTok, Facebook, YouTube ed Eventbrite.
