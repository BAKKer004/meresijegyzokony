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

## 1. Előkészítés és Tervezés

### 1.1. Eszközök gyári beállításainak visszaállítása (Factory Reset)

#### Mikrotik LHG18 LTE Antenna Resetelése
- Húzza ki az eszközt a tápellátásból.
- Nyomja meg és tartsa lenyomva a reset gombot.
- Csatlakoztassa vissza a tápellátást, miközben továbbra is nyomva tartja a reset gombot.
- Tartsa lenyomva a gombot, amíg a status LED villogni nem kezd (kb. 5 másodperc).
- Engedje el a gombot, az eszköz visszaáll a gyári beállításokra.

#### Mikrotik nRay 60GHz Antennák Resetelése
- Ismételje meg a fent leírt folyamatot mindkét antennán (192.168.88.2 és 192.168.88.3).

#### SOHO Router Resetelése
- Keresse meg a reset gombot az eszközön.
- Áramtalanítás után nyomja be a reset gombot.
- Kapcsolja vissza az eszközt és tartsa lenyomva kb. 10 másodpercig, amíg a gyári visszaállítás folyamat lezajlik.

### 1.2. Hálózati Topológia Tervezése
- **Használt eszközök és IP-címek:**
    - **Mikrotik LHG18 LTE:** 192.168.88.1
    - **Mikrotik nRay 60GHz Master:** 192.168.88.2
    - **Mikrotik nRay 60GHz Slave:** 192.168.88.3
    - **Router (AP mód):** 192.168.88.4
    - **Switch (opcionális):** 192.168.88.254
    - **Kliens laptop:** 192.168.88.100-250 (DHCP-ből)
- **Alhálózati maszk:** 255.255.255.0
- **Hálózati diagram:** Készítse el a diagramot a Draw.io eszközzel.

---

## 2. Eszközök Telepítése és Konfigurálása

### 2.1. Mikrotik LHG18 LTE Antenna Beállítása

- **Csatlakozás az eszközhöz:** 
    - Csatlakoztassa a laptopot Ethernet kábellel.
    - Laptop IP: 192.168.188.2, Alhálózati maszk: 255.255.255.0, Átjáró: 192.168.188.1
- **Böngésző / WinBox belépés:** 
    - Cím: [http://192.168.188.1](http://192.168.188.1)
    - Felhasználónév: admin, jelszó: antennán
- **Konfigurálás:**
    - Állítsa be az LTE kapcsolatot a szolgáltató APN beállításaival.
    - Beállítások: IP: 192.168.88.1, DHCP: 192.168.88.100-250, alhálózati maszk: 255.255.255.0.
    - Mentse a beállításokat és ellenőrizze a kapcsolatot.
    - Végezzen ping tesztet a külső szerverhez (8.8.8.8) és mérje a késleltetést.
- **Jelerősség paraméterek:** 
    - Rögzítse a jelerősségi paramétereket (RSRP, RSRQ, SINR, RSSI).

### 2.2. Mikrotik nRay 60GHz Antennák Beállítása

#### Master Antenna (192.168.88.2) Beállítása
- **Csatlakozás:** Csatlakoztassa Ethernet kábellel.
- **Böngésző / WinBox belépés:** 
    - Cím: [http://192.168.88.2](http://192.168.88.2)
    - Felhasználónév: admin, jelszó: antennán
- **Beállítások:**
    - Állítsa be az eszközt “Master” módban.
    - Ellenőrizze az IP-t, hogy a Slave antenna csatlakozni tudjon.

#### Slave Antenna (192.168.88.3) Beállítása
- **Csatlakozás:** Ismételje meg a fenti lépéseket a Slave antennánál.
- **Beállítások:**
    - Állítsa be az eszközt “Slave” módban, csatlakozzon a Master antennához.

- **Kapcsolat ellenőrzése:** 
    - Ellenőrizze a kapcsolat minőségét (WIRELESS 60G STATUS).
    - Készítsen képernyőképet az aktuális értékekről.

### 2.3. SOHO Router Beállítása AP Módban

- **Csatlakozás:** Csatlakoztassa a routert Ethernet kábellel a laptophoz.
- **IP-cím keresése:** 
    - Használja a `arp -a` parancsot a megfelelő IP-cím megtalálásához.
- **Wi-Fi beállítások:** 
    - SSID: GazdaXX, Jelszó: G1234567 (XX - azonosító szám).
- **Konfigurálás:**
    - Állítsa AP módba az eszközt és manuálisan állítsa be a tartományt (192.168.88.xxx).
    - Ellenőrizze a többi beállítást.

---

## 3. Hálózati Tesztelés és Hibakeresés

### 3.1. Ping Teszt Végrehajtása
- Nyisson parancssort és pingelje meg az eszközöket:
    - `ping 192.168.88.1`
    - `ping 192.168.88.2`
    - `ping 192.168.88.3`
    - `ping 192.168.88.4`
- **Hálózati hiba esetén:**
    - Használja az `ipconfig`, `ipconfig /all`, `ipconfig /release`, `ipconfig /renew` parancsokat.
    - Rögzítse a válaszidőket és a sikeres csomagokat.

### 3.2. Sávszélesség Mérése (iperf használata)
- **Iperf telepítése:**
    - Telepítse az iperf3 szoftvert: `winget install iperf3`
- **Teszt futtatása:**
    - Az egyik laptopon futtassa szerverként: `iperf3 -s`
    - A másikon futtassa kliensként: `iperf3 -c 192.168.88.xxx`
- **Tűzfal beállítása:** 
    - Engedélyezze a szükséges hálózati felfedezést: `netsh advfirewall firewall set rule group="Network Discovery" new enable=Yes`
- **Eredmények rögzítése:** 
    - Rögzítse a sávszélesség mérési eredményeket (Mbps).

---

## 4. Dokumentáció és Értékelés

### Hálózati Forgalom Monitorozása és Hibakeresés
- Használja az iperf szoftvert a sávszélesség mérésére és rögzítse az eredményeket.
- Végezzen ping és traceroute teszteket a hálózati kapcsolatok ellenőrzésére.
- Azonosítson és hárítson el esetleges hálózati hibákat.

### Dokumentáció Készítése
- Készítsen részletes dokumentációt:
    - A hálózati topológia és IP-címek.
    - Eszközök konfigurációs lépései és beállításai.
    - Mérési eredmények és azok elemzése.
    - Hálózati biztonsági beállítások.
    - Hibák és azok elhárításának leírása.

---

**Aláírás:**  
**Név:**  
**Dátum:**  
# Mérési Jegyzőkönyv

## 1. Mérés Célja
 A mikrotik LHG18 antenna és egy SIM-kártya segítségével internetet fogunk és a Mikrotik nRay 60GHz antenna segítségével kihosszabbítjuk a wifi routuerhez,majd az internetet szétsugározzuk a tanterembe  
 
 ---

## 2. Használt Eszközök

| Eszköz                     | Típus                       | Funkció                                           |
|----------------------------|-----------------------------|---------------------------------------------------|
| mikrotik                   | LHG18                       | az inetrenet befogása                             |
| mikrotik                   | nRay 60GHz                  | az internet kihosszabítása a Wifi routerhez       |
| Asus                       | RT-AX58                     | az internet sugárzására                           |

---

## adatok 
| Eszköz                     | Típus                       | Funkció                                           |
|----------------------------|-----------------------------|---------------------------------------------------|
| mikrotik                   | LHG18                       | az inetrenet befogása                             |
| mikrotik                   | nRay 60GHz                  | az internet kihosszabítása a Wifi routerhez       |
| Asus                       | RT-AX58                     | az internet sugárzására                           |


**Aláírás:** Oláh Bence

**Dátum:** 2024. 11. 27.
