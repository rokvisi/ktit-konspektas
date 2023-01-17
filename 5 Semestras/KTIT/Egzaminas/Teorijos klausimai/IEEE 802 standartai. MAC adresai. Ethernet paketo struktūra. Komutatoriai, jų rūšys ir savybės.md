## IEEE 802 standartai
Aprašo duomenų perdavimo spartą, ryšio terpes ir atstumus.
Visi naudoja tą patį Ethernet paketo formatą, todėl tarpusavyje suderinami.

| Standartas   | Greitis        |
| ------------ | -------------- |
| IEEE 802.3   | 10 Mbps        |
| IEEE 802.3u  | 100 Mbps       |
| IEEE 802.3z  | 1000 Mbps      |
| IEEE 802.3ae | 10 Gbps        |
| IEEE 802.bm  | 40 ir 100 Gbps |

## MAC adresai
MAC adresas (Ethernet adresas) susideda iš 2 dalių po 3 baitus (gamyklos suteiktas + mazgo eilės numeris).

Visuotinis (broadcast) adresas yra `FF:FF:FF:FF:FF:FF`.
> Svarbu, kad **lokaliame** tinkle MAC adresas butų unikalus.

## Ethernet paketas (kadras)
Dydžiai skaičiuojami baitais/oktetais (baitas = oktetas = 8 bitai).
Jei gavėjo apskaičiuota kontrolinė suma nesutampa su siuntėjo pateikta suma, kadras skaitomas sugadintu.

##### Struktūra
| | Preamble                | SFD       | MAC Dest | MAC Src   | Length      | Payload   | FCS             |
| - | ----------------------- | --------- | -------- | --------- | ----------- | --------- | --------------- |
| Aprašymas | skirta sinchronizacijai | skirtukas | gavėjas  | siuntėjas | kadro ilgis | duomenys  | kontrolinė suma |
| Baitai | 7                       | 1         | 6        | 6         | 2           | 46 - 1500 | 4               |
 
##### Paaiškinimai
- Preamble - skirta imtumo sinchronizacijai.
- SFD - Start frame delimiter (skirtukas).
- MAC Des/Src - Atitinkamai gavėjo ir siuntėjo MAC adresai.
- Length - Viso kadro (ethernet frame) ilgis.
- Payload - Siunčiami duomenys. (Jei duomenys < 46 baitai, *pridedamas atitinkamas kiekis nulinių baitų - padding*).
- FCS - Paketo kontrolinė suma (MAC Dest + MAC Src + Length + Payload) (pvz. 5827: 5+8=1**3**+2=5+7=1**2**=2)

## Komutatorių rūšys ir savybės
Komutatorius:
- Komutuoja gautą paketą į tam tikrą jungtį pagal gavėjo MAC adresą
- Automatiškai susiformuoja MAC adresų lentelę
- Nekeičia paketo
- Nereikalauja konfiguravimo
- Neturi jokių adresų

Rūšys:
- Nevaldomi
	-  jungtys gali dirbti skirtinguose režimuose.
	- Turi automatinį režimo nustatymą - sparta/dupleksas.
- Valdomi
	- MAC adresų filtravimas.
	- Spanning tree (*The Spanning Tree Protocol (STP) is responsible for identifying links in the network and shutting down the redundant ones, preventing possible network loops*.)
	- Port mirroring (*Port mirroring is used on a network switch to send a copy of network packets seen on one switch port to a network monitoring connection on another switch port.*)
	- [[Virtualūs lokalūs tinklai, Kadrų žymėjimas IEEE802.1q#Virtualūs lokalūs tinklai|VLAN]]
