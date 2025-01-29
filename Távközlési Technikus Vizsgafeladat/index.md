# MÉRÉSI JEGYZŐKÖNYV

**A mérést végző neve:** Oláh Bence  
**A mérés tárgya:** komplex távközlési hálózat építési feladat


**A mérés száma:** 8. mérés  
**A mérés dátuma:** 2025. 01. 29  
**A mérést vezette:** Sándor Péter  

**Évfolyam:** 13. E  
**Csoport:** GYAK 2  
**Helyszín:** V3 Labor 

---
# Mérési Jegyzőkönyv: Komplex Távközlési Hálózat Tervezése, Telepítése és Mérése

**Időtartam:** 2 óra  

## 1. Eszközök és Beállítások

### Eszközök

| Eszköz | Típus |
|--------|-------------------------------|
| Mikrotik LHG18 LTE | LTE antenna |
| Mikrotik nRay 60GHz | Mikrohullámú antennák |
| SOHO router |  ASUS |
| Laptop vagy PC | Hálózati teszteléshez |
| HP Switch | (opcionális) |
| iperf szoftver | Sávszélesség méréshez |

### Eszközök IP-címek

| Eszköz | IP-cím |
|--------|----------------|
| Mikrotik LHG18 LTE | 192.168.88.1 |
| Mikrotik nRay 60GHz Master | 192.168.88.2 |
| Mikrotik nRay 60GHz Slave | 192.168.88.3 |
| Router (AP mód) | 192.168.88.4 |
| Switch (opcionális) | 192.168.88.254 |
| Kliens laptop | 192.168.88.100-250 (DHCP) |

**Alhálózati maszk:** 255.255.255.0  

## 2. Hálózati Tesztelés Eredményei

### 2.1. Mikrotik LHG18 LTE Antenna Jelerősségi Paraméterei

| Paraméter | Érték |
|-----------|--------|
| RSRP (Reference Signal Received Power) | [-80dBm] |
| RSRQ (Reference Signal Received Quality) | [-130dB] |
| SINR (Signal to Interference plus Noise Ratio) | [21dB] |
| RSSI (Received Signal Strength Indicator) | [-49dB] |

### 2.2. Ping Teszt Eredményei

| Cél IP cím | Válaszidő (ms) | Csomagok (sikeres/sikertelen) |
|------------|---------------|-------------------------------|
| 192.168.88.1 | [Érték] | [Érték] |
| 192.168.88.2 | [Érték] | [Érték] |
| 192.168.88.3 | [Érték] | [Érték] |
| 192.168.88.4 | [Érték] | [Érték] |

### 2.3. Sávszélesség Mérési Eredmények (iperf3)

| Forrás IP | Cél IP | Sávszélesség (Mbps) | Eredmény |
|-----------|--------|---------------------|----------|
| [Laptop IP] | 192.168.88.xxx | [Érték] | [Érték] |
| [Laptop IP] | 192.168.88.xxx | [Érték] | [Érték] |

### 2.4. Internet Elérés Teszt

- **Ping Teszt (8.8.8.8):**
  - Válaszidő: [Érték] ms
  - Csomagok: [Érték] sikeres / [Érték] sikertelen
- **Speedtest eredmény:**
  - Letöltési sebesség: [Érték] Mbps
  - Feltöltési sebesség: [Érték] Mbps

## 3. Eszközök Állapotának Ellenőrzése

### 3.1. Mikrotik nRay 60GHz Antennák Kapcsolati Állapot

| Eszköz | Status | Kapcsolati minőség |
|--------|--------|---------------------|
| Master antenna (192.168.88.2) | [90] | [7] |
| Slave antenna (192.168.88.3) | [90] | [7] |

## 4. Hibakeresési Eredmények

- **Tűzfal engedélyezés:**
  - Hálózati felfedezés engedélyezve: [Igen]
- **DHCP és IP-címek ellenőrzése:**
  - DHCP szerver működése: [Ige]
  - Megújított IP-címek: [Érték]

---

**Aláírás:**  
**Név:*Oláh Bence*  
**Dátum:*2025.01.29*  




