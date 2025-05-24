# RAID a Windows: Què és, Utilitats i Nivells Existents

**RAID** (Redundant Array of Independent Disks) és una tecnologia que permet combinar diversos discos durs físics en una sola unitat lògica per millorar el rendiment, la seguretat o ambdues coses. A Windows, RAID s’utilitza per protegir dades, augmentar la velocitat d’accés o ampliar la capacitat d’emmagatzematge.

## Utilitats del RAID a Windows

- **Protecció de dades:** Evita la pèrdua d’informació en cas de fallada d’un disc.
- **Millora del rendiment:** Augmenta la velocitat de lectura i escriptura.
- **Gestió flexible de l’espai:** Permet combinar discos de diferents capacitats.

## Nivells de RAID Existents

- **RAID 0 (Striping):** Millora el rendiment, però no ofereix redundància.
- **RAID 1 (Mirroring):** Duplica les dades en dos discos per seguretat.
- **RAID 5:** Combina rendiment i redundància mitjançant paritat distribuïda.
- **RAID 10 (1+0):** Barreja mirroring i striping per a màxima seguretat i velocitat.

A Windows, es poden configurar aquests nivells de RAID tant per programari (Gestió de Discos) com per maquinari (controladores RAID dedicades).
## Com Configurar RAID a Windows

### Opcions de Configuració

A Windows, pots configurar RAID de dues maneres principals:

- **RAID per programari:** Utilitzant l’eina de Gestió de Discos de Windows o Storage Spaces.
- **RAID per maquinari:** Mitjançant una controladora RAID dedicada, habitualment configurada des de la BIOS o UEFI abans d’iniciar el sistema operatiu.

### Configuració de RAID per Programari

#### Mitjançant Gestió de Discos

1. Accedeix a la Gestió de Discos (`diskmgmt.msc`).
2. Selecciona els discos que vols utilitzar.
3. Fes clic dret i tria l’opció per crear un volum reflectit (RAID 1) o un volum distribuït (RAID 0).
4. Segueix l’assistent per completar la configuració.

#### Mitjançant Storage Spaces

1. Obre el “Tauler de control” i accedeix a “Espais d’emmagatzematge”.
2. Crea un nou grup d’emmagatzematge i afegeix-hi els discos.
3. Tria el tipus de tolerància a errors (simple, duplicat, paritat).
4. Dona nom i format al nou espai d’emmagatzematge.

### Configuració de RAID per Maquinari

1. Connecta els discos a la controladora RAID del teu equip.
2. Accedeix a la BIOS/UEFI i entra a la utilitat de configuració RAID.
3. Crea una nova matriu RAID seleccionant el nivell desitjat (0, 1, 5, 10).
4. Desa la configuració i inicia Windows.
5. Instal·la els controladors RAID si cal.

## Avantatges i Inconvenients dels Nivells de RAID

| Nivell   | Avantatges                          | Inconvenients                    |
|----------|-------------------------------------|----------------------------------|
| RAID 0   | Màxim rendiment, ús total de l’espai| Cap redundància, risc de pèrdua total de dades |
| RAID 1   | Alta seguretat, fàcil recuperació   | Només la meitat de la capacitat disponible |
| RAID 5   | Bon equilibri entre seguretat i espai| Rendiment d’escriptura inferior, mínim 3 discos |
| RAID 10  | Màxima seguretat i rendiment        | Necessita mínim 4 discos, menys espai útil |

## Consideracions Addicionals

- **Còpies de seguretat:** RAID no substitueix les còpies de seguretat. Sempre mantingues còpies externes de les dades importants.
- **Compatibilitat:** Les matrius RAID per maquinari poden no ser llegibles en altres equips sense la mateixa controladora.
- **Monitoratge:** Utilitza eines de monitoratge per detectar errors als discos i actuar ràpidament.

## Recursos Addicionals

- [Documentació oficial de Microsoft sobre Storage Spaces](https://learn.microsoft.com/windows-server/storage/storage-spaces/)
- [Guia de configuració RAID per maquinari](https://learn.microsoft.com/windows-server/storage/)

Amb aquestes opcions, pots adaptar la configuració RAID a les teves necessitats de rendiment i seguretat a Windows.