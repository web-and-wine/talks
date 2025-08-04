
--- 
author: Bitory GmbH - Tim Olbrich
date: 12.06.2025 
paging: Page %d of %d
--- 
theme: ascii
---
#  Fantastische Terminal Tools 
## und wo sie zu finden sind.
### Web and Wine - Juni 2025


```text
    @@@@@@@@@@@@@     @@@  @@@@@@@@@@@@@@@@@    @@@@@@@@@@@@      @@@@@@@@@@@@@    @@@@          @@@
    @@@@@@@@@@@@@@@   @@@@ @@@@@@@@@@@@@@@@@  @@@@@@@@@@@@@@@@    @@@@@@@@@@@@@@@  @@@@@       @@@@@
                @@@@  @@@@        @@@       @@@@@         @@@@@:::::          @@@@   @@@@     @@@@@ 
                @@@@  @@@@        @@@       @@@@         :::@@@@::::          @@@@    @@@@@  @@@@
@@@@@@@    @@@@@@@@   @@@@        @@@      @@@@      ::::    -::::            @@@@     @@@@@@@@@
@@@@@@@   @@@@@@@@@   @@@@        @@@      @@@@  ::::    :::::+@@ @@@    @@@@@@@@       @@@@@@@
    @@@          @@@  @@@@        @@@      @@@@::    ::::::: @@@@ @@@@ @@@@@@@@@          @@@@
    @@@          @@@@ @@@@        @@@      -@@@@:::::::::   @@@@  @@@@    @@@@@@          @@@
    @@@          @@@@ @@@@        @@@    :: --:::::::     @@@@@   @@@@       @@@@         @@@
    @@@@@@@@@@@@@@@@  @@@@        @@@   ::::::+@@@@@@@@@@@@@@@    @@@@        @@@@        @@@
    @@@@@@@@@@@@@@    @@@         @@@           @@@@@@@@@@@@      @@@         @@@@        @@@
```
---
# Warum Terminal-Tools verwenden?
- **Geschwindigkeit & Effizienz**:
  - Oft schneller als grafische Alternativen
  - Tastatur-zentrierter Workflow → keine Maus nötig

- **Remote-Fähigkeit**:
  - Funktionieren problemlos über SSH auf Servern
  - Kein GUI-Zugriff erforderlich

- **Ressourcenschonend**:
  - Brauchen wenig Speicher und CPU
  - Perfekt für ältere Maschinen oder schwache Server

- **Flexibilität & Komposition**:
  - Tools lassen sich miteinander kombinieren 
  - Kleine spezialisierte Tools → mächtige Workflows (Unix-Philosophie)

- **Plattformunabhängig**:
  - Funktionieren auf Linux, macOS und teilweise Windows (z. B. mit WSL)
  - Gleiche Tools lokal und remote nutzbar

- **Reproduzierbarkeit**:
  - Einmal definierte Befehle oder Skripte führen immer zum selben Ergebnis
  - Ideal für DevOps, Build-Prozesse, CI/CD

- **Community & Dokumentation**:
  - Viele Tools sind gut dokumentiert und weit verbreitet
  - Große Unterstützung in der Entwickler-Community

- **Erweiterbarkeit**:
  - Terminal-Tools können leicht erweitert oder angepasst werden
  - Viele haben Plugins oder lassen sich durch Konfigurationsdateien anpassen
---
# Terminal Multiplexer
- Gleichzeitiges Ausführen und Verwalten mehrerer Shell-Sessions.

- **Bekannte Tools**:
  - `tmux`
  - `zellij`

- **Features**:
  - Aufteilen des Terminals in **mehrere Fenster/Panels** (horizontal und vertikal)
  - **Detach & Reattach**: Session kann getrennt und später wieder verbunden werden
  - **Persistente Sessions**: Prozesse laufen weiter, auch wenn die Verbindung getrennt wird
  - **Session-Management**: Benennen, Listen und Wechseln von Sessions
  - **Tastenkombinationen**: Steuerung über konfigurierbare Tastenkürzel
  - **Scripting und Automatisierung**: Start von Sessions mit vordefinierten Layouts und Befehlen

- **Nutzungsszenarien**:
  - Arbeit auf entfernten Servern (z. B. über SSH)
  - Lang laufende Prozesse ohne Screen-Blocking
  - Paralleles Arbeiten an mehreren Projekten

---
# Coding (Neovim)


- **Verbesserte Plugin-Architektur**:
  - Plugins können in beliebigen Sprachen (z. B. Lua, Python) geschrieben werden
  - Asynchrone Ausführung von Plugins → keine Blockierung der UI

- **Eingebaute Lua-Unterstützung**:
  - Schneller, moderner Ersatz für Vimscript
  - Lua kann für Konfiguration, Plugins und Keybindings genutzt werden

- **Leichtgewichtig und schnell**:
  - Startet sofort, braucht kaum Ressourcen
  - Optimal für Low-End- oder Remote-Systeme

- **Terminal-Integration**:
  - Integriertes Terminalfenster (kein Wechsel zum externen Terminal nötig)
  - Praktisch für Testen, Build-Scripts, Git etc.

- **Bessere Defaults und UX**:
  - Viele Dinge funktionieren “out of the box” besser als in Vim
  - Weniger Bedarf für umfangreiche Basiskonfigurationen

- **LSP-Integration (Language Server Protocol)**:
  - Native Unterstützung für Autocompletion, Go-to-Definition, Hover, usw.
  - Funktioniert mit Tools wie `nvim-lspconfig`, `none-ls`, `mason`

- **Aktive Community und schnelle Entwicklung**:
  - Regelmäßige Updates mit Bugfixes und Features
  - Große Auswahl moderner Plugins (z. B. `telescope`, `nvim-tree`, `cmp`, `treesitter`)

- **Perfekt für Power-User**:
  - Maximale Kontrolle durch Tastenkombinationen, Makros, Scripting
---
# Git Tooling
- Git (wer hätte es gedacht)
- LazyGit 
- gh
---
# Docker Tooling
- Docker (wer hätte es gedacht)
- LazyDocker 
---
# Database
- LazySQL
---
# Learnings
- Passe deine Konfig nicht an wenn du gerade anfangen willst zu arbeiten (vielleicht auch Skill Issue)
- Erstmal die Basics in vertrauten Umgebungen
- Eventuell mit einer vorkonfigurierten Variante starten -> Iterieren
- Der gleichzeitige Umstieg auf vim und ein Split Keyboard killt die Produktivität
- Man lernt viel mehr über die eingesetzten Sprachen und deren Tooling
- Es kochen am Ende alle nur mit Wasser
---
# Fazit
- Würde ich es wieder tun? Ja!
- Ein spaßiges und personalisiertes Setup steigert den Spaß beim Arbeiten ungemein 
- Gesteigerte Produktivität (Die verlorene muss ja wieder reingeholt werden)
- Auf jedem Server etc. gibt es irgendwo ein vim
- Die Maus fühlt sich komisch an. 
- I use vim btw.
---
# Danke für die Aufmerksamkeit
```bash
:q
E37: No write since last change (add ! to override)
:q!
```
---
# Quellen
- [Slides](https://github.com/maaslalani/slides)
- [Neovim](https://neovim.io/)
- [LazyGit](https://github.com/jesseduffield/lazygit)
- [LazyDocker](https://github.com/jesseduffield/lazydocker)
- [LazySQL](https://github.com/jorgerojas26/lazysql)
- [Slides](https://github.com/maaslalani/slides)
- [Neovim](https://neovim.io/)
