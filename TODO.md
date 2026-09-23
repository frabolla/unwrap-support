# TODO

## Download dell'app dal sito
Decisione: **Opzione A — link diretto a GitHub Releases**. ✅ Fatto.
Repo dell'app: **frabolla/unwrap-macOS-release**. Release v1.0
pubblicata il 23/09/2026, asset `Unwrap.dmg`.

- [x] Pubblicare il binario (.dmg) come asset di una GitHub Release del
      repo `frabolla/unwrap-macOS-release` (release v1.0).
- [x] Collegare in `index.html` (IT ed EN) il pulsante "Scarica per
      Mac" a
      `https://github.com/frabolla/unwrap-macOS-release/releases/latest/download/Unwrap.dmg`
      (il link `latest` punta sempre automaticamente all'ultima
      versione, senza doverlo aggiornare a ogni nuova release — **a
      patto che l'asset si chiami sempre `Unwrap.dmg` in ogni
      release futura**, altrimenti il link non troverà il file).
- [x] Collegare il link "Note di rilascio" a
      `https://github.com/frabolla/unwrap-macOS-release/releases`.
- [ ] Confermare che l'app in questa release sia firmata con
      certificato Developer ID e notarizzata presso Apple (necessario
      per non essere bloccata da Gatekeeper al primo avvio).

## Aggiornamenti automatici (Sparkle)
- [ ] Integrare [Sparkle](https://sparkle-project.org) nell'app per
      permettere l'auto-update fuori dal Mac App Store.
- [ ] Generare e pubblicare il feed appcast (XML) a ogni release, con
      changelog.
- [ ] Firmare gli update con la chiave EdDSA di Sparkle.

## Distribuzione via Homebrew
- [ ] Creare una formula Homebrew **cask** per Unwrap, così l'app si
      installa con `brew install --cask unwrap`.
- [ ] Sottomettere il cask a `homebrew-cask` (o mantenere un tap proprio,
      tipo `frabolla/homebrew-unwrap`, come primo passo più semplice).
- [ ] Tenere il cask aggiornato ad ogni nuova release (si può automatizzare
      con GitHub Actions).

## Mac App Store
- [ ] Completare la versione MAS (sandboxing, review Apple) e riattivare il
      pulsante "Disponibile su Mac App Store" sul sito, rimosso il
      23/09/2026 perché non ancora pronta.
