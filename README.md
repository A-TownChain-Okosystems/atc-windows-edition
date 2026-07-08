# ATC Windows Edition

## Status: Vision / Planungsphase -- kein Code vorhanden

Dieses Repository ist der Platzhalter fuer eine **Windows-native Version** des
A-TownChain-Oekosystems, die **nicht** auf dem bare-metal ShivaCore-Kernel
(Rust, no_std, siehe [atc-shivacore](https://github.com/A-TownChain-Okosystems/atc-shivacore))
aufbaut, sondern in einer **anderen, noch zu waehlenden Programmiersprache**
fuer klassisches Windows-Deployment entwickelt wird.

## Wichtige Abgrenzung

- **GlobusOS / ShivaCore** (das eigentliche bare-metal Betriebssystem-Projekt)
  bleibt der alleinige OS-Standard des Oekosystems -- siehe Architektur-Entscheidung
  vom 05.07.2026 (eigener Kernel von Grund auf, Rust no_std, kein Linux-Unterbau).
- Dieses Repo ersetzt **nicht** GlobusOS/ShivaCore. Es ist ein **separates,
  paralleles Vorhaben** fuer eine Windows-Zielgruppe, die eine klassische
  installierbare Anwendung (kein eigenes OS/Kernel) erwartet.

## Offene Fragen (noch zu klaeren)

- **Sprache:** Welche Sprache fuer die Windows-Version? Kandidaten: C#/.NET
  (schnelle Windows-Integration, WinUI/WPF), C++ (Performance, naeher an
  bestehenden Rust-Kernel-Konzepten), oder etwas anderes -- noch nicht
  entschieden.
- **Scope:** Handelt es sich um einen Windows-Client/eine Desktop-App fuer
  Teile des Oekosystems (z.B. Wallet, Explorer, Dashboard) oder um einen
  eigenstaendigen Windows-Systemdienst? Noch offen.
- **Verhaeltnis zu bestehenden Repos:** Falls Teile aus `atc-mobile`,
  `atc-frontend` oder `atc-backend` wiederverwendet werden sollen (z.B. als
  Referenz fuer API-Vertraege), wird das hier dokumentiert, sobald geklaert.

## Naechster Schritt

Sprachentscheidung treffen, danach Sprint-0-Grundgeruest anlegen (analog zu
[KERNEL_FROM_SCRATCH_PLAN.md](https://github.com/A-TownChain-Okosystems/a-townchain-os/blob/main/KERNEL_FROM_SCRATCH_PLAN.md)
fuer ShivaCore).

---
*Angelegt: 08.07.2026 -- Vision/Planungs-Repo, kein produktiver Code.*
