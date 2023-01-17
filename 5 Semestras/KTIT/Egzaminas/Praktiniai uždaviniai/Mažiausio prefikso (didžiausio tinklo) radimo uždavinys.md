## Teorija
Todo

## Uždavinių pavyzdžiai:

### Duoti tinklo potinklių adresai. Pasirinkite prefiksą taip, jog potinklyje tilptų didžiausias tinklo įrenginių skaičius:

![[Pasted image 20230109233824.png]]
Atsakymas:
21, 10, 22, 28
6, 14, 12, 30
Nereikalingi: 0, 7, 16, 26

IP adresas yra 4 dvejetainiai skaičiai sujungti nuosekliai į vieną didelį skaičių.
Kiekvienas IP adreso dėmuo yra individualus dvejetainis skaičius.
Musų tikslas surasti, kiek visame IP adrese yra nulių iš dešinės pusės.
Tą skaičių atėme iš 32, gausime norimą prefiksą (kaukę).

Imame `200.64.248.0`, kaip pavyzdį.

Pirmas skaičius = `248`
Praleidome nulių = `1`

`248` konvertuojame į dvejetainį formatą:

| 128 | 064  | 032  | 016  | 008   | 004   | 002   | 001   |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1   | 1   | 1   | 1   | 1   | 0   | 0   | 0   | 

Skaičius `248` turi 3 nulius iš dešinės.

Kadangi praleidome vieną 0 (dvejetainė forma `00000000`), dar pridedame $1*8=8$ nulius.

Visame IP adrese nulių nuo dešinės yra:
$3_{248\_nuliai} + 8_{praleisti\_nuliai} = 11_{ip\_nuliai}$ 

Nulius atimame iš 32, randame prefiksą (kaukę):
$32_{magic}-11_{ip\_nuliai}=21_{prefiksas}$

Atsakymas: ==/21==

---