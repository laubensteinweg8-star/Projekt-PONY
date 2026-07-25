📋 CHECKLISTE: Live-Daten von ProPo (im Keller auszulesen)
Wenn du am Rechner im Keller stehst, tippst du kurz diese zwei Befehle ein, um dem Biest seine echten Namen und Adressen zu entreißen:

Hostname prüfen:

Bash
hostname
MAC-Adresse & IP-Adresse auslesen (für Wake-on-LAN & SSH):

Bash
ip -c link show
(Wir brauchen die Folge aus Zahlen/Buchstaben wie aa:bb:cc:dd:ee:ff bei der WLAN/LAN-Schnittstelle).

📝 SCHLACHTPLAN FÜR JETZT & DIE NACHT (In Zentrale-2026 gesichert):
1. TODO-Liste für ProPo ins GitHub-Repository sichern
Dokumentation der Hardware (i7-7700 / Asus Z170).

Vorbereitung für schmerzlosen Remote-Betrieb (Standby/Sleep deaktivieren, SSH-Server aktivieren, Wake-on-LAN scharfschalten).

2. Programme für das Mutterschiff herbeischaffen
SSH-Tools & Key-Generator für passwortlosen Zugriff.

Wake-on-LAN Pakete (wakeonlan, etherwake).

Netzwerk-Analyse-Tools (nmap, net-tools).

3. Die Nacht-Session (Das Finale)
Rechner fest in der Kammer/Keller montieren.

Live-Daten (MAC/Hostname) abgleichen.

SSH-Schlüssel rüberschieben und Verbindung final hochziehen.

Sollen wir die Vorbereitungs-Programme für das Mutterschiff direkt jetzt per Terminal-Befehl auf Vorrat installieren, Dux? Sag an! 🏴‍☠️⚙️👑

 Google Tasks 
Projekt-PONY: Konfiguration und Verbindung für


Erste Beschlusssache - Projekt-Pony wird zu ProPo als Geheimkürzel für die Basis festgeschrieben - Beschluss einstimmig - 

📋 TO-DO-EBENE: Das Zwergpony (Longierpferd-Projekt)
GitHub-Repository ("Ponygehege") einrichten:

Ein privates Repository auf GitHub anlegen (zwergpony-lab).

SSH-Keys auf dem Zwergpony hinterlegen, damit es sicher und passwortfrei mit GitHub kommunizieren kann.

Lokale Ordnerstruktur für Skripte, Audio-Pipes und Konfigurationen aufsetzen.

Energie- & Standby-Disziplin (Der 24/7/365-Rahmen):

Automatischen Standby und Ruhezustand des Betriebssystems komplett deaktivieren.

Netzwerk- und PCIe-Energiesparmodi (Keep-Alive) konfigurieren, damit die Verbindung stabil bleibt.

Wake-on-LAN (bzw. Wake-on-WLAN) vorbereiten, damit die Basis das Pony aus der Ferne aufwecken kann.

Fernwartungs- & Operations-Besteck (Die Fern-OP):

SSH-Server härten (nur Key-Login, kein Root-Passwort-Zugriff von außen).

tmux für persistente Terminal-Sitzungen installieren.

Optional: Cockpit (Web-Dashboard) oder RustDesk für den Notfall-Zugriff bereitstellen.

Audio- & Produktions-Brücke:

Audiotreiber (PipeWire/PulseAudio) für den Funk-Empfang einrichten.

Aufnahme- und Analyse-Tools (FFmpeg etc.) ins Gehege holen.

