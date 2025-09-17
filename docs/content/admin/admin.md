# Aufgaben eines Systemadministrators im Betrieb

Systemadmins stellen sicher, dass IT-Systeme stabil, sicher und performant laufen. Sie betreiben Infrastruktur (Server, Netzwerk, Clients, Cloud), automatisieren Routineaufgaben, unterstützen Nutzer und setzen Sicherheits-/Compliance-Vorgaben um.

## Beispiele aus der Wirtschaft

{{ youtube_video("https://www.youtube.com/embed/z_3t9DZWa7w?si=EqlPtI_CdqEeNb4r") }}

{{ youtube_video("https://www.youtube.com/embed/OQIIHKusBIM?si=9vCrJGQQxzGRjw1Z")}}

{{ youtube_video("https://www.youtube.com/embed/1Ro5P0HU4kY?si=1yX1F3svbszdUw1G")}}

??? info "Text"

    [:fontawesome-solid-external-link: Interview bei sheer imc](https://www.scheer-imc.com/de/blog/artikel/job-it-system-administrator/){ target=_blank rel="noopener noreferrer" }

## Kernaufgaben

### Betrieb & Wartung
- Server/Clients bereitstellen (Imaging, MDM), Patch-/Update-Management, Treiber-/Firmwarepflege
- Benutzer- und Rechteverwaltung (AD/Entra, Gruppen, GPOs, SSO)
- Datei-, Druck-, Mail-, Kollaborationsdienste (z. B. M365/Google Workspace)
- Virtualisierung & Container (VMware/Hyper‑V/Proxmox; Docker/K8s)
- Lifecycle-Aufgaben nach IMAC/R/D (Install, Move, Add, Change, Remove, Dispose) inkl. sicherer Datenlöschung/Refurbishing [Q1].

### Netzwerk
- LAN/WLAN/VPN einrichten und pflegen (Switching, VLANs, DHCP/DNS, Firewall/UTM)
- Performance-/Verfügbarkeitsüberwachung, Troubleshooting (Latenz, Paketverlust)

### Sicherheit
- Endpoint-/Server-Security (AV/EDR), Härtung, MFA, Least‑Privilege
- Schwachstellen-/Patch-Management, Log-/SIEM-Auswertung, Incident Response
- Backup/Restore testen (RPO/RTO), Offsite/immutable Backups
- Informationssicherheit & IAM organisatorisch verankern [Q9].

### Monitoring & Verfügbarkeit
- Monitoring/Alerting (z. B. Zabbix, PRTG, Prometheus) einrichten
- Kapazitätsplanung (Storage, CPU/RAM, Lizenzen), Trendanalysen
- APM/EUEM einsetzen (synthetisch, Real‑User‑Monitoring, JS‑Injection, Device‑Monitoring) [Q2].
- Monitoring‑Domänen abdecken: Server/OS, Netzwerk/Firewall/DHCP/DNS, DB, Cloud/Container, Security, Umgebungsfaktoren [Q3].
- Wartungsstrategien von reaktiv/periodisch zu präventiv/prädiktiv entwickeln (Analytics, KI‑gestützte Warnungen) [Q2].

### Automatisierung & Scripting
- Skripte/Playbooks (PowerShell, Bash, Python, Ansible) für Deployments, Checks, On‑/Offboarding
- Standard‑Konfigurationen per IaC/Policy (GPO, Intune, Ansible)
- Change-/Release‑Workflow: RFC erfassen/bewerten/freigeben/implementieren; Change‑Management klar definieren [Q4].

### Support & Collaboration
- 2nd-/3rd‑Level‑Support, Ticket-/SLA‑Bearbeitung, Wissensdatenbank pflegen
- Servicedesk als SPOC, ACD/Multichannel‑Annahme; Tickets sauber erfassen/klassifizieren [Q5].
- Standardprozesse: Incident, Service Request, Problem, Change; CMDB/Configuration‑Management nutzen [Q6].
- Ticket‑Flow & Eskalation (Kategorisierung, Priorität, SLA, RFC) definieren [Q7].
- Rollen/Verantwortungen via RACI festlegen; Service Owner/Case Owner benennen [Q8].

### Prozesse, Compliance & Dokumentation
- Change-/Release-/Problem‑Management (ITIL‑orientiert), Doku, Notfallhandbuch/Runbooks
- Asset‑, Lizenz‑ und Vertragsmanagement
- Datenschutz/ISO/BCM‑Vorgaben umsetzen, Audit‑Vorbereitung
- Service‑Portfolio‑ & Service‑Catalogue‑Management; Service‑Level‑Management mit SLA/OLA/UC [Q9][Q10].

### Projekte
- System-/Cloud‑Migrationen, Rollouts, Standorteröffnungen
- Evaluierung neuer Tools, PoCs, Kosten‑/Nutzen‑Analysen

## Tagesablauf (Beispiel)
1. **Morgens:** Monitoring‑Alarme & Tickets sichten, Prioritäten setzen
2. **Vormittags:** Patches/Deployments in Test, kleinere Changes, Rechtevergaben, Onboardings
3. **Nachmittags:** Projektarbeit (Migration, Automatisierung), Troubleshooting komplexer Fälle
4. **Später:** Doku aktualisieren, Backups/Jobs prüfen, Übergabe an Bereitschaft

## Regelmäßige Routinen (Kurz‑Checkliste)
- **Täglich:** Alarme & Backups prüfen, kritische Tickets, AV/EDR‑Status
- **Wöchentlich:** Patches testen/ausrollen, Reports (Verfügbarkeit, Kapazität), DR‑Stichproben
- **Monatlich:** Schwachstellen‑Scan, Recovery‑Tests, Lizenz‑/Asset‑Abgleich
- **Quartalsweise:** Notfallübung, IAM‑Rezertifizierung, Architektur‑Review

## Wichtige Skills & Tools
- Windows/Linux‑Admin, AD/Entra, M365/Exchange, Virtualisierung, Netzwerk‑Know‑how
- PowerShell/Bash, Automatisierung/IaC, Monitoring/SIEM, Backup‑Suiten
- Saubere Doku, Ticketing (Jira/GLPI/ServiceNow), ITIL‑Grundlagen

## KPIs (Beispiele)
- **Reaktionszeiten am Servicedesk** verbindlich kommunizieren und messen [Q11].
- **Verfügbarkeit/Uptime** über Availability‑Management definieren und reporten [Q9].
- **Kontinuierliche Verbesserung** (PDCA/CSI) mit KPI‑Analysen verankern [Q9].

## Unterschiede nach Unternehmensgröße
- **KMU:** Generalist – „End‑to‑End“ zuständig (Server, Netzwerk, Cloud, Support).
- **Konzern:** Spezialisierung (z. B. IAM, Netzwerk, Endpoint, Cloud), klare ITIL‑Prozesse.
- **MSP‑Setups:** Services per SLA, proaktives Remote‑Monitoring/Wartung aus dem Servicedesk heraus [Q12].

---

## Quellenhinweise (für dein internes Doku‑Archiv)
Alle Verweise beziehen sich auf: *Westermann, IT‑Berufe Fachstufe, Lernfelder 6–9 (PDF-Ausgabe).*

- **[Q1] IMAC/R/D‑Lebenszyklus** – Lernfeld 6 „Serviceanfragen bearbeiten“, Abschnitt *IT‑Phasen im IMAC/R/D‑Lebenszyklus* (S. 14 ff.).
- **[Q2] APM/EUEM & Wartungsstrategien** – Lernfeld 6, *APM & EUEM (Synthetisch, RUM, JS‑Injection, Device)* und Überblick *Reaktiv/Periodisch/Präventiv/Prädiktiv* (S. 70–71).
- **[Q3] Monitoring‑Domänen & Beispiele** – Lernfeld 6, *Infrastruktur‑Monitoring* (Server/Netz/Dienste/Umwelt, inkl. Cloud/Container/Security) (S. 51 ff.).
- **[Q4] Change‑Management/RFC‑Ablauf** – Lernfeld 6, *Change‑Fälle analysieren* und Servicedesk‑Prozessübersicht (S. 41 ff.).
- **[Q5] SPOC, ACD, Servicedesk‑Begriffe** – Lernfeld 6, *Erstkontaktaufnahme von Services* (S. 34–36). 
- **[Q6] Standardprozesse & CMDB** – Lernfeld 6/9, *Servicedesk‑Basisprozesse* und *Configuration‑Management* (S. 41 ff.,  — CMDB in Service‑Prozessübersicht S. …/Kontext in LF 9).
- **[Q7] Ticket‑Flow & Eskalation** – Lernfeld 6, *Abläufe der Service‑Basisprozesse* (S. 41 ff.).
- **[Q8] RACI‑Matrix & Rollen** – Lernfeld 6, *R‑A‑C‑I* inkl. Rollen/Zuordnung (S. 34–36).
- **[Q9] Service‑Portfolio/-Katalog, SLM, Capacity/Availability/Continuity, ISMS** – Lernfeld 6, *Service‑Management‑Prozesse* (S. … um S. 59 ff.).
- **[Q10] SLA/OLA/UC‑Definitionen** – Lernfeld 6, *Vertragsarten der Servicebeteiligten* (S. 26–27).
- **[Q11] Reaktionszeiten/Kundenkommunikation** – Lernfeld 6, *Serviceanalyse & Ticketdaten/Vertragsbasis* (S. 34 ff.) sowie *Prioritäts-/Klassenübersicht* (S. 41 ff.).
- **[Q12] MSP/Remote‑Services** – Lernfeld 6, *Cloud‑/Remote‑Bearbeitung aus dem Servicedesk* und Begriffsübersicht (MSP) (S. 34 ff., 14 ff.).
