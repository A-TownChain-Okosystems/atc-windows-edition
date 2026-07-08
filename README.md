# ATC Windows Edition

## Status: Sprachentscheidung getroffen (08.07.2026) -- Sprint 0 offen

Windows-native Version des A-TownChain-Oekosystems. **Sprache: Rust** (Entscheidung
vom 08.07.2026) -- aber **nicht** bare-metal/no_std wie der ShivaCore-Kernel, sondern
Rust mit **std** fuer klassisches Windows-Deployment (Ziel-Target z.B.
`x86_64-pc-windows-msvc`).

## Wichtige Abgrenzung

- **GlobusOS / ShivaCore** (bare-metal Rust no_std, siehe
  [atc-shivacore](https://github.com/A-TownChain-Okosystems/atc-shivacore)) bleibt der
  alleinige OS-Standard des Oekosystems. Dieses Repo ersetzt das nicht.
- Dieses Repo ist eine **separate, parallele** Windows-Applikation/Client
  (klassisches gehostetes Rust mit `std`, kein eigener Kernel/Bootloader).
- Beide Projekte teilen die Sprache (Rust), aber nicht die Zielplattform-Ebene:
  ShivaCore = bare-metal OS-Kernel, Windows-Edition = Anwendung auf bestehendem
  Windows-Unterbau.

## Offene Fragen

- **Scope:** Desktop-App (z.B. Wallet/Explorer/Dashboard als GUI, Kandidat:
  `egui`/`tauri`) oder Windows-Dienst/CLI-Tool? Noch offen.
- **Verhaeltnis zu bestehenden Repos:** Wiederverwendung von API-Vertraegen aus
  `atc-backend`/`atc-gateway` wahrscheinlich, Details folgen nach Scope-Entscheidung.

## Naechster Schritt

Scope festlegen (Desktop-App vs. Dienst/CLI), danach Sprint 0: Cargo-Projekt mit
Windows-Target aufsetzen, "Hello World" fuer den gewaehlten Scope.

---
*Aktualisiert: 08.07.2026 -- Rust-Entscheidung getroffen, Scope noch offen.*
