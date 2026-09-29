---
alt_url: /en/projects/tokencounter/
title: "TokenCounter"
tagline: "TUI da terminale per tracciare il consumo di token nel tempo, in percentuale o in dollari."
language: "Python"
tags: ["TUI", "CLI"]
github: "https://github.com/MarKco/tokencounter"
order: 2
---

Un'applicazione da terminale (TUI) colorata per tenere traccia del consumo di token nel tempo, in
percentuale o in dollari, con grafici a linee o a barre, tendenza proiettata e ciclo di reset
mensile.

Funziona in due modalità indipendenti — percentuale (0-100%) o dollari (con un tetto di spesa
configurabile) — passando dall'una all'altra con `Ctrl+M` senza perdere i dati dell'altra modalità.
Tutto viene salvato in `~/.config/tokencounter/data.json`. Include anche una modalità demo
(`Ctrl+D`) che genera dati simulati per vedere il comportamento del grafico senza toccare i dati
reali.
