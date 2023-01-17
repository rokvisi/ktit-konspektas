## Teorija:
Todo

## Uždavinių pavyzdžiai:

### Naudojant komandą „ping“ į serverį gautas atsako laikas RTT=3 ms. Koks maksimalus atstumas iki serverio, jei kelias eina optiniais kabeliais? Nurodykite kilometrais.

RTT - Paketo kelionės laikas iki serverio **ir atgal**.

Laiką dalinam iš 2, nes klausia apie atstumą iki serverio (kelionė tik į vieną pusę):
$t=\frac{3ms}{2}=1.5ms$

Laiką konvertuojame į sekundes:
$t=1.5*10^{-3}s$

Greitis duotas (optinis kabelis):
$V = 2 * 10^8 m/s$

Taikome laiko/atstumo/greičio formulę, gaunant atsakymą:
$L = tV = (1.5*10^{-3})*(2*10^{8})=3*10^5m$

Atsakymą konvertuojame į kilometrus:
$L=3*10^5m = 3*10^2km=300km$

Atsakymas: ==300 km==

---
### Koks minimalus atsako laikas milisekundėmis (RTT), jei siuntėjas ir gavėjas bendrauja per geostacionarų palydovą 36 000 km aukštyje?

![[Pasted image 20230110232536.png]]

RTT - Paketo kelionės laikas iki serverio **ir atgal**.
Iš viso 4 siuntimai (client -> sat -> server -> sat -> client).

Randame visą atstumą:
$L = 4*(36*10^3)=144*10^3km$

Atstumą konvertuojame į metrus:
$L=(144*10^3)*10^3=144*10^6m$

Greitis duotas (vakumas):
$V = 3 * 10^8 m/s$

Taikome laiko/atstumo/greičio formulę, gaunant atsakymą:
$t=\frac{L}{V}=\frac{144*10^6}{3 * 10^8}s$

Atsakymą konvertuojame į milisekundes:
$t=\frac{144*10^6}{3*10^8}*10^3=\frac{144*10^9}{3*10^8}=\frac{1440}{3}=480ms$

Atsakymas: ==480ms==

---
### Turime optinį žiedą. Atstumas tarp miestų yra po 100 km, t.y. viso žiedo ilgis 500 km. Paskaičiuokite, koks galimas minimalus RTT ping‘ui tarp kompiuterio ir serverio, kai: -visame LAN‘e duomenų perdavimo sparta yra 10 Gbps; -linija tarp miestų D ir E yra nutrūkusi. Atsakyma pateikite milisekundėmis.

![[Pasted image 20230109234514.png]]

RTT - Paketo kelionės laikas iki serverio **ir atgal**.
$V_{lan}>=1$, todėl laikome, kad duomenų perdavimas tarp kompiuterių neturi įtakos.
Kadangi, tarp D ir E praėjimo nėra, reikia eiti aplinkui.

$L=2 * 4 * 100= 2 * 400 = 800km$, dauginame iš 2, nes kelionė **pirmyn-atgal**.
Atstumą konvertuojame į metrus:
$L=800 * 10^3m$

Greitis duotas (optinis kabelis):
$V=2*10^8m/s$

Taikome laiko/atstumo/greičio formulę, gaunant atsakymą:
$t=\frac{L}{V}=\frac{800*10^3}{2*10^8}=\frac{8*10^5}{2*10^8}=\frac{8}{2*10^3}=\frac{4}{1000}s$

Atsakymą konvertuojame į sekundes:
$t=\frac{4}{1000}*10^3=4ms$

Atsakymas: ==4ms==