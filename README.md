# nice!view-c

Ein custom nice!view Shield für ZMK Keyboards mit erweiterten Features und optimierten Widget-Funktionen.

## Übersicht

Dieses Repository enthält eine erweiterte Implementierung des nice!view Displays für ZMK KeymapCharts mit:

- **Custom Status Screen**: Erweiterte Anzeige für Tastaturstatus, Batterie und Bluetooth-Profile
- **Optimierte Widgets**: Hochperformante C-Implementierung für die Displayanzeige
- **Shield Definition**: Vollständige ZMK Shield-Konfiguration

## Struktur

```
├── boards/shields/nice_view-c/     # Shield Definitionsdateien
│   ├── widgets/                    # Custom Widget-Implementierungen
│   ├── nice_view-c.overlay         # Devicetree Overlay
│   ├── nice_view-c.conf            # Konfigurationsdatei
│   └── CMakeLists.txt              # Build-Konfiguration
├── zephyr/                         # Zephyr Module Definition
└── LICENSE                         # Lizenzinformation
```

## Installation

Dieses Shield wird als Zephyr-Modul in ein ZMK-Projekt integriert:

1. Kopiere dieses Verzeichnis in dein ZMK-Projekt
2. Aktualisiere deine `west.yml` Konfiguration

```yaml
manifest:
  projects:
    # ... deine anderen Module ...
    - name: nice-view-c
      url: https://github.com/mrtnRitter/nice-view-c
```

3. Konfiguriere dein Shield in der `.conf` Datei:

```
CONFIG_SHIELD=nice_view_c
```

## Custom Widgets

Das Shield beinhaltet mehrere optimierte Widget-Funktionen:

- **Status Widget**: Zeigt Bluetooth-Verbindungsstatus und Profile
- **Battery Widget**: Batterie- und Ladestandanzeige
- **Peripheral Status**: Unterbrechungstoggles und Statusanzeigen

## Lizenz

Dieses Projekt unterliegt der im `LICENSE` File festgelegten Lizenz.

## Support

Weitere Informationen zur Konfiguration und Verwendung findest du in der Dokumentation der einzelnen Shield-Komponenten.
