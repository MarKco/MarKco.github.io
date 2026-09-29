---
title: "TokenCounter"
tagline: "A terminal TUI for tracking token consumption over time, in percentage or in dollars."
language: "Python"
tags: ["TUI", "CLI"]
github: "https://github.com/MarKco/tokencounter"
order: 2
alt_url: /progetti/tokencounter/
---

A colored terminal application (TUI) for tracking token consumption over time, in percentage or in
dollars, with line or bar graphs, a projected trend, and a monthly reset cycle.

It works in two independent modes — percentage (0-100%) or dollars (with a configurable spending
ceiling) — switching between them with `Ctrl+M` without losing the other mode's data. Everything is
saved to `~/.config/tokencounter/data.json`. It also includes a demo mode (`Ctrl+D`) that generates
simulated data to preview the graph's behavior without touching real data.
