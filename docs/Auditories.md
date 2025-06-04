# Què és una auditoria?

Una **auditoria** és el procés de registrar i revisar esdeveniments o activitats que tenen lloc en un sistema informàtic. El seu objectiu principal és supervisar l’ús dels recursos, detectar accessos no autoritzats, identificar canvis en la configuració i garantir el compliment de les polítiques de seguretat.

## Per a què és útil?

- **Seguretat:** Permet detectar intents d’accés no autoritzats o activitats sospitoses.
- **Compliment:** Ajuda a complir normatives legals i polítiques internes.
- **Resolució de problemes:** Facilita la investigació d’incidents i la identificació d’errors.
- **Control de canvis:** Registra modificacions en fitxers, configuracions i comptes.

## Com funciona a Windows Server?

A **Windows Server**, l’auditoria es configura mitjançant la **Política d’auditoria** (Audit Policy) a l’Editor de directives de seguretat local o a través de les **Directives de grup** (Group Policy). Els passos bàsics són:

1. **Configurar la política d’auditoria:** Selecciona els esdeveniments a auditar (inici de sessió, accés a fitxers, canvis en objectes, etc.).
2. **Registrar esdeveniments:** Windows desa els esdeveniments auditats al **Visualitzador d’esdeveniments** (Event Viewer), dins del registre de seguretat.
3. **Revisar els registres:** Els administradors poden analitzar aquests registres per detectar activitats inusuals o no autoritzades.

L’auditoria a Windows Server és una eina clau per a la gestió i seguretat dels sistemes empresarials.

## Auditoria inici sessió

Per configurar una auditoria em d'entrar a Directives de seguritat local al servidor.

![a](../img/audi.png)

Aquí podem configurar qualsevol auditoria tant per, inicis de sessió, accés a objectes, privilegis etc.

Jo configurare una auditoria d'inici de sessió.

![a](../img/ci.png)

Le configurat per registrar cada inici de sessió exitos per tant he marcat l'opció "Correcto".

Per veure el resultat he tancat la sessió actual.

![a](../img/bb.png)

Seguidament entro al registre de windows per comprovar el registe.

![a](../img/even.png)

Ens dirigim a la secció de registres de Windows i seguitat.

![a](../img/www.png)

I ja puc veure el registre d'inici de sessió amb l'ID 4624.

![a](../img/logon.png)

Si fem doble clic ens dona més informació del registre com el dispositiu l'usuari i el registre complet.

![a](../img/inf.png)

## Auditoria accés a objectes

He fet un altra prova d'auditoria per accés a objectes.

![a](../img/objectes.png)


