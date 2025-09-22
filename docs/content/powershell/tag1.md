# Cmdlet


Ein PowerShell-Befehl, die in der Konsole ausgeführt werden kann, wird `Cmdlet` genannt.

Es hat immer die Form:

```bash
<Cmdlet> -Parameter Wert
```

```powershell
get-childitem                        # Listet Dateien/Ordner im aktuellen Verzeichnis
get-help <Befehl>                    # Zeigt Hilfe zu einem Cmdlet
get-help <Befehl> -online            # Öffnet die Online-Hilfe
get-command -Noun Date
get-command -noun Date -verb get
get-command -noun D*
```
