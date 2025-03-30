Dieses Repository enthält die Konfiguration und Dokumentation für eine containerisierte Bereitstellung der Open-Source Fotoverwaltungsplattform [Immich](https://github.com/immich-app/immich).  
Die Umsetzung erfolgte im Rahmen des Moduls **LB169 – Services mit Containern bereitstellen**.

---

## 🔧 Setup

1. Repository klonen:
```bash
git clone https://github.com/sid00123/SchnyderSidenyLB-169.git
cd SchnyderSidenyLB-169
```

2. `.env` Datei vorbereiten:
```bash
cp example.env .env
```

3. Container starten:
```bash
docker compose -d
```

---

## ⚙️ Dienste & Architektur

| Container                 | Beschreibung                                            |
|--------------------------|---------------------------------------------------------|
| `immich-server`          | Web-GUI & API unter http://localhost:2283              |
| `immich-machine-learning`| Gesichts- und Objekterkennung                          |
| `redis`                  | Zwischenspeicher & Sessionverwaltung                   |
| `database` (PostgreSQL)  | Persistente Speicherung der Metadaten                  |

---

## 📂 Verzeichnisstruktur

- `docker-compose.yml` → Container-Definitionen
- `.env.example` → Vorlage für Umgebungsvariablen
- `library/` → Upload-Ordner für Bilder und Videos
- `postgres/` → Volume für PostgreSQL-Datenbank

---

## ✅ Testfälle

- ✔️ Webzugriff auf Immich
- ✔️ Upload und Anzeige eines Bildes
- ✔️ Erstellung eines Albums
- ✔️ Generierung eines Sharing-Links
- ✔️ Daten bleiben nach Neustart erhalten

---

## 📃 Lizenz & Autor

Dieses Projekt wurde im Rahmen der Leistungsbeurteilung LB169 erstellt.  
© 2025 Sidney Schnyder
