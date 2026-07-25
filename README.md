📋 TO-DO-EBENE: Das Zwergpony (ProPo)
GitHub-Repository ("Ponygehege") einrichten:

Privates Repo zwergpony-lab auf GitHub anlegen.

SSH-Keys auf ProPo hinterlegen für sichersten Sync.

Lokale Ordnerstruktur für Skripte, Audio-Pipes und Configs aufsetzen.

Energie- & Standby-Disziplin (24/7-Rahmen):

Automatischen Standby/Ruhezustand komplett deaktivieren.

PCIe-/Netzwerk-Keep-Alive konfigurieren.

Wake-on-LAN scharfschalten.

Fernwartungs- & Operations-Besteck:

SSH-Server härten (nur Key-Login).

tmux für persistente Sitzungen installieren.

Optional: Cockpit/RustDesk als Notfall-Dashboard.

Audio- & Produktions-Brücke:

PipeWire/PulseAudio für Funk-Empfang vorbereiten.

FFmpeg und Analyse-Tools laden.
EOF



cat << 'EOF' > ~/LEGENDE_PROPO.md
# 📜 LEGENDE: PROPO-LAB // KAMMERSYSTEM (24/7-NODE)

## 1. WARUM? (Der Zweck)
* **Auslagerung von Last & Lärm:** Die Kiste (i7-7700 / Asus Z170) wandert in die Kammer/den Keller, damit das Mutterschiff leise und ungestört bleibt.
* **24/7 Dauerläufer & Remote-Knecht:** Für automatisierte Hintergrund-Jobs, Audio-Processing, Downloads, Daten-Pipes und Langzeit-Tests, die durchlaufen müssen, während du schläfst oder Karin Nachtschicht hat.
* **Prozess-Sicherheit:** Durch die Auslagerung bleibt das Hauptsystem immer zu 100% geschmeidig und frei für dein tagesaktuelles Arbeiten.

## 2. WOMIT? (Das Besteck & Die Hardware)
* **ProPo (Zwergpony):** Intel i7-7700 / Asus Z170 / Linux
* **Mutterschiff:** Steuerzentrale (Kubuntu / Ryzen 9 / RTX 4000 Ada)
* **SSH (Public Key):** Passwortlose, vollverschlüsselte Tunnel-Verbindung
* **Wake-on-LAN (`wakeonlan`):** Aufwecken des Ponys aus dem Schlafmodus direkt vom Mutterschiff aus
* **`tmux`:** Persistente Konsolen-Sitzungen (Skripte laufen weiter, selbst wenn SSH trennt)
* **PipeWire / FFmpeg:** Audio-Stream-Vorbereitung für Funk- & Produktions-Signale
* **GitHub (`zwergpony-lab` / `Zentrale-2026`):** Synchrones Logbuch & Code-Ablage für beide Rechner

## 3. WIE? (Der Operations-Ablauf in 4 Phasen)

### Phase 1: Physischer Einbau (Draußen / Kammer)
* ProPo wird in der Kammer verkabelt (Strom + LAN/WLAN).
* Kaltstart & Auslesen der Live-MAC sowie des exakten Hostnamens.

### Phase 2: Die Härtung (24/7-Konfiguration)
* Standby/Sleep im Linux von ProPo komplett killen (`systemctl mask sleep.target`).
* SSH-Server scharfschalten und Root-Passwort-Login sperren (nur Key-Auth).

### Phase 3: Der Mutterschiff-Koppler
* SSH-Key vom Mutterschiff auf ProPo schieben (`ssh-copy-id`).
* Start-Skript auf dem Mutterschiff hinterlegen: `propo-on` weckt auf, wartet auf Ping und klinkt dich per SSH direkt ein.

### Phase 4: Der schmerzfreie Regelbetrieb
* Du sitzt oben am Mutterschiff, tippst `propo-on` und arbeitest in der Kammer, als stünde die Kiste direkt unter deinem Tisch.

---

## 📋 CHECKLISTE: Live-Daten von ProPo (im Keller auszulesen)
```bash
# Hostname prüfen
hostname

# MAC-Adresse & IP-Adresse auslesen (für WoL & SSH)
ip -c link show


📜 LEGENDE: PROPO-LAB // KAMMERSYSTEM (24/7-NODE)1. WARUM? (Der Zweck)Auslagerung von Last & Lärm: Die Kiste (i7-7700 / Asus Z170) wandert in die Kammer/den Keller, damit das Mutterschiff leise und ungestört bleibt.24/7 Dauerläufer & Remote-Knecht: Für automatisierte Hintergrund-Jobs, Audio-Processing, Downloads, Daten-Pipes und Langzeit-Tests, die durchlaufen müssen, während du schläfst oder Karin Nachtschicht hat.Prozess-Sicherheit: Durch die Auslagerung bleibt das Hauptsystem immer zu 100% geschmeidig und frei für dein tagesaktuelles Arbeiten.2. WOMIT? (Das Besteck & Die Hardware)Komponente / ToolRolle & ZweckProPo (Zwergpony)Intel i7-7700 / Asus Z170 / LinuxMutterschiffSteuerzentrale (Kubuntu / Ryzen 9 / RTX 4000 Ada)SSH (Public Key)Passwortlose, vollverschlüsselte Tunnel-VerbindungWake-on-LAN (wakeonlan)Aufwecken des Ponys aus dem Schlafmodus direkt vom Mutterschiff austmuxPersistente Konsolen-Sitzungen (Skripte laufen weiter, selbst wenn SSH trennt)PipeWire / FFmpegAudio-Stream-Vorbereitung für Funk- & Produktions-SignaleGitHub (zwergpony-lab)Synchrones Logbuch & Code-Ablage für beide Rechner3. WIE? (Der Operations-Ablauf in 4 Phasen)Phase 1: Physischer Einbau (Draußen / Kammer)ProPo wird in der Kammer verkabelt (Strom + LAN/WLAN).Kaltstart & Auslesen der Live-MAC sowie des exakten Hostnamens.Phase 2: Die Härtung (24/7-Konfiguration)Standby/Sleep im Linux von ProPo komplett killen (systemctl mask sleep.target).SSH-Server scharfschalten und Root-Passwort-Login sperren (nur Key-Auth).Phase 3: Der Mutterschiff-KopplerSSH-Key vom Mutterschiff auf ProPo schieben (ssh-copy-id).Start-Skript auf dem Mutterschiff hinterlegen: propo-on weckt auf, wartet auf Ping und klinkt dich per SSH direkt ein.Phase 4: Der schmerzfreie RegelbetriebDu sitzt oben am Mutterschiff, tippst propo-on und arbeitest in der Kammer, als stünde die Kiste direkt unter deinem Tisch.

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

