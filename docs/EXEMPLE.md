## Prova de RAID 5 a VirtualBox

A continuació, s'explica que es realitzarà una prova pràctica de configuració de RAID 5 utilitzant VirtualBox com a entorn de virtualització. L'objectiu és simular el funcionament d'un sistema RAID 5 per entendre millor els seus avantatges i limitacions. Per a això, es crearà una màquina virtual amb el sistema operatiu Windows 10, a la qual s'afegiran quatre discs durs virtuals. Aquests discs es faran servir per configurar el volum RAID 5 des del propi sistema operatiu, permetent observar el procés de creació, la gestió de la redundància i la tolerància a fallades. Aquesta pràctica ajudarà a comprendre com es distribueixen les dades i la paritat entre els discs, així com els passos necessaris per recuperar la informació en cas de fallada d'un dels discs.

Ara he afegit 4 discs al virtualbox.

![a](../img/10s.png)

Un cop dins entroa la configuració de discos i podem veure que detacta els 3 discos virtuals afegits.

![a](../img/11.png)
![a](../img/12.png)

Ara cal convertir els discs virtuals a discs dinàmics per poder crear volums etc.

Ja surt l'opció de ferho en RAID 5.
![a](../img/vol.png)

Ens obrira una pestanya de l'asistent.

![a](../img/asisten.png)

I seleccionarem els discs per crear el RAID 5.

![a](../img/nou.png)

Assigno una lletra.

![a](../img/lletra.png)

Formateigo el volum amb format NTFS predeterminat de Windows.

![a](../img/for.png)

Surtira aquest avís.

![a](../img/avis.png)

I ja els tenim formatats per al RAID5.

![a](../img/forma.png)

## Prova fallada

Ara realitzare una prova de fallada per comprovar la funcionalitat de RAID5 per mantenir les dades útils.

Pimer he creat una carpeta i un fitxer a la unitat del RAID5 en el meu cas la D:.

![a](../img/fallo.png)

 **Simulo la fallada**
 
 Ara elimino un dels tres discs.
 Clicare a sense connexió  al disc 3.

 ![a](../img/eli.png)

![a](../img/ad.png)

I puc comprovar que encara existeix la carpeta i l'arxiu.

![a](../img/fallo.png)
## Conclusions

- RAID 5 ofereix una bona combinació de seguretat i eficiència.
- Protegeix les dades davant la fallada d’un disc sense perdre gaire capacitat ni rendiment.
- És útil en entorns on la disponibilitat i la integritat de la informació són importants.
- No requereix una gran inversió en discs addicionals.
- Tot i així, no substitueix la necessitat de fer còpies de seguretat.
