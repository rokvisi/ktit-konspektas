
## OSI modelio sluoksniai ir jų apibūdinimai:
- Taikymo sluoksnis - skirtas vartotojui. Pvz.: HTTP aprašo sąveiką tarp naršyklės ir WEB serverio.
- Pateikimo sluoksnis - duomenų formatai, šifravimas.
- Sesijos sluoksnis - autentikacija, ryšio paruošimas, eiga ir nutraukimas.
- [[Transporto sluoksnis. Prievadai (portai). Klaidų taisymas ir spartos reguliavimas. Siuntimo lango metodas|Transporto sluoksnis]] - duomenų apsikeitimas tarp taikomųjų procesų.
- [[Tinklo sluoksnis. Interneto principai. IP paketo formatas#Tinklo sluoksnis|Tinklo sluoksnis]] - transportavimas tinklu, adresacija, maršrutų parinkimas.
- Kanalo sluoksnis - [[IEEE 802 standartai. MAC adresai. Ethernet paketo struktūra. Komutatoriai, jų rūšys ir savybės#Ethernet paketas (kadras)|Kadrai]], antraštės, perdavimas tarp gretimų mazgų.
- Fizinis sluoksnis - signalai, jungtys, dažniai ir pan.

![osi model 7 layers](https://www.cloudflare.com/img/learning/ddos/what-is-a-ddos-attack/osi-model-7-layers.svg "osi model 7 layers")

## Komunikavimo procesas:
1. Taikymo sluoksnis:
	1. vartotojas per naršyklę kreipiasi į tinklo paslaugą.
	2. naršyklė prie vartotojo duomenų prideda antraštę ir perduoda paketą transporto sluoksniui per TCP.
2. Transporto sluoksnis:
	1. TCP formuoja sujungimo su paslauga prašymo paketą (SYN), antraštėje nurodo paslaugos rūšį (pvz. portą 80) ir atidaro savo portą (pvz. 1212) duomenų priėmimui.
	2. perduoda paketą tinklo sluoksniui - IP
4. Tinklo sluoksnis - iš DNS serverio gauna paslaugos IP ir įrašo į antraštę kartu su siuntėjo IP adresu, perduoda į Ethernet sąsają.
5. Kanalo sluoksnis - perduoda paketus tik lokaliame tinkle, taigi perduos ne galutiniam gavėjui, o esančiam tarpiniam lokalaus tinklo mazgui (pvz. maršrutizatoriui). Į antraštę prideda siuntėjo ir savo MAC adresus, išsiunčia [[IEEE 802 standartai. MAC adresai. Ethernet paketo struktūra. Komutatoriai, jų rūšys ir savybės#Ethernet paketas|kadrą]].