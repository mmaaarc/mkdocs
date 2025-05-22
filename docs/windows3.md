## Introducció

En aquest sprint abordarem la configuració i la gestió de dominis en un entorn Windows, així com el maneig de comptes d'usuari, grups i perfils mòbils. També establirem polítiques de seguretat i control d'accés a recursos, tant locals com de xarxa.

## Active Directory

Active Directory és el servei de Microsoft que permet gestionar els dominis en xarxes distribuïdes, per això utilitzare un Windows server amb el Active Directory instal·lat.


Creare dos adaptadors un amb connexió interna i l'altre amb NAT. 


![a](../img/interna.png)

- Posteriorment, comprovarem que la configuració de xarxa al servidor detecta ambdós adaptadors.

![a](../img/ipconf.png)



### - Configuració del Domini

Un cop feta l'instal·lacio és reiniciara el sistema i ja podre accesdir al domini.

![a](../img/dom.png)

Tot i que el primer que s'ha de fer és administrar el servidor 

![a](../img/agregar.png)

Ara començare a instal·lar els rols i serveis.

![a](../img/probar.png)

![a](../img/sul.png)


També activare el servei DNS i el servei Active Directory.

Jo també he fet funcional el servidor com a domini per tant li he assignat un nom de domini.

![a](../img/domain.png)


Li assigno una contrasenya.

![a](../img/con.png)

![a](../img/baiges.png)

Un cop revisades les comprobacions ja estara instal·lat.

![a](../img/ya.png)

### - Unió d'equips

Per fer proves he creat un nou usuari dins herramientas del servidor i usuarios equipos de Active Directory.

![a](../img/usu.png)

Creo l'usuari Joan al servidor.

![a](../img/j.png)

I una contrasenya.

![a](../img/co.png)



A continuació entrare en un client desde un altra màquina al domini.

![a](../img/estatic.png)

Comprovo que puc fer ping.

![a](../img/png.png)

Ara uneixo el client al servidor. 

![a](../img/jss.png)

M'unire al usuari creat joan.

![a](../img/joa.png)

![a](../img/cuenta.png)

![a](../img/fg.png)

I ja estare dins del domini amb l'usuari.

![a](../img/siu.png)



### - Creació de grups

Podem crear grups per gestionar els usuaris de manera més eficaç. El procés per crear grups és molt similar al de crear usuaris.

![a](../img/grupos.png)

A continuació creo un grup de prova anomenat jugadors
![a](../img/jugador.png)

Ara he afegit l'usuari Joan al grup jugadors.

![a](../img/mm.png)



### - Unitats Organitzatives (UO) i GPOs

Les unitats organitzatives (UO) ens permeten organitzar els objectes de domini (com usuaris i equips) per aplicar polítiques de manera més eficient.



- Crearem una nova UO amb el botó dret sobre el domini i afegirem usuaris per provar les configuracions.





He afegit l'usuari a l'únitat organitzativa
![a](../img/asd.png)


#### - GPOs

Les polítiques de grup (GPO) permeten establir configuracions per a usuaris i equips dins del domini.



- Crearem una GPO per la UO i vincularem una política que mostri un missatge de benvinguda als usuaris quan iniciïn sessió.

![a](../img/mo.png)
![a](../img/admin.png)

![a](../img/ini.png)
![a](../img/ho.png)


- A continuació, aplicarem restriccions com la prohibició d'accés al bluetooth.

![a](../img/blue.png)

- Realitzarem proves amb els usuaris per verificar que les restriccions funcionen correctament.

![gpo](../img/anom.png)



També podem establir polítiques de contrasenya a través de GPO, com la durada o complexitat de les contrasenyes.



### - Perfils mòbils

Els perfils mòbils permeten que els usuaris accedeixin a les seves dades des de qualsevol client del domini, guardant la informació en el servidor.

- Primer he creat una carpeta per perfils mobils.

![pmo](../img/mobils.png)

- Ara compartixo la carpeta amb els usuaris del grup jugadors.

![gpo](../img/comp.png)


- En quant a permisos he assignat lectura i escriptura

![gpo](../img/pper.png)

![gpo](../img/d.png)

Un cop fet això he compartit la carpeta al usuari joan.

![gpo](../img/c.png)


I ara si accedeixo al client ja podre accedir a la carpeta creada al servidor compartida als usuaris del grup jugadors, en aquest cas Joan si que pertany al grup.

![gpo](../img/client.png)
