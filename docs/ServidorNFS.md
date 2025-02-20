Pimer instl·lare el servidor nfs al Ubuntu, amb aquesta comanda.

![a](./img/nfs.png)

També l'instl·lació per la part del Ubuntu client.

![a](./img/rpcbind.png)


I per al client Windows.

![a](./img/windows.png)

Seguidament anire a activar o desactivar característiques de Windows.

![a](./img/pas2.png)

I finalment activare el servei nfs per al client.

![a](./img/servei.png)

Ara creo una carpeta anomenada compartida i li dono els permisos adients.

![a](./img/carpetan.png)

Ara al arxiu exports afegeixo aquesta línia 

![a](./img/rs.png)

Si ara faig la prova amb el windows puc comprovar que efectivament esta compartida cal recordar que tene que estar al mateix rang de xarxa.

![a](./img/ww.png)

Sí ara creo una carpeta desde el Windows la tinc que poder visualitzar al servidor.

![a](./img/hola.png)

Efectivament apareix al servidor.

![a](./img/compartida.png)