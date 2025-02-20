## Instal·lació ldap al servidor

En primer lloc he instal·lat el servidor ldap i ldap-utils per configurar el servidor.

![a](./img/ldap.png)

Un cop instal·lat configurare el servidor ldap amb les credencials que jo vulgui.

![a](./img/reconfigure.png)

Un cop dins ens demana si volem guardar o eliminar lo configuració que hi ha actualment direm que sí.

![a](./img/yes.png)

Ara configurare el que s'anomena el name of the LDAP search per tant el nom del domini , que en el meu cas és marc.cat.

![a](./img/domini.png)

També ens demana la versió, selecciono la 3.

![a](./img/versi0o.png)

Posem el root com a admin de la base de dades.

![a](./img/root.png)

Compte de root.

![a](./img/privilegis.png)


Ara li assigno una contrasenya.

![a](./img/contrasenya.png)

I finalment el tipus d'encriptació per la contrasenya.

![a](./img/encrip.png)

Ara si faig un slapcat puc comprovar que s'ha aplicat la configuració al servidor.

![a](./img/slapcat.png)

## Creació usuaris al servidor

Dins del fitxer usu.ldif puc crear un nou usuari en el meu cas he creat l'usuari alu1 on li he creat el directori /home/alu1.

![a](./img/alu1.png)

També he creat una nova unitat organitzativa amb el nom users dins del fitxer uo.ldif.

![a](./img/unitat.png)

I finalment un nou grup anomenat alumnes on afagirem com a membre a alu1, tot això al fitxer grup.ldif.

![a](./img/ldif.png)

Ara ja tinc els fitxers configurats per crear els objectes que necessito, em queda anyadir-los amb la comanda ldapadd.

![a](./img/ldapadd.png)

## Unir client al domini

Un cop tinc el server actiu i ben configurat hi puc fer la prova per unir un client en aquest domini.

Jo he iniciat una nova màquina Ubuntu Desktop que fara com a client i s'unira al servidor ldap.

![a](./img/s3.png)

Un cop dins ens demana la configuració on posare ldap:// i la IP del servidor que és 10.0.2.15.

![a](./img/ldap1.png)

També he d'afegir la línia de gshadow al fitxer nsswitch.conf.

![a](./img/nss.png)


També he d'afegir la línia session optional
![a](./img/session.png)

També afegire aquesta línia.

![a](./img/s3g.png)

Ara si faig un getent passwd puc comprovar que tinc l'usuari al client, per tant estic connectat.

![a](./img/nice.png)

Per tant puc accedir a l'usuari.

![a](./img/alu11.png)

![a](./img/whoami.png)



## Perfils Mobils 


Ara crearem un altra carpeta i li pasarem la ruta al arxiu /rtc/exports.

![a](./img/perfil.png)

Li assignarem per al usuari alu2 el directori de la carpeta que hem creat.

![a](./img/alu2.png)

Li indiquem aquesta línia.
![a](./img/aaa.png)

Apartir d'aquí ja no vaig poder accedir a alu2. 