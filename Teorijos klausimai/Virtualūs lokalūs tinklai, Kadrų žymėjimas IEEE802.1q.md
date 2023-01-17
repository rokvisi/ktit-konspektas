## Virtualūs lokalūs tinklai
Skirtingos paskirties įrenginius galima jungti prie to paties komutatoriaus. Tam pačiam LAN priklausantys įrenginiai gali būti prijungti prie skirtingų komutatorių.

1. Komutatorius dalinamas į keletą virtualių komutatorių, jungtims suteikiant skirtingas VLAN žymes (numerius).
2. Kiekvienas VLAN turi nuosavą MAC adresų lentelę ir neturi jokio ryšio su kitais.
3. Komutatoriai tarpusavyje sujungiami bendromis jungtimis.
4. Kad perduodant bendru kanalu paketai nesusimaišytų, komutatorius jų [[IEEE 802 standartai. MAC adresai. Ethernet paketo struktūra. Komutatoriai, jų rūšys ir savybės#Ethernet paketas#Struktūra|kadrą]] papildo VLAN žymėmis.

## Kadrų žymėjimas IEEE 802.1q
IEE 802.1q kadras yra beveik identiškas, kaip kiti IEE 802.* kadrai, išskyrus, kad turi **2 papildomas VLAN žymes**.

#### Paprastas 802.* kadras
![[IEEE 802 standartai. MAC adresai. Ethernet paketo struktūra. Komutatoriai, jų rūšys ir savybės#Ethernet paketas#Struktūra]]

#### 802.1q kadras

| Preamble                | SFD       | MAC Dest | MAC Src   |  *VLAN Tag* | *VLAN*   | Length      | Payload   | FCS             |
| ----------------------- | --------- | -------- | --------- | --------- | ------ | ----------- | --------- | --------------- |
| skirta sinchronizacijai | skirtukas | gavėjas  | siuntėjas |  0x8100 (802.1q tag'as)   | Prioritetas (4 bit) + VLAN id (12 bit)   | kadro ilgis | duomenys  | kontrolinė suma |
| 7                       | 1         | 6        | 6         | 2         | 2   | 2           | 46 - 1500 | 4               |
