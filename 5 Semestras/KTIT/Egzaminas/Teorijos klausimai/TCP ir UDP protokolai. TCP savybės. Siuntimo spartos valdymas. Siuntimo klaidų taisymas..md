TCP ir UDP yra **vieninteliai** [[Transporto sluoksnis. Prievadai (portai). Klaidų taisymas ir spartos reguliavimas. Siuntimo lango metodas#Transporto sluoksnis|transporto sluoksnio]] protokolai.
Tik transporto sluoksnio protokolai turi galimybė kreiptis į kompiuterį konkrečiu prievadu (port).
Prievadas (*dest* ir *src*) nurodomas **paketo** antraštėje (header).

## TCP
Protokolas **turi** klaidų/praradimų taisymą. Gali aptarnauti kelis sujungimus tuo pačiu portu.

![[Transporto sluoksnis. Prievadai (portai). Klaidų taisymas ir spartos reguliavimas. Siuntimo lango metodas#Spartos reguliavimas]]

##### Klaidų taisymas:
- Siuntėjas pats nežino, kokie paketai nepasiekė gavėjo, todėl gavėjas turi siųsti atgal paketų gavimo patvirtinimus ([[Transporto sluoksnis. Prievadai (portai). Klaidų taisymas ir spartos reguliavimas. Siuntimo lango metodas#ACK (Acknowlegment) klaidų taisymas|ACK]]).
- [[Transporto sluoksnis. Prievadai (portai). Klaidų taisymas ir spartos reguliavimas. Siuntimo lango metodas#Siuntimo langas|Siuntimo langas]], mažinamas pusiau, jei per timeout laiką negaunamas patvirtinimas.

##### Potencialios problemos:
- Skirtingi RTT *(reikia adaptyvaus laukimo laiko nustatymo mechanizmo)*.
- Didelis vėlinimas ir didelė vėlinimo sklaida *(reikia sugebėti atpažinti vėluojančius paketus)*.
- Skirtingi gavėjo talpumai *(reikia reguliuoti siuntimą pagal gavėjo galimybes priimti duomenis)*.
- Skirtingi tinklo pralaidumai pagal gavėjus/laiką *(reikia reaguoti į perkrovas tinkle)*.

## UDP
Protokolas **neturi** duomenų pristatymo garantijos, tačiau yra paprastas, spartus ir nereikalauja daug resursų. Gali būti naudojamas multicast režime.

Taikomas, kai:
- Taikomasis procesas negali laukti, kol kelyje prarasti duomenys bus pakartotinai perduoti. O nedidelis prarastų duomenų kiekis neturės didelės įtakos (video, audio).
- Taikomasis procesas pats rūpinasi prarastų duomenų siuntimo pakartojimu.
- Duomenų perdavimas vyksta kanalu, kuriame paketų praradimo praktiškai nėra.