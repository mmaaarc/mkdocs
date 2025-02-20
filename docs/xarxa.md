# Configuració xarxa VirtualBox

Per poder tenir connexió a internet tindrem que afegir una o varies interfícies a la màquina.

En aquest cas he afegit un adaptador amb Xarxa NAT, aquest tipus de Xarxa ens proporciona una direcció IP dinàmica que podrem utilitzar en qualsevol lloc i aquesta IP no cambiara.

El primer que cal fer és anar a  **Fitxer** // **Eines** //  **Network Manager**.

Aquí crearem una nova xarxa NAT.

![a](/img/xarxanat.png)


Un cop fet això ja puc assignar la xarxa NAT creada a la màquina.

![a](/img/xarxa.png)

Si accedim al Ubuntu i fem un ip a podrem comprovar que rep la IP per DHCP.

![a](/img/ips.png)


## Opcions Xarxa 

De la mateixa manera que podem posar una IP per DHCP podem posar-la manual i de diferents maneres.


## IP manual per terminal

Per aixó tinc que obrir una finestra amb la terminal, i dirigirme hasta el fitxer 01-network-manager-all.yaml on podre cambiar els paràmetres de xarxa.

![a](/img/ruta.png)

I li assignare un IP manual diferent.

![a](/img/netplanmanual.png)

Un cop fet això caldra aplicar els canvis amb la comanda netplan apply (nom fitxer).

![a](/img/guardar.png)

Si no apareix res significa que els canvis han estat aplicats correctament, en el cas contrari apareixeran els errors i la línia exacta.

## IP manual interfície gràfica 

Aquesta és la forma més facil per establir una IP com a usuari, ja que és molt més visual.

 Per això em dirigire a la secció de paràmetres, cap

 ![a](/img/m.png)

 
 I ara em dirigire a la secció de xarxa, i aplicare la configuració, la Adreça de xarxa que volem donarli a l 'ordinador, la mascara de xarxa /24 i la adreça del router  (Passarel·la).

 ![a](/img/cable.png)


 I si posem ip a ens mostrara la ip assignada a la interfície enp0s3.

 ![a](/img/c.png)
<p xmlns:cc="http://creativecommons.org/ns#" >Aquesta obra té la llicència <a href="https://creativecommons.org/licenses/by-nc-nd/4.0/?ref= chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC BY-NC-ND 4.0<img style="height:22px!important;margin-left:3px ;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical -align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical -align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/nc.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical -align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/nd.svg?ref=chooser-v1" alt=""></a></p>