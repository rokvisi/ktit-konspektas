## Teorija
Todo

## Uždavinių pavyzdžiai:

### Tekste naudojami 8 simboliai: αβγδεζηθ , kurių pasikartojimo tikimybės lygios: po 0,125. Kiek bitų perduoda tekstas: βδδαεθεεβγ ?

Duota:
$S = \{α, β, γ, δ, ε, ζ, η, θ\}$
$n = |S|=8$
$L_{tekstas} = 10$

Pagrindinė formulė vieno simbolio persiuntimui:
$H(p)=\Sigma_{i=1}^{n}(p_i*log_2(\frac{1}{p_i})) bitų$

Kadangi tikimybės lygios, formulė tampa:
$H(p)=n*(\frac{1}{n}*log_2(\frac{1}{\frac{1}{n}}))=n*\frac{1}{n}*log_2(n)=log_2(n)$

Vieną simbolį persiųsti reikia:
$H(p)=log_2(8)=3 bitų$

Visą tekstą persiųsti reikia:  
$I_{tekstas}=H(p)*L_{tekstas}=3*10=30 bitų$

Atsakymas: ==30 bitų==