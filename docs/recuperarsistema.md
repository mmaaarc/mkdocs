# Recuperar GRUB 

Si som usuaris nous i no tenim prou coneixements d'informàtica és possible que algun cop el nostre equip no arranqui i en alguns casos el propi usuari ha eliminat una petita part del sistem d'arrencada o simplement esta danyat, per això fare una prova de com recuperar el sistema borran la carpeta GRUB.


# BOOT REPAIR
 

  Jo ho he fet amb una maquina virtual Ubuntu tot i que normalment un usuari bàsic utilitzara el seu propi sistema operatiu per tant tindra que instal·lar a una unitat apart tant sigui un pen drive o una unitat USB la ISO de recuperació 
  BOOT REPAIR.

   ![a](/img/boot.png)

  Ara ja tenim la ISO instal·lada però primer tindre que eleiminar la carpeta grub del ubuntu.
    
   ![a](/img/mv.png)

Ara si intentem reiniciar la màquina apareixera aquest error que ens indica que no hi ha sistema d'arrencada ja que l'hem eliminat.
   ![a](/img/error.png)

Per tant ara és el moment on tenim que inserir en cas de ser un usuari amb la seva màquina local el dispositiu USB amb la ISO del BOOTREPAIR pero amb el meu cas desde virtual box posare la ISO.

![a](/img/boot1.png)

I ara iniciare un altre cop la màquina, si ets un usuari amb la teva màquina local per inserir al dispositiu USB mantindras la tecla F10, SUPR, F12 depenent el tipus de placa base per entrar al administrador d'arrencada.

Un cop dins ens apareixera una interfície gràfica, seleccionarem l'opció REPAIR BOOT.

![a](/img/repair.png)

Seguidament ens pregunta quina opció de recuperació volem posare la recomanda.

![a](/img/tipus.png)

I començara la reparació.

![a](/img/pas.png)

Finalment si s'ha reparat correctament ens apareixera aquesta pestanya.

![a](/img/succes.png)

Ara reiniciare la màquina i ja tindre el grub instal·lat per tant podre iniciar la màquina.

![a](/img/be.png)

![a](/img/fet.png)

# SUPERGRUB2

És una altra eina de recuperació d'arranc tot i que és més complexa i et brinda més control i personalització.

Seguirem els mateixos passos que amb el boot repair, primer ens baixarem la ISO del supergrub2

![a](/img/iso1.png)

També tinc una màquina Ubuntu la cual iniciare i fare un altra prova borrant el grub.

![a](/img/mv.png)

Ens apareixera el mateix error ja que hem borrat el GRUB.

![a](/img/error.png)

Ara inserire la ISO del SuperGrub2.

![a](/img/grub2.png)

Ens apareixera un menú com aquest.

![a](/img/menu.png)

Seleccionare detecta sistemes operatius i particions.


![a](/img/detecta.png)

I per últim seleccionare el sistema operatiu que tenia Linux i la partició generica. 

![a](/img/linux.png)

Un cop fet això al reiniciar ja podre accedir a l'interfície gràfica tot i que per que continue funcionant he tingut que instal·lar el disco general.

![a](/img/disco.png)

Seguidament actualitzare el GRUB2

![a](/img/recu2.png)

I finalment instal·lare el GRUB.

![a](/img/ya.png)

Un cop fet això ja tindre l'arranvc arreglat.
<p xmlns:cc="http://creativecommons.org/ns#" >Aquesta obra té la llicència <a href="https://creativecommons.org/licenses/by-nc-nd/4.0/?ref= chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC BY-NC-ND 4.0<img style="height:22px!important;margin-left:3px ;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical -align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical -align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/nc.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical -align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/nd.svg?ref=chooser-v1" alt=""></a></p>