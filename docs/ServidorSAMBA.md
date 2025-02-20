# Introducció al servidor Samba
Un servidor Samba és una implementació lliure del protocol de xarxa SMB/CIFS, que permet la comunicació i l'intercanvi de fitxers entre ordinadors amb sistemes operatius diferents, com ara Linux, Windows i macOS. Samba facilita la integració de màquines Linux en entorns de xarxa Windows, permetent compartir recursos com ara fitxers i impressores de manera transparent i segura. A més, Samba pot actuar com a controlador de domini, gestionant autenticacions i permisos d'accés en una xarxa corporativa.

Primer instal·lo el servidor SAMBA.

![a](./img/ssamba.png)



Ara creare la carpeta on també li donare permisos.

![a](./img/carpetaa.png)


Ara dins del fitxer smb.conf un cop instl·lat samba posarem els permisos que li volem donar a la carpeta

![a](./img/proves.png)


Per aplicar els canvis realitzats he fet un systemctl restart smbd nmbd per reiniciar el servidor.

![a](./img/restart.png)


Ara he creat els usuaris al servidor, amb el useradd.

![a](./img/add.png)

Ara he creat més usuaris per fer proves.
![a](./img/colors.png)

Ara faig un tail per veure els usuaris que he creat.

![a](./img/tail.png)

Ara assigno una contrasenya al usuaris dins del servidor samba d'aquesta manera.

![a](./img/users.png)

Per últim canviarem algúns permisos com ara que l'usuari roig no pugui entrar, que els usuaris del grup colors puguin llegir i que balu pot llegir i escriure. També podrem iniciar sessió com a convidat.

![a](./img/conf.png)

## Proves amb client

Per configurar la part del client, repetirem els passos anteriors, fer un update i després instal·lar el paquet de samba.

![a](./img/instalar.png)

Un cop instal·lat el samba client obrire l'explorador d'arxius i posare la IP del servidor juntament amb la carpeta compartida.

![a](./img/samb.png)

Ara ens demanara com ens vole autenticar com anonim o com un usuari registrat.

![a](./img/autenti.png)

Ens registrem amb l'usuari blau que té permisos sobre la carpeta i efectivament la podem veure.

![a](./img/anonim.png)

Comprovació de permísos creats.

![a](./img/p.png)

Si intento entrar amb els usuaris que no tenen permís sobre la carpeta com son groc i roig no ens deixa.

![a](./img/roig.png)

![a](./img/groc.png)

![a](./img/er.png)
