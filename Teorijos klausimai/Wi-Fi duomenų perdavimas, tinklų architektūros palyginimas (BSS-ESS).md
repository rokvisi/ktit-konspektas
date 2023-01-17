## Wi-Fi duomenų perdavimas
Naudojamas CSMA protokolas su kolizijų išvengimo (CA) mechanizmu, kuris leidžia išvengti laike sutampančio duomenų perdavimo tarp daugelio įrenginių.

Principai:
- Stebėk kanalą
- Kai jis atsilaisvina - nepulk iš karto siųsti.

Bazinis įrenginys - prieigos taškas (AP - access point)
Kiekvienas AP turi savo SSID - WLAN identifikatorių.

## Tinklų architektūros palyginimas (BSS ir ESS)
| Pavadinimas   | BSS                                                    | ESS                                                                                                              |
| ------------- | ------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------- |
| Apibūdinimas  | Kiekvienas AP turi atskirą SSID ir savo zoną           | Visi AP sudaro vieną zoną su tuo pačiu SSID                                                                      |
| Įranga        | Belaidis                                               | Prieeigos taškų sistema                                                                                          |
| Taikymas      | Individualiam naudojimui                               | Didelėms zonoms sukurti                                                                                          |
| Autentikacija | Nustatytas slaptažodis (WEB, WPA2)                     | Individualizuota (802.1x)                                                                                        |
| Problemos     | Galimi trukdžiai esant daugeliui AP netoli vienas kito pvz.: butuose | Vartotojas yra keliose AP zonose ir juda iš vienos zonos į kitą (dėl to reikalingas kontroleris pvz.: *eduroam*) | 

