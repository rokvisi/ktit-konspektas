## Konstantos
Sklidimo greitis vakuume - $3*10^8$
Sklidimo greitis optinėje skaiduloje - $2*10^8$
Laikyti, kad kilobitas - $10^3$ bitų; megabitas - $10^6$ bitų.

## Uždaviniams
$K=log_{2}(L)$
$K$ - bitų skaičius bode.
$L$ - signalo lygių skaičius.

$V_{max}=2B*log_2(L)$, bitais per sek (b/s).
$B$ - dažnių juostos plotis. (Hz)
$L$ - signalo lygių skaičius.

Pagrindinė formulė vieno simbolio persiuntimui:
$H(p)=\Sigma_{i=1}^{n}(p_i*log_2(\frac{1}{p_i}))$, bitų (b).
Vieno simbolio persiuntimui esant lygioms tikimybėms:
$H(p)=n*(\frac{1}{n}*log_2(\frac{1}{\frac{1}{n}}))=n*\frac{1}{n}*log_2(n)=log_2(n)$, bitų (b).

$A_p=10lg(\frac{P_{įj}}{P_{iš}})$

### RTT (atstumo, greičio, laiko) formulės
$t_{siunt}=\frac{K}{R}$, bitais per sek (b/s).
$K$ - paketo ilgis bitais (b).
$R$ - tinklo greitaveika (b/s).
$t_{sklid}=\frac{L}{V}$, bitais per sek (b/s).
$L$ - atstumas tarp tinklo mazgų (m).
$V$ - signalo sklidimo greitis (m/s).