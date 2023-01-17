## Teorija:
Todo

## Uždavinių pavyzdžiai:

### Duotas potinklis 10.10.0.0/22 (segmento dydis 1024). A potinklį sudaro 12,5 proc. viso potinklio, B sudaro 50% viso potinklio, C sudaro 25% viso potinklio. Rasti kiekvienam potinkliui: A,B,C potinklio pradžią, pirmojo potinklio kompiuterio adresą, paskutinio kompiuterio adresą ir kaukę.

Duotas segmento dydis: 1024
Procentaliai suskaičiuojame reikiamus potinklio dydžius (**išrikiuojame mažėjimo tvarka!**):
B - $1024*0.5=512$
C - $1024*0.25=256$
A - $1024*0.125=128$

Skaičiuojame potinklių adresus:

B:
Kaukė (512): `/23 = 255.255.254.0`
Potinklio adresas: `10.10.0.0/23`
Tinklo adresai: `10.10.0.0 - 10.10.1.255`
Adresai kompiuteriams: `10.10.0.1 - 10.10.1.254`
C:
Kaukė (256): `/24 = 255.255.255.0`
Potinklio adresas: `10.10.2.0/24`
Tinklo adresai: `10.10.2.0 - 10.10.2.255`
Adresai kompiuteriams: `10.10.2.1 - 10.10.2.254`
A:
Kaukė (128): `/25 = 255.255.255.128`
Potinklio adresas: `10.10.3.0/25`
Tinklo adresai: `10.10.3.0 - 10.10.3.127`
Adresai kompiuteriams: `10.10.3.1 - 10.10.3.126`