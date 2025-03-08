# RAID 5

RAID 5 és una configuració de disc que utilitza striping amb paritat. Les dades es distribueixen entre tres o més discos, amb informació de paritat per permetre la recuperació en cas de fallada d'un disc. RAID 5 ofereix una bona combinació de rendiment, capacitat i tolerància a fallades.

El primer pas és assegurar-se que els quatre discos estiguin correctament connectats al sistema. Podeu verificar-ho visualment i amb eines de gestió del sistema.

![RAID Diagram](../img/discos.png)


El primer pas és assegurar-se que els quatre discos estiguin correctament connectats al sistema. Podeu verificar-ho visualment i amb eines de gestió del sistema.

![RAID Diagram](../img/4.png)

Ara he creat les particions per als 4 discos.

![RAID Diagram](../img/particions.png)

Aquesta instrucció agrupa les particions dels quatre discos en un únic dispositiu RAID, anomenat /dev/md0.

![RAID Diagram](../img/ce.png)

Podem fer un detail per comprovar que s''ha creat correctament.

![RAID Diagram](../img/detail.png)

Un cop fet això formateijo la partció on tinc els discos creada anteriorment.

![RAID Diagram](../img/format.png)

Ara creare una carpeta on muntare la partició temporalment.

![RAID Diagram](../img/mount.png)

Per desar la configuració actual del RAID, escanegeu-la i deseu-la al fitxer de configuració executant:

![RAID Diagram](../img/rot.png)

Obriu el fitxer /etc/mdadm/mdadm.conf amb l'editor de text que preferiu per confirmar que la configuració s'ha desat correctament. Si cal, realitzeu els ajustos addicionals corresponents.

![RAID Diagram](../img/device.png)


## Configuració del Muntatge Automàtic FSTAB ##

Per assegurar que el dispositiu RAID es munte automàticament en arrencar el sistema, afegiu la línia corresponent al fitxer /etc/fstab. D'aquesta manera, no caldrà muntar-lo manualment en cada reinici.

![RAID Diagram](../img/inici.png)

A continuació he creat un arxiu i una carpeta per fer la comprovació.

![RAID Diagram](../img/prof.png)

A continuació, es simula la fallada eliminant el disc número 3 del conjunt RAID.

![RAID Diagram](../img/falla.png)

Ara cal executar aquestes comandes per poder activar el RAID al reiniciar la màquina.

![RAID Diagram](../img/pass.png)

Finalment si entro a la carpeta podem comprovar que els arxius i carpetes creades continuen existint.

![RAID Diagram](../img/yess.png)
