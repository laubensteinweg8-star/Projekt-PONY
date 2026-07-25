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

