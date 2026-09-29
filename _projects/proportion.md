---
alt_url: /en/projects/proportion/
title: "ProPortion"
tagline: "Ricalcola le dosi delle ricette: per persone, ingrediente, fattore o dispensa."
language: "Kotlin"
tags: ["Android", "Jetpack Compose"]
playstore: null
private_repo: true
featured: true
order: 1
---

<!-- playstore: aggiungi il link Play Store quando lo hai a portata di mano -->

ProPortion è un'app Android che ricalcola le dosi delle ricette di cucina. Funziona completamente
offline: non serve un account, non c'è sincronizzazione, non c'è raccolta dati.

Si inserisce una ricetta con le sue quantità e il numero di persone per cui è pensata, poi si
ricalcola ogni quantità a partire da un solo vincolo — persone diverse, la quantità disponibile di
un ingrediente, un moltiplicatore, oppure quello che c'è davvero in dispensa. Il valore aggiunto
rispetto a fare i conti a mente è la correttezza in cucina: l'app sa che le uova non si possono
dimezzare, che "un pizzico di sale" non si scala, e che una torta cotta a 1,5× la dose non cuoce
per 1,5× il tempo.

![Dashboard di ProPortion](/assets/images/projects/proportion/home.png)

## Cosa fa

- **Quattro modi per scalare una ricetta:** per persone, per un ingrediente disponibile, per un
  fattore diretto (×0,5, ×2, ×3, o un valore a piacere), oppure per quello che c'è in dispensa —
  con calcolo del fattore limitante e segnalazione dell'ingrediente collo di bottiglia.
- **Avvisi intelligenti:** arrotondamento per ingredienti discreti (uova, spicchi, fette...) e
  avviso da forno quando il fattore di scala esce dalla fascia 0,7×–1,4×, con suggerimento di un
  nuovo diametro teglia.
- **Proporzioni salvabili come varianti**, condivisione come testo o file `.proportion`, backup e
  ripristino dell'intera libreria.
- **Modalità cucina** a schermo acceso, lista della spesa persistente, e conversione tra peso,
  volume e quantità (incluse unità imperiali).
- Italiano, inglese, spagnolo e catalano. Temi chiari/scuri, supporto Material You.

![Modalità cottura](/assets/images/projects/proportion/cook-mode.png)

## Licenza e privacy

Software libero, licenza **GNU GPL v3.0**. Nessun dato lascia il dispositivo: nessun account,
nessuna sincronizzazione cloud.
