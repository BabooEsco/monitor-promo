# monitor-promo

Minisito di presentazione di **MONITOR** (BABOO ESCo), pubblicato su GitHub Pages
all'indirizzo **https://scopri-monitor.baboo.eu**. Grafica secondo la guida di stile MONITOR
(stile di monitor.baboo.eu); storyboard, schede video e form ripresi da scopri-mosaika.baboo.eu.

## Struttura
- `index.html` — tutto il sito (CSS e JS inline, nessuna dipendenza).
- `CNAME` — dominio personalizzato per GitHub Pages.
- `assets/` — logo, icone, favicon, sfondo impulso e mockup del telefono (il mockup è anche incorporato in `index.html`);
  `logo-baboo-light.png` è il logo BABOO del piè di pagina (copia da baboo.eu).
- `media/` — da creare quando arriveranno i video veri.

## Contenuti
Nel blocco `<script>` di `index.html`:
- `HERO` — storyboard del video di apertura generale.
- `AUD` — per ogni pubblico (Famiglie, Aziende, Condomini, Comunità energetiche, Installatori): testi, video di apertura e 5 schede video con storyboard (`shots`).

Finché un elemento non ha il campo `video`, il player mostra lo storyboard
("video in produzione") con scene e sottotitoli temporizzati.

## Inserire un video vero
1. Caricare il file in `media/` (MP4 H.264 + AAC, 1280×720 o 1920×1080, con `-movflags +faststart`).
2. Nell'elemento (`HERO`, `hero` del pubblico o una delle `cards`) aggiungere:
   `video:'media/nome.mp4'` e, se servono, `poster:'media/nome.jpg'`, `vtt:'media/nome.vtt'`, `dur:52`.
3. Gli `shots` restano: diventano i capitoli cliccabili sotto il video (`t` = secondo nel video).
   `dur` è la durata scritta sulle schede; senza `dur` le schede mostrano quella dello storyboard.
4. Se il file non si carica, il player torna da solo allo storyboard.

## Pubblicazione (da fare solo dopo approvazione)
1. Creare il repo `BabooEsco/monitor-promo` e caricare questi file sul branch `main`.
2. Settings → Pages → Source: *Deploy from a branch*, `main` / root.
3. DNS di baboo.eu: record `CNAME` `scopri-monitor` → `babooesco.github.io`
   (stessa impostazione usata per scopri-mosaika).
4. In Settings → Pages verificare il dominio e attivare *Enforce HTTPS*.

Link diretti per pubblico: `#famiglie`, `#aziende`, `#condomini`, `#cer`, `#installatori`.
