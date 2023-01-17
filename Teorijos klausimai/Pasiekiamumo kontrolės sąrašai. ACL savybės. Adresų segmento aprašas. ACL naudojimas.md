## Pasiekiamumo kontrolės sąrašai
Skirti *stateless firewall* realizacijai. Jie diegiami maršrutizatoriuose arba specialiuose srautų filtravimo stotyse.

## ACL savybės
- Paketų tikrinimas pagal nurodytą filtrą nustatytoje maršrutizatoriaus sąsajoje
- Filtras gali būti taikomas *in* arba *out* krypties paketams.
- Kiekvienas krypties paketas tikrinamas ar atitinka kurios nors taisyklės aprašą.
- ACL rezultatas yra *permit* arba *deny*.
- Kai tik randama paketui tinkama taisyklė, vykdomas joje nurodytas veiksmas, o tolesnės taisyklės **nebetikrinamos**.

## ACL naudojimas
- Blokuoti komunikavimui pakanka blokuoti paketus viena kryptimi.
- Leisti išimtinį duomenų apsikeitimą būtina iš abiejų pusių.
- Jeigu **nėra ACL**, tada visi paketai leidžiami.
- Sąrašo pabaigoje visada taikoma taisyklė `deny ip any any`.

## Adresų segmento aprašymas
Adresų segmentas, kuriam taikoma taisyklė aprašomas nurodant segmento pradinį adresą ir šabloną (wildcard).

|                | su kauke                  | su šablonu                     |
| -------------- | ------------------------- | ------------------------------ |
| vienas adresas | `1.1.1.1 255.255.255.255` | `1.1.1.1 0.0.0.0 host 1.1.1.1` |
| segmentas /24  | `1.1.1.0 255.255.255.0`   | `1.1.1.0 0.0.0.255`            |
| segmentas /28  | `2.2.2.0 255.255.255.240` | `2.2.2.0 0.0.0.15`             | 

