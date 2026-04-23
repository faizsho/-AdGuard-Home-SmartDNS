# 🛡️ AdGuard Home + SmartDNS Optimization (Ubuntu 22.04)

Dokumentasi ini berisi panduan instalasi dan konfigurasi optimasi DNS menggunakan **AdGuard Home** sebagai frontend (Filtering) dan **SmartDNS** sebagai backend (Speed/Racing Upstream).

## 🚀 Mengapa Kombinasi Ini?
- **AdGuard Home:** UI yang luar biasa untuk memantau trafik, manajemen client, dan filter iklan/malware yang sangat mudah.
- **SmartDNS:** Mesin DNS paling efisien untuk melakukan *racing* (mencari upstream tercepat) secara paralel dan manajemen cache tingkat tinggi.

## 🏗️ Arsitektur Jaringan
`Client` -> `AdGuard Home (Port 53)` -> `SmartDNS (Port 5353)` -> `Internet (DoH/DoT Upstreams)`

---

## 🛠️ Langkah Instalasi

### 1. Update Sistem & Tool Dasar
```bash
sudo apt update && sudo apt install curl wget tar -y
