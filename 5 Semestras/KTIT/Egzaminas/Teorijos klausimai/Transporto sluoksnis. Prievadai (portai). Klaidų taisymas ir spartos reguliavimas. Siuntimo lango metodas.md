## Transporto sluoksnis
- Aprašo duomenų mainus tarp tinklinių taikomųjų procesų.
- Tinklo sluoksnis pristato duomenis į nurodytą tinklo mazgą. Tada išpakuotų duomenų srautą konkrečiam taikomajam procesui atiduoda transporto sluoksnis.
- Tai paskutinis OSI modelio sluoksnis, kuriame numatytas duomenų perdavimo klaidų taisymas.

## Funkcijos
- Keistis duomenimis tarp taikomųjų procesų per prievadus (port).
- Taisyti perdavimo klaidas ([[#ACK (Acknowlegment) klaidų taisymas|ACK]])
- Siuntimo spartos valdymas ([[#Siuntimo langas]])

## Prievadai (port)
- Į transporto sluoksnį ateinantys paketai rikiuojami į atskiras eiles kiekvienam taikomajam procesui.
- Duomenų paketų eilė prie taikomojo proceso vadinama prievadu (port).
- Prievadų numeriai yra transporto sluoksnio paketų adresai.
- Standartiniai taikomieji procesai turi fiksuotus prievadų numerius. Juos nustato **IANA** (Internet Assigned Numbers Authority)

## Klaidų taisymas ir spartos reguliavimas

##### ACK (Acknowlegment) klaidų taisymas
Siuntėjas numeruoja siunčiamų duomenų porcijas ir kiekvienai iš jų per nustatytą laiką $\Delta T$ turi gauti patvirtinimą ACK iš gavėjo.

Nesulaukus ACK per nustatytą laiką, duomenų siuntimas kartojamas.

##### Spartos reguliavimas
1. TCP išbando tinklo pralaidumo galimybes.
2. TCP Reaguoja į perkrovas sulėtindamas duomenų siuntimą.

## Siuntimo langas
$n$ - siuntimo langas.

1. Išsiunčiama $n$ porcijų paeiliui.
2. Kol tebevyksta siuntimas, turėtų ateiti pirmųjų porcijų gavimo patvirtinimai [[#ACK (Acknowlegment) klaidų taisymas|ACK]]. Tolesnio siuntimo **nestabdom**, kol kelyje esančių porcijų skaičius **neviršys** $n$. 

Esant idealioms siuntimo sąlygoms $n$ porcijų dydžio langas "slysta" išsiunčiamų duomenų eile maksimaliu siuntimo greičiu.