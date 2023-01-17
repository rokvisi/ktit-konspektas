## Teorija
Todo

## Uždavinių pavyzdžiai:

### Perdavimui skirtos dažnių juostos plotis 50 MHz. Reikalinga 300 Mbps perdavimo sparta. Kiek bitų turi koduoti viena signalo būsena?

Duota:
$B=50MHz=50*10^6Hz$
$V_{max}=300 Mbps =300*10^6 b/s$
$K=log_2(L)=?$

Pagrindinė formulė:
$V_{max} = 2B * log_2(L)=2B*K$

Išvedame:
$K=\frac{V_{max}}{2B}=\frac{300*10^6}{2*50*10^6}=3$

Atsakymas: ==3 bitai vienoje būsenoje==

---

### Signalo būsenų pasikeitimo dažnis 1000 kartu per sek., signalų būsenų skaičius 16. Kiek laiko milisekundėmis užtruks pranešimo 100101010111 perdavimas?

Duota:
$L=16$, skirtingų signalo būsenų
$n_{pranešimo}=12$, bitų ilgio pranešimas

Randame, kiek viena būsena perduoda bitų:
$K=log_2(L)=log_2(16)=4$, bitai vienoje būsenoje

Randame, kiek būsenų reikės, kad perduoti pranešimą:
$\frac{n_{pranešimo}}{K}=\frac{12}{4}=3$, būsenų

Randame, kiek laiko užtruks 3 būsenos:
$\frac{3}{1000}s$ 

Atsakymą konvertuojame į milisekundes:
$\frac{3}{1000}*10^3=3ms$

Atsakymas: ==3ms== 

---

### Signalo būsenų pasikeitimo dažnis 2000 kartu per sek., signalų būsenų skaičius 8. Kiek laiko milisekundėmis užtruks pranešimo 100101010111 perdavimas?

Duota:
$L=8$, skirtingų signalo būsenų
$n_{pranešimo}=12$, bitų ilgio pranešimas

Randame, kiek viena būsena perduoda bitų:
$K=log_2(L)=log_2(8)=3$, bitai vienoje būsenoje

Randame, kiek būsenų reikės, kad perduoti pranešimą:
$\frac{n_{pranešimo}}{K}=\frac{12}{3}=4$, būsenų

Randame, kiek laiko užtruks 4 būsenos:
$\frac{4}{2000}=\frac{2}{1000}s$

Atsakymą konvertuojame į milisekundes:
$\frac{2}{1000}*10^3=2ms$

Atsakymas: ==2ms==

---

### Duotas greitis V(b/s)=32000 b/s ir V(bod) = 16000 bodų ir duota seka: 10010011110101 (kažkas tokio). Ir reikia nubraižyti grafiką pagal duotą seką bei apskaičiuoti reikšmes L ir K

Duota:
$V_{b/s}=32000$
$V_{bod}=16000$
$n_{pranešimas}=14$

Kadangi, bodų (būsenų) perduodame $V_{bod}$, o bitų perduodame $V_{b/s}$. Reikia bitus dalinti iš būsenų, kad gauti, kiek viena būsena perduoda bitų.

Randame, kiek viena būsena perduoda bitų:
$K=\frac{32000}{16000}=2$, bitai vienoje būsenoje

Randame, kiek iš viso yra skirtingų būsenų:
$L=2^K=2^2=4$, skirtingų būsenų

Randame, kiek būsenų reikės, kad perduoti pranešimą:
$\frac{n_{pranešimas}}{K}=\frac{14}{2}=7$

Braižome grafiką:
![[Pasted image 20230109230741.png]]