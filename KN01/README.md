# KN01

## Aufgabe A

Ein Hypervisor ist eine Software, die Ressourcen von physischen Hardware mehreren VMs gleichzeitig zur Verfügung stellen kann. Es erlaubt, auf physischer Hardware Virtuelle Umgebungen neben dem tatsächlichem Host Computer auszuführen. 

### Unterschiede Hypervisor Typ 1 & 2

|Hypervisor Typ|Ressourcenzuweisung                       |Bedienung            |Zu bietende Leistung|
|--------------|------------------------------------------|---------------------|--------------------|
|Typ 1         |Greifen direkt auf Hardware des Host zu   |komplex              |Hohe Leistung       |
|Typ 2         |handelt Ressourcenzuweisung mit dem OS aus|einfacher zu bedienen|Tiefere Leistung    |

* Hypervisoren vom Typ 1 greifen direkt auf die Hardware des Hosts zu, während Hypervisoren vom Typ 2 die Ressourcenzuweisung mit dem betriebssystem aushandelt.
* Die Benutzung und Verwaltung eines Typ 1 Hypervisor ist viel komplexer als die eines Typ 2, welches auch für technisch nicht versierte Benutzer einfacher ist zu bedienen.
* Typ 1 Hypervisoren bieten eine höhere Leistung, da keine Ressourcen mit dem Betriebsystem ausgehandlet werden müssen, anders als bei Typ 2 Hypervisoren. Diese dürfen nur vom System bereitgestellte Ressourcen beützen.

## Aufgabe B

### Host-System Ressourcen überprüfen

Ich vermute, dass das System ein Hypervisor vom Typ 2 verwendet, da die VM in einer Anwendung läuft (VM VirtualBox), und nicht direkt auf physischer Hardware.

Das host-System hat 16 Logische Prozessoren und 16 GB RAM. Wir verwenden VM VirtualBox.

* RAM: ![image](https://github.com/user-attachments/assets/53677f2e-7d5e-4500-b17a-5243386eec46)

* Logische Prozessoren: ![image](https://github.com/user-attachments/assets/c8df280a-df8c-48f2-affb-c42581cd8512)

### Umsetzen von VM mit mehr RAM / CPU Kerne als eigentlich möglich

* Wie im Bild unten gezeigt wurde der VM mehr RAM zugeordnet, als das Host-System hat.

Einstellungen VM: ![image](https://github.com/user-attachments/assets/70e4843f-9c9c-463e-9d4e-869f88088110)

* Die VM wurde beim aufstarten "soft locked", es passierte nach dem im Bild unten gezeigten nichts mehr, daher konnten wir die Befehle in der VM selbst nicht ausprobieren. Wahrscheinlich passiert das, weil VirtualBox keine richtige Fehlerbehebung implementiert hat, um so etwas zu vermeiden.

"Fehlermeldung" VM: ![image](https://github.com/user-attachments/assets/2b953e30-1ebe-43e9-991f-44cce0438296)
