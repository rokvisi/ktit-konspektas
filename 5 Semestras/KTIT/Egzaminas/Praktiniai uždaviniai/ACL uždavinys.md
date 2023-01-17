## Teorija:
Todo

## Uždavinių pavyzdžiai:

### Reikalingas ACL sąrašas, kuris tikrintų paketus ateinančius į M3 maršrutizatoriaus (angl. rauterio) kairiąją sąsają (angl. interfeiso). Sąrašas turi drausti kompiuteriui 192.168.2.1, esančiam 192.168.2.0/24 potinklyje pasiekti Viešas WWW serverį (2.2.2.20)

![[Pasted image 20230109234322.png]]
ACL taisyklės šablonas:
`[permit/deny] [proto] [sender_ip] [sender_inverse_mask] [host_ip] [host_inverse_mask]`
Vietoj `[ip][inverse_mask]` kombinacijos galima naudoti `any`. Galios visiems paketams.
Vietoj `[ip][inverse_mask]` kombinacijos galima naudoti `host [ip]`. Galios vienam kompiuteriui.
Vietoj `[inverse_mask]` galima naudoti `0.0.0.0`. Galios visam tinklui.

`sender` ir `host` gali būti ir kompiuteriai ir tinklai. Todėl naudojant kompiuterio IP su kauke `0.0.0.0`, taisyklė vistiek galios tik tam kompiuteriui.
>Gali būti netiesa!

Atvirkštinės kaukės skaičiavimas (kiekvieną kaukės dėmenį atimti iš 255):
Tinklo kaukė = 255.255.255.0
Atvirkštinė kaukė = 0.0.0.255
>Šio skaičiavimo uždaviniui nereikia.

Uždavinio atveju taisyklė taikoma iš kairės pusės. Taisyklėje `sender` bus `Viešas WWW`.

Atsakymas:
deny ip 2.2.2.20 0.0.0.0 192.168.2.1 0.0.0.0
permit ip any any

Nereikalingos komandos:
deny ip 192.168.2.1 0.0.0.0 2.2.2.20 0.0.0.0