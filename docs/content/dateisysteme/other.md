# Dateisystemvergleich

{{ youtube_video("https://www.youtube.com/embed/_h30HBYxtws?si=h3cR81XJ96xiauSK") }}

## Kernaussagen (Kurzfassung)
- **FAT32** ist sehr kompatibel, unterstützt aber **nur Dateien bis 4 GB** und ist für moderne, große Datenträger ungeeignet.
- **exFAT** ist der **Kompromiss für Wechseldatenträger** (USB/SD): große Dateien, wenig Overhead, breite Unterstützung in Windows, macOS und vielen Geräten.
- **NTFS** ist das **Standard-Dateisystem für Windows-Laufwerke** mit **Rechten, Verschlüsselung, Quotas, Kompression** und **Journaling**.
- **ext4** ist das **Standard-Dateisystem vieler Linux-Distributionen**; unterstützt große Volumes/Dateien, Journaling und Extents.
- **APFS** ist das **moderne Dateisystem von Apple** (macOS/iOS/iPadOS): **Copy-on-Write, Snapshots, Verschlüsselung**, für SSDs optimiert.

## Vergleichstabelle
| Merkmal | FAT32 | exFAT | NTFS | ext4 | APFS |
|---|---|---|---|---|---|
| **Typische Nutzung** | Sehr alte Geräte, maximale Kompatibilität | USB-Sticks, SD-Karten, externe Laufwerke | Windows-System-/Datenlaufwerke, externe Laufwerke (Windows-fokussiert) | Linux-System-/Datenlaufwerke | macOS-/iOS-Geräte, Apple-Ökosystem |
| **Max. Dateigröße (typisch)** | 4 GB | sehr groß (praktisch >> 4 GB) | sehr groß (praktisch >> TB) | sehr groß (praktisch >> TB) | sehr groß (praktisch >> TB) |
| **Journaling** (Änderungsprotokoll für Crash-Konsistenz) | ✗ | ✗ | ✓ | ✓ | ✓ (Copy-on-Write) |
| **Rechte/ACLs** (steuern, **wer** lesen/schreiben/ausführen darf) | ✗ | ✗ | ✓ | ✓ (POSIX/ACL) | ✓ |
| **Plattform-Kompatibilität** | Breite Geräte-Kompatibilität | Breite OS-/Geräte-Kompatibilität | Windows nativ; Linux/macOS mit Treibern/Read-Only | Linux nativ; andere OS teils nur mit Tools | Apple-Geräte nativ |
| **Besonderheiten** | Einfache Struktur, schnell, aber limitiert | Guter Mittelweg für große Dateien auf Wechseldatenträgern | MFT, EFS, BitLocker-Support, Quotas | Extents, HTree-Verzeichnisse | Snapshots, Verschlüsselung, SSD-optimiert |


!!! tip "Schnellauswahl"
    - **USB/SD zwischen Windows & macOS:** *exFAT*  
    - **Windows-System/Arbeits-SSD:** *NTFS*  
    - **Linux-System/Server:** *ext4* (oder XFS/Btrfs je nach Bedarf)  
    - **Apple-Geräte:** *APFS*

## Genutzte Allocationtypen

| Speicherstrategie        | Prinzip                                                                 | Typische Dateisysteme                              | Bemerkungen                                                                                     |
|--------------------------|-------------------------------------------------------------------------|----------------------------------------------------|-------------------------------------------------------------------------------------------------|
| **Contiguous Allocation** (zusammenhängend) | Jede Datei liegt in einem durchgehenden Blockbereich auf dem Datenträger. | Sehr alte Systeme (z. B. frühe CP/M, einfache Embedded-Dateisysteme) | Einfach, schnelle Zugriffe, aber **Fragmentierung**-Probleme. In modernen Dateisystemen kaum genutzt. |
| **Chained Allocation** (verkettet)          | Datei besteht aus Blöcken, die jeweils einen Zeiger auf den nächsten Block enthalten (wie eine verkettete Liste). | **FAT12/16/32** (File Allocation Table) | FAT speichert die Ketten in einer separaten Tabelle („FAT“). Vorteil: keine externe Fragmentierung, Nachteil: langsamer zufälliger Zugriff. |
| **Indexed Allocation** (indiziert)          | Jede Datei hat eine Index-Struktur (z. B. Inode), die die Blockadressen enthält. | **UFS**, **ext2/3/4**, **NTFS**, **XFS**, **Btrfs**, **ZFS**, **APFS** | Sehr flexibel, erlaubt große Dateien, einfacher Direktzugriff. Praktisch Standard in modernen Dateisystemen. |

## Praxis: Eigenes System prüfen (nur lesend)

=== "Windows (PowerShell)"
    ```powershell
    Get-Volume | Select DriveLetter, FileSystem, FileSystemLabel, Size, SizeRemaining
    ```
=== "Linux"
    ```bash
    lsblk -f
    # oder
    df -T
    ```
=== "macOS"
    ```bash
    diskutil list
    diskutil info /Volumes/DeinVolume
    ```