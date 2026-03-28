![Marino Lab Banner](docs/screenshots/marinolab_banner.png)

# 🚗 CarDash System
### Android Infotainment & Phone Gateway

> Trasforma il tuo smartphone e un tablet in un sistema di infotainment professionale per l'auto — senza modifiche hardware.

[![Version](https://img.shields.io/badge/version-1.0-cyan?style=flat-square)](https://github.com/stramari/MarinoLab/releases/latest)
[![Android](https://img.shields.io/badge/Android-5.0%2B-green?style=flat-square&logo=android)](https://github.com/stramari/MarinoLab/releases/latest)
[![License](https://img.shields.io/badge/licenza-Trial%207gg%20%7C%20Full-orange?style=flat-square)](https://marinolab.lemonsqueezy.com/)
[![Download](https://img.shields.io/badge/⬇%20Download-APK-blue?style=flat-square)](https://github.com/stramari/MarinoLab/releases/latest)
[![Lingua](https://img.shields.io/badge/lingua-%F0%9F%87%AE%F0%9F%87%B9%20Italiano%20%7C%20%F0%9F%87%AC%F0%9F%87%A7%20English-lightgrey?style=flat-square)](https://github.com/stramari/MarinoLab)

---

## 📸 Anteprima

### Dashboard Principale (Tablet)
> Tachimetro digitale, radio attiva, scorciatoie alle app e salvataggio parcheggio — tutto in un colpo d'occhio.

![Dashboard Principale](docs/screenshots/dashboard_main.png)

### Google Maps + Floating Sidebar
> Il tablet usa il GPS del telefono per navigare con Google Maps o Waze — anche senza GPS hardware. La barra laterale flottante rimane sempre accessibile.

![Google Maps con sidebar](docs/screenshots/maps_floating.png)

### Radio Web Integrata
> Migliaia di stazioni italiane e mondiali, preferiti e controlli play/pausa — tutto senza uscire dalla dashboard.

![Modulo Radio](docs/screenshots/radio.png)

### Gestione Chiamate
> Tastierino e rubrica sincronizzata direttamente dal telefono, ottimizzati per la guida.

![Telefono e Rubrica](docs/screenshots/telefono.png)

### Salva Parcheggio (Dialogo Tablet)
> Il sistema mostra la precisione GPS in tempo reale e ti avvisa se il segnale è scarso prima di salvare.

![Salva Parcheggio Tablet](docs/screenshots/parking_tablet.png)

---

### App Server (Smartphone)

| Pannello Principale | Salva Parcheggio | Guida Bussola |
|---|---|---|
| ![Server Main](docs/screenshots/server_main.jpg) | ![Server Parking](docs/screenshots/server_parking.jpg) | ![Bussola](docs/screenshots/compass.jpg) |

> La **Guida Bussola** ti indica la direzione e la distanza esatta dalla tua auto parcheggiata.

### Attivazione Licenza
![Licenza](docs/screenshots/license.jpg)

---

## ✨ Funzionalità Principali

### 📱 App Server — sul tuo smartphone
- **Gateway TCP/UDP** — trasmette GPS, velocità e notifiche al tablet in tempo reale
- **Mirroring notifiche** — WhatsApp, Maps e altre app appaiono sulla dashboard
- **Gestione chiamate** — avvio chiamate anche sopra il lock screen
- **Parking Tracker** — salva la posizione con precisione metrica e ti riporta all'auto tramite bussola grafica

### 🖥️ App Bridge — sul tablet in auto
- **Tachimetro digitale** — velocità in km/h con stato GPS e connessione server
- **Mock GPS** — inietta il segnale del telefono nel tablet, abilitando Google Maps e Waze anche senza GPS hardware
- **Radio Web** — migliaia di stazioni via Radio-Browser API con gestione preferiti
- **Floating Sidebar** — barra laterale sempre visibile con controlli rapidi
- **Discovery automatica** — si connette al telefono non appena riconosce l'hotspot Wi-Fi

---

## 🚀 Come Iniziare

### Requisiti
- Uno **smartphone Android** (minSdk 21 / Android 5.0+) con SIM
- Un **tablet Android** (o autoradio Android) da montare in auto
- Una connessione Wi-Fi condivisa dallo smartphone (hotspot)

### Installazione — 3 passi

**1. Scarica le app**

| App | Dispositivo | Link |
|---|---|---|
| `CarDash Server` | 📱 Smartphone | [⬇ Download APK](https://github.com/stramari/MarinoLab/releases/latest) |
| `CarDash Bridge` | 🖥️ Tablet | [⬇ Download APK](https://github.com/stramari/MarinoLab/releases/latest) |

**2. Concedi i permessi**

Entrambe le app guidano l'utente tramite un flow interattivo per i permessi necessari (overlay, notifiche, posizione, chiamate). Ogni permesso è spiegato con il motivo per cui serve.

**3. Connetti**

Attiva l'hotspot Wi-Fi sullo smartphone → avvia CarDash Server → avvia CarDash Bridge sul tablet. La connessione avviene in automatico.

---

## 🔑 Licenza & Prezzi

Il sistema include un **trial gratuito di 7 giorni** con tutte le funzionalità attive. Nessuna carta di credito richiesta.

Al termine del trial, puoi acquistare la licenza full su:

👉 **[marinolab.lemonsqueezy.com](https://marinolab.lemonsqueezy.com/)**

**Non è necessario scaricare o reinstallare nulla.** Dopo l'acquisto riceverai una mail con la tua chiave di licenza nel formato `XXXX-XXXX-XXXX-XXXX`. Inseriscila nell'app Server alla voce **"Attiva Licenza"** — verrà sincronizzata automaticamente anche sul tablet.

> ⚠️ **Anti-reset**: il sistema di protezione del trial è progettato per resistere a reset della data o reinstallazioni.

---

## ❓ FAQ

**Il tablet ha bisogno del GPS?**
No. CarDash inietta il segnale GPS del telefono nel sistema Android del tablet, permettendo l'uso di Google Maps e Waze anche su tablet senza GPS hardware.

**Funziona con qualsiasi tablet Android?**
Sì, da Android 5.0 in poi. Ottimizzato per l'uso in orizzontale.

**Perché servono tutti quei permessi?**
Ogni permesso ha uno scopo preciso: l'overlay serve per la sidebar flottante sopra Maps, le notifiche per il mirroring, la posizione per il GPS e il parking tracker, le chiamate per il tastierino. Nessun dato viene inviato a server esterni.

**Funziona senza connessione internet?**
La dashboard, il tachimetro, le chiamate e il parking tracker funzionano completamente offline. La radio web e il controllo aggiornamenti richiedono internet.

**Come ricevo gli aggiornamenti?**
L'app controlla automaticamente la presenza di nuove versioni su GitHub all'avvio e mostra una notifica con il changelog se disponibile.

---

## 📡 Protocollo di Comunicazione

| Porta | Protocollo | Uso |
|---|---|---|
| `8080` | TCP | Comandi, rubrica, notifiche, licenza |
| `8888` | UDP | Beacon discovery, telemetria GPS |

| Comando | Descrizione |
|---|---|
| `GPS_DATA` | Telemetria completa (Lat, Lon, Vel, Alt) |
| `SPEED:VAL:ST` | Velocità e stato connessione |
| `INCOMING` | Chiamata in entrata con nome contatto |
| `LICENSE_SYNC` | Sincronizzazione licenza tra dispositivi |
| `GET_CONTACTS` | Recupero rubrica dal tablet |
| `NOTIFICATION` | Mirroring notifiche app terze |

---

## 🏗️ Architettura del Progetto

Il progetto è un sistema **multi-modulo Gradle**:

- **`:app-server`** — Foreground Service con beacon UDP, server TCP, telemetria GPS e listener notifiche
- **`:app-bridge`** — UI ottimizzata per la guida con mock GPS, radio Media3/ExoPlayer e floating sidebar
- **`:common`** — Libreria condivisa con `LicenseManager` e costanti di comunicazione

**Stack tecnico:** Kotlin · Android SDK 36 · Media3/ExoPlayer · Radio-Browser API · Lemon Squeezy

---

## 🛠️ Build & Release

### Requisiti di sviluppo
- Android Studio Hedgehog o superiore
- Android SDK minSdk 21, targetSdk 36
- Foreground Service Types dichiarati: `connectedDevice`, `location`, `mediaPlayback`

### Rilasciare un aggiornamento

1. `Build > Generate Signed Bundle / APK` → seleziona il modulo → modalità **Release**
2. I file si trovano in `app-bridge/release` e `app-server/release`
3. Su GitHub vai su **Releases → Create a new release**, crea un tag (es. `v1.1`) e allega i file:
   - `cardash_server.apk`
   - `cardash_client.apk`
4. Modifica `cardash/version.json` incrementando `versionCode` e aggiornando `changelog`
5. Al prossimo avvio, gli utenti ricevono la notifica di aggiornamento automatica

---

## 📂 Struttura Screenshot

Per visualizzare correttamente le immagini in questo README, carica gli screenshot nella seguente struttura:

```
docs/
└── screenshots/
    ├── marinolab_banner.png     ← Banner Marino Lab (in cima al README)
    ├── dashboard_main.png       ← Dashboard principale tablet
    ├── maps_floating.png        ← Google Maps + floating sidebar
    ├── radio.png                ← Modulo radio
    ├── telefono.png             ← Tastierino + rubrica
    ├── parking_tablet.png       ← Dialogo salva parcheggio (tablet)
    ├── server_main.jpg          ← Pannello principale server
    ├── server_parking.jpg       ← Salva parcheggio server
    ├── compass.jpg              ← Guida bussola
    └── license.jpg              ← Schermata attivazione licenza
```

---

**Sviluppato da [Marino Lab](https://marinolab.lemonsqueezy.com/) · CarDash System v1.0 · Ultimo aggiornamento: 28 Marzo 2026**
