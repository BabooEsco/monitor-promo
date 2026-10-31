# monitor-promo

Minisito di presentazione di **MONITOR** (BABOO ESCo), pubblicato su GitHub Pages
all'indirizzo **https://scopri-monitor.baboo.eu**. Grafica secondo la guida di stile MONITOR
(stile di monitor.baboo.eu); storyboard, schede video e form ripresi da scopri-mosaika.baboo.eu.

## Struttura
- `index.html` — tutto il sito (CSS e JS inline, nessuna dipendenza).
- `CNAME` — dominio personalizzato per GitHub Pages.
- `assets/` — logo, icone, favicon, sfondo impulso e mockup del telefono (il mockup è anche incorporato in `index.html`).
- `media/` — da creare quando arriveranno i video veri.

## Contenuti
Nel blocco `<script>` di `index.html`:
- `HERO` — storyboard del video di apertura generale.
- `AUD` — per ogni pubblico (Famiglie, Aziende, Condomini, Comunità energetiche): testi, video di apertura e 5 schede video con storyboard (`shots`).

Finché un elemento non ha il campo `video`, il player mostra lo storyboard
("video in produzione") con scene e sottotitoli temporizzati.

## Pubblicazione (da fare solo dopo approvazione)
1. Creare il repo `BabooEsco/monitor-promo` e caricare questi file sul branch `main`.
2. Settings → Pages → Source: *Deploy from a branch*, `main` / root.
3. DNS di baboo.eu: record `CNAME` `scopri-monitor` → `babooesco.github.io`
   (stessa impostazione usata per scopri-mosaika).
4. In Settings → Pages verificare il dominio e attivare *Enforce HTTPS*.

Link diretti per pubblico: `#famiglie`, `#aziende`, `#condomini`, `#cer`.
