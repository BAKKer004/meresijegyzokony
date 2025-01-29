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



# Mérési Jegyzőkönyv: Komplex Távközlési Hálózat Tervezése, Telepítése és Mérése **Időtartam:** 2 óra ## 1. Eszközök és Beállítások ### Eszközök: - Mikrotik LHG18 LTE antenna - Mikrotik nRay 60GHz mikrohullámú antennák - SOHO router (D-Link, TP-Link, ASUS) - Laptop vagy PC - HP Switch (opcionálisan) - iperf szoftver ### Eszközök IP-címek: - Mikrotik LHG18 LTE: 192.168.88.1 - Mikrotik nRay 60GHz Master: 192.168.88.2 - Mikrotik nRay 60GHz Slave: 192.168.88.3 - Router (AP mód): 192.168.88.4 - Switch (opcionális): 192.168.88.254 - Kliens laptop: 192.168.88.100-250 (DHCP-ből) ### Alhálózati maszk: 255.255.255.0 ## 2. Hálózati Tesztelés Eredményei ### 2.1. Mikrotik LHG18 LTE Antenna Jelerősségi Paraméterei - **RSRP (Reference Signal Received Power):** [Érték] - **RSRQ (Reference Signal Received Quality):** [Érték] - **SINR (Signal to Interference plus Noise Ratio):** [Érték] - **RSSI (Received Signal Strength Indicator):** [Érték] ### 2.2. Ping Teszt Eredményei | Cél IP cím | Válaszidő (ms) | Csomagok (sikeres/sikertelen) | |------------------|----------------|-------------------------------| | 192.168.88.1 | [Érték] | [Érték] | | 192.168.88.2 | [Érték] | [Érték] | | 192.168.88.3 | [Érték] | [Érték] | | 192.168.88.4 | [Érték] | [Érték] | ### 2.3. Sávszélesség Mérési Eredmények (iperf3) | Forrás IP | Cél IP | Sávszélesség (Mbps) | Eredmény | |------------------|-----------------|---------------------|----------| | [Laptop IP] | 192.168.88.xxx | [Érték] | [Érték] | | [Laptop IP] | 192.168.88.xxx | [Érték] | [Érték] | ### 2.4. Internet Elérés Teszt - **Ping Teszt (8.8.8.8):** - Válaszidő: [Érték] ms - Csomagok: [Érték] sikeres / [Érték] sikertelen - **Speedtest eredmény:** - Letöltési sebesség: [Érték] Mbps - Feltöltési sebesség: [Érték] Mbps ## 3. Eszközök Állapotának Ellenőrzése ### 3.1. Mikrotik nRay 60GHz Antennák Kapcsolati Állapot - **Master antenna (192.168.88.2):** - WIRELESS 60G STATUS: [Érték] - Kapcsolati minőség: [Érték] - **Slave antenna (192.168.88.3):** - WIRELESS 60G STATUS: [Érték] - Kapcsolati minőség: [Érték] ## 4. Hibakeresési Eredmények - **Tűzfal engedélyezés:** - Hálózati felfedezés engedélyezve: [Igen/Nem] - **DHCP és IP-címek ellenőrzése:** - DHCP szerver működése: [Igen/Nem] - Megújított IP-címek: [Érték] --- **Aláírás:** **Név:** **Dátum:**
