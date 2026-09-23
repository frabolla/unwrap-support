# TODO

## Download dell'app dal sito
Decisione: **Opzione A — link diretto a GitHub Releases**.
Repo dell'app: **frabolla/unwrap-macOS** (nessuna release pubblicata
al 23/09/2026).

- [ ] Firmare l'app con certificato Developer ID e notarizzarla presso Apple
      (necessario comunque, indipendentemente dal canale di distribuzione:
      senza notarizzazione Gatekeeper blocca l'app al primo avvio).
- [ ] Pubblicare il binario (.dmg o .zip) come asset di una GitHub Release
      del repo `frabolla/unwrap-macOS`.
- [ ] Non appena la release è pubblicata, sostituire in `index.html`
      (IT ed EN) il link segnaposto `#download-placeholder` del pulsante
      "Scarica per Mac" con:
      `https://github.com/frabolla/unwrap-macOS/releases/latest/download/<NomeFile>.dmg`
      (`<NomeFile>` = nome esatto dell'asset caricato nella release; il
      link `latest` punta sempre automaticamente all'ultima versione,
      senza doverlo aggiornare a ogni nuova release).
- [ ] Sostituire anche il link "Note di rilascio" con
      `https://github.com/frabolla/unwrap-macOS/releases`.
- [ ] Riattivare i due `<a>` (rimuovere `onclick="return false;"`).

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
