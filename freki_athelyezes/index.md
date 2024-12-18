# MÉRÉSI JEGYZŐKÖNYV

**A mérést végző neve:** Oláh Bence  
**A mérés tárgya:** Antennák teljesítményének és jelminőségének összehasonlítása  
**A mérés száma:** 5. mérés  
**A mérés dátuma:** 2024. 12. 12 

**A mérést vezette:** Sándor Péter  

**Évfolyam:** 13. E  
**Csoport:** GYAK 2  
**Helyszín:** V3 Labor  

---

## 1. Mérés célja  
A mérés célja három különböző típusú antenna, az **Iskra P20**, az **ISKRA P2845** és az **IKUSI FLASHD C48** teljesítményének összehasonlítása, valamint a jelszint és jelminőség (MER - Modulation Error Ratio) vizsgálata három különböző frekvencián (522 MHz és 730 Mhz).

---

## 2. Alkalmazott mérőeszközök és készülékek  

| Műszer neve                         | Típus       | Gyártási szám |
| ----------------------------------- | ----------- | ------------- |
|  Antenna                            |    philips  |    SDV5228    |
| Programozható antennaerősítő-szűrő  | Johansson   | 8202          |
| Antenna                             | Iskra       | P20, P2845    |
| Antenna                             | IKUSI       | FLASHD C48    |
| Spectrum Analizátor                 | Metek       | HDD           |

---

### 3. **Mérési helyszín és környezet**
- **Antenna magassága**: 2 m
- **Környezet jellemzői**: V3 labor
- **Adó távolsága**: 15 m

---

## 4. Antennák teljesítménye különböző frekvenciákon

| Frekvencia (MHz) | Antenna          | Jelszint (dBm) | MER (dB) | Bitsebesség (Mbps) |
| ---------------- | ---------------- | -------------- | -------- | ------------------ |
| **730 MHz**      | Iskra P20        | -61.8          | 24.6     | 8.2 – 8.6          |
|                  | ISKRA P2845      | -58.8          | 26.3     | 8.6 – 9.6          |
|                  | IKUSI FLASHD C48 | -58.5          | 27.0     | 8.4 – 9.2          |
| **522 MHz**      | Iskra P20        | -59.0          | 26.6     | 8.2 – 9.2          |
|                  | ISKRA P2845      | -52.8          | 33.2     | 8.2 – 10.0         |
|                  | IKUSI FLASHD C48 | -52.6          | 30.0     | 7.8 – 9.2          |


---

## 5. Értékelés

### Jelszint
Az **ISKRA P2845** antenna mutatta a legmagasabb jelszinteket minden frekvencián, különösen a 33. csatornán (570 MHz), ahol -52,8 dBm-es eredményt produkált. Az **IKUSI FLASHD C48** szintén magas jelszintet ért el, míg az **Iskra P20** antenna a leggyengébb jelszinteket mutatta, különösen a 706 MHz-es frekvencián (-64.8 dBm).

### Jelminőség (MER)
Az **ISKRA P2845** antenna kiemelkedett a modulációs hibaarány (MER) tekintetében is, a legmagasabb értéket a 33. csatornán érte el (33.2 dB). Az **IKUSI FLASHD C48** stabil jelminőséget biztosított minden frekvencián, míg az **Iskra P20** a 706 MHz-en jelentős jelminőség romlást mutatott (19.5 dB).

### Bitsebesség
A bitsebesség értékei az **ISKRA P2845** antennánál voltak a legjobbak, különösen a 570 MHz-es csatornán, ahol akár 10 Mbps is elérhető volt. Az **IKUSI FLASHD C48** antenna szintén magas bitsebességet biztosított a nagyobb frekvenciákon, míg az **Iskra P20** gyengébb teljesítményt mutatott a magasabb frekvenciákon.

---

## 6. Következtetés
Az **ISKRA P2845** antenna a legjobb teljesítményt nyújtotta mind a jelszint, mind a jelminőség és bitsebesség tekintetében, különösen a közepes frekvenciatartományban (570 MHz). Az **IKUSI FLASHD C48** stabil és megbízható választás, míg az **Iskra P20** csak alacsonyabb frekvenciákon javasolt használatra.

---

## 7. Javaslatok
Az **ISKRA P2845** antenna javasolt elsődleges használatra, mivel minden frekvencián magasabb jelszintet és jobb jelminőséget biztosított. Amennyiben költséghatékonyabb megoldás szükséges, az **IKUSI FLASHD C48** is megfelelő választás lehet. Az **Iskra P20** csak alacsonyabb frekvenciákon javasolt, ahol még kielégítő teljesítményt nyújt.

---

## 8. P-20 Képek:
<details>
    <summary>Kattins a részletekért</summary>

    **522Mhz Mért Képek:**
    <img src="(https://github.com/user-attachments/assets/df0295de-7f7b-4c67-be33-2e877e88db5e)">
    <img src="(https://github.com/user-attachments/assets/7d429f8c-11b8-42ec-80f2-f86730abd5b5)">
    <img src="(https://github.com/user-attachments/assets/c315dc73-6c86-4627-bcf6-dd85bcb6fd24)"/>
---

    **730MHz Mért Képek**
    <img src="(https://github.com/user-attachments/assets/5d7c7da6-d5f5-415b-8b83-e59abdfd36b9)"/>
    <img src="(https://github.com/user-attachments/assets/6d896358-fa15-47b1-a8df-8de4de9c54ce)"/>
    <img src="(https://github.com/user-attachments/assets/6e62e904-7b70-48ef-9227-5e136cfc17e1)"/>
---



</details>

<br>

## 9. P-2845 Képek:
<details>

    <summary>Kattins a részletekért</summary>

    **522hz Mért Képek:**
    <img src="(https://github.com/user-attachments/assets/dfbd6ec1-9e25-401a-948f-d25b23a16922)"/>
    <img src="(https://github.com/user-attachments/assets/0d0e9622-5886-4f60-904e-a5f44064663a)"/>
    <img src="(https://github.com/user-attachments/assets/996f4499-8d36-4a54-bdee-9da6fd9c04cc)"/>
---

    **730MHz Mért Képek**
    <img src="(https://github.com/user-attachments/assets/3ea60c29-6a45-4bf1-b790-51ddc13a0ba6)"/>
    <img src="(https://github.com/user-attachments/assets/6be9ad2c-c5d5-4865-8b95-9a9c1d2edd47)"/>
    <img src=(https://github.com/user-attachments/assets/503098c7-e5c0-469c-b546-024970b651e6)"/>
---

  

</details>

<br>

## 10. FlashHD C-48 Képek:
<details>
    <summary>Kattins a részletekért</summary>

    **522Mhz Mért Képek:**
    <img src="(https://github.com/user-attachments/assets/630ce8ba-0ba0-46dd-b1e1-122f6bc0378f)"/>
    <img src="(https://github.com/user-attachments/assets/ec6c2e9a-d360-4bc6-93ba-bdf6dc1d9c10)"/>
    <img src="(https://github.com/user-attachments/assets/7585990a-1748-4386-a1a1-9ec3f70a8143)"/>
---

    **730MHz Mért Képek**
    <img src="(https://github.com/user-attachments/assets/4166b43f-81e0-4d6b-b1fe-5bd997908b5f)"/>
    <img src="(https://github.com/user-attachments/assets/d79bb126-cd25-4281-8eca-348f7fa160de)"/>
    <img src="(https://github.com/user-attachments/assets/e9d47fca-6999-4124-99b4-2bab39554e1f)"/>
---


</details>


<br>




**Aláírás:**  
Sándor Péter  
**Dátum:** 2024. 10. 14
