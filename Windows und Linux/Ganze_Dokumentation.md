Adressreservierung für Linux-Client
===

Wichtig ist das der Linux-Client im selben Netz ist wie der Server

![image](https://github.com/user-attachments/assets/562c695c-e767-479b-9957-ad97cfa63185)

In Linux angekommen öffnet ihr den Terminal mit der Tastenkombination **„Strg+Alt+T“** und schreibt **„ip a“** in den Terminal rein. Danach kopiert ihr euch die Mac-Adresse und geht zu eurem Windows Server.

![image](https://github.com/user-attachments/assets/2088fe4e-8b17-4618-a82b-ba21f9345444)

In Windows geht ihr dann auf **„DHCP“** und wählt die Option **„Reservierungen“** aus

![image](https://github.com/user-attachments/assets/678c4cb0-ace0-412e-ad72-8de3bec854f6)

Hier macht ihr einen Rechtsklick und klickt auf „Neue Reservierung“.

Jetzt geben sie die gewünschte IP-Adresse und die Mac-Adresse des Linux-Clients an. WICHTIG anstatt dem Doppelpunkt wird ein Beistrich hinzugefügt!! Vergesst dann nicht auf DHCP zu klicken

![image](https://github.com/user-attachments/assets/a3961671-188e-456e-a919-e21ab973336e)

Danach sollten eure **„Adressleases“** so aussehen 

![image](https://github.com/user-attachments/assets/37b56e8e-4ea8-4e30-a30e-74f4ad12d37d)

Bereichsoptionen beim DHCP
===

Falls du etwas vergessen hast beim DHCP hinzuzufügen kannst du sie immer nachjustieren

![image](https://github.com/user-attachments/assets/3549454c-b7da-411c-835a-7cdb1e8ae3be)

Client pingen, ohne die Firewall auszuschalten
===

Um den Client zu pingen ohne die Firewall auszuschalten muss man erst in die Firewall Einstellungen gehen

![image](https://github.com/user-attachments/assets/4ec9a637-bb15-4a97-81ec-64e6cd0f071e)

Danach muss in den Eingehenden Regeln diese zwei Regeln aktiviert werden

![image](https://github.com/user-attachments/assets/fc56bd4f-c9a4-4a01-985b-799c87f8ae0c)

Computername ändern bei Windows Client
===

Das ist meine Version es gibt natürlich etliche Version.
Drück die Tastenkombination „Win+i“ und gehe auf System

![image](https://github.com/user-attachments/assets/54d8af67-aef7-4ba8-a05f-1e4cfb120603)

Runterscrollen und auf Info drücken

![image](https://github.com/user-attachments/assets/f27e85e9-b22c-4192-9a36-98eda4baaf6e)

![image](https://github.com/user-attachments/assets/3e303b30-1f0c-4cf4-b934-bd04762a0196)

![image](https://github.com/user-attachments/assets/6d88030c-f4da-475e-a6de-165014c0b221)

![image](https://github.com/user-attachments/assets/0cb6f0af-9194-4b5e-a1b8-75454d7a41ae)

DHCP-Server einrichten
===

Unter Rollen und Features klickt ihr dann auf DHCP-Server 

![image](https://github.com/user-attachments/assets/3f17fece-a582-4b2d-8b71-90953c929b27)

Wieder hier auf der zweiten Seite alles freilassen und dann auf Installieren drücken
Nach der Installation müssten dann hier klicken

![image](https://github.com/user-attachments/assets/9989f3e1-ff87-4dd4-b7f6-66faac680938)

Dann auf **„Commit ausführen“** und **„Schließen“** klicken.

![image](https://github.com/user-attachments/assets/bbfbcb9d-70ea-4dbf-b1c3-2c113edf6c43)

Unter **„Tools“** dann klickt ihr dann auf **„DHCP“**

![image](https://github.com/user-attachments/assets/674406bb-df61-4274-9993-460b34f49d96)

Rechtsklick auf **„IPV4“** und dann auf **„Neuer Bereich“** klicken

![image](https://github.com/user-attachments/assets/76bc62f2-4152-4d3f-bd00-abffdb871248)

Nachdem ihr den Namen eingegeben habt müsst ihr die Start- und End-IP-Adresse eingeben

![image](https://github.com/user-attachments/assets/f4683a9e-560c-4213-b826-c2da24506515)

Danach einfach machen was gefragt ist

DNS einrichten nach der Hochstufung
===

Da du der Server ein Domänencontroller ist wurde die Forwad-Lookupzone schon eingerichtet. Jetzt fehlt nur noch die Reverse-Lookupzone 

![image](https://github.com/user-attachments/assets/ded123e6-c7e0-4312-b049-c9ff0fd96558)

Immer auf weiter drücken und dann hier die ersten 3 stellen der internen IP-Adresse eingeben

![image](https://github.com/user-attachments/assets/b3a26609-c28c-4169-baa8-62e3121bda2d)

In der Reverse-Lookupzone muss man dann einen PTR-Eintrag machen

![image](https://github.com/user-attachments/assets/1ab7af36-59ce-48d3-9a2a-71fc48a7170a)

Auf **„Durchsuchen“** klicken und seinen Server finden

![image](https://github.com/user-attachments/assets/cce3d68f-390e-4a45-92c2-22025301ae1d)

![image](https://github.com/user-attachments/assets/a710d3d4-c721-4569-9b6e-168bd907113b)

Gasterweiterung in der VM installieren
===

Klicke links oben in der VM auf **„Geräte“** und dann auf **„Gasterweiterungen einlegen“**

![image](https://github.com/user-attachments/assets/50e17c9c-96c4-4257-a8e2-f00ded46ee70)

Nachdem ihr auf **„Gasterweiterungen einlegen“** geklickt habt schließt ihr den Explorer und öffnet ihn dann wieder. So sollte der Explorer nun aussehen

**Vorher**

![image](https://github.com/user-attachments/assets/2cc60327-9f6d-460a-a00f-7953e98f1096)

**Nachher**

![image](https://github.com/user-attachments/assets/e69dca45-683c-4602-8fc7-d65e8f90653b)

Klickt jetzt auf **„CD-Laufwerk (D:) VirtualBox Guest Additions“** und wählt die Version, die mit **„amd64“** endet.

![image](https://github.com/user-attachments/assets/5df95bcd-e2f0-4a55-88cb-4092dd30bd32)

Klick euch durch und startet die VM neu

Laufwerk C umbenennen
===

Öffne den Explorer und mache einen Rechtsklick auf **„Lokaler Datenträger (C:)“** und klicke auf **„Umbenennen“**

![image](https://github.com/user-attachments/assets/6dea4d51-d95b-4b82-8a53-ff2a805d9f17)

Netzwerkadapter hinzufügen
===

Klicke in VirtualBox auf das Zahnrad

![image](https://github.com/user-attachments/assets/16ebb992-5c08-4f8a-87d9-fb2f52c858cf)

Dann auf Netzwerk und einen weiteren Adapter hinzufügen

![image](https://github.com/user-attachments/assets/21e960ab-c75d-4121-96b1-9932cf28b98e)

Netzwerkdrucker einrichten (Windows)
===

Um einen Netzwerkdrucker einzurichten müssen wir unter **„Rollen und Features hinzufügen“** **„Druck- und Dokumentdienste“** anklicken

![image](https://github.com/user-attachments/assets/0e0ffb37-45b3-4741-b039-7243462cce6d)

Druckserver hier anklicken

![image](https://github.com/user-attachments/assets/db9f36c4-c58d-4c7c-a115-d80c9e3a3877)

Unter **„Tools“** auf **„Druckerverwaltung“**

![image](https://github.com/user-attachments/assets/b3bb2047-40cd-486e-96ef-0cf326324985)

Macht einen Rechtsklick auf **„Drucker“** und klickt **„Drucker hinzufügen“**

![image](https://github.com/user-attachments/assets/e6da23d3-5112-48ce-9f13-bf22ef2905ba)

![image](https://github.com/user-attachments/assets/947c980f-7613-4380-975f-9d4a900e5661)

![image](https://github.com/user-attachments/assets/0ad2ade3-59d2-45a5-85d0-5217a331cd9e)

![image](https://github.com/user-attachments/assets/cc8eabf0-75c3-42d7-80af-1c88ddedd798)

![image](https://github.com/user-attachments/assets/1828a7d5-0c0a-43d9-ae1f-afd02e8dd50d)

Hier ist es egal was ihr nimmt

![image](https://github.com/user-attachments/assets/8ada4d70-e984-41a4-98f8-a182ba4715da)

![image](https://github.com/user-attachments/assets/482da7a5-0781-4fc5-854d-1450a15cc7d8)

Netzwerkkarten umbenennen
===

Führt die Tastenkombination **„Win+R“** aus und schreibt **„ncpa.cpl“** in die leiste danach einen Rechtsklick auf die Netzwerkkarte und dann auf Umbenennen drücken. (Kleiner Tipp: Wenn ihr mehrere Netzwerkkarten umbenennen wollt dann macht es nacheinander sonst wiest ihr nicht welche Netzwerkkarte welche ist!!)

![image](https://github.com/user-attachments/assets/092f8212-ee63-4404-b75d-5c7b8fef4425)

Neues Volumen erstellen
===

In den Einstellungen geht ihr dann auf Massenspeicher und drückt auf dieses Zeichen

![image](https://github.com/user-attachments/assets/120a6659-0642-4b83-a979-e3468743827f)

![image](https://github.com/user-attachments/assets/c727d577-3015-4d97-b893-02ecc3f628fa)

![image](https://github.com/user-attachments/assets/686214d8-247c-44da-b160-9af90437cc9a)

![image](https://github.com/user-attachments/assets/db062618-d685-4af7-9000-b9ce672818e3)

![image](https://github.com/user-attachments/assets/211d2b8b-021d-48fc-b3b7-2b83ce8864ac)

Wenn ihr dann auf Fertigstellen geklickt habt ist es wichtig hier eure Festplatte auszuwählen und auf **„Auszuwählen“** zu klicken

![image](https://github.com/user-attachments/assets/41154b44-9486-42c8-a586-2655fb03285f)

Zurück in eurem Server müsst ihr einen Rechtsklick auf das Windows-Logo machen und auf **„Datenträgerverwaltung“** klicken

![image](https://github.com/user-attachments/assets/ac1375b0-3d0a-4518-b455-d1bf01d381d9)

Hier dann bitte MBR wählen

![image](https://github.com/user-attachments/assets/dc7ba55f-5021-4214-b636-b3bfa7c64966)

Hier bitte runterscrollen und einen Rechtsklick auf den Schwarzen Balken machen

![image](https://github.com/user-attachments/assets/00e013a8-6eb1-4ef0-b7e7-453508693710)

Und dann auf den Anforderungen entsprechend die Sachen auswählen

Passwort auf dem Server ändern
====

Rechtsklick auf das Windowssymbol dann auf Computerverwaltung klicken

![Screenshot 2024-10-26 172944](https://github.com/user-attachments/assets/49b8d16f-be6b-4b2f-9bf6-dacba83c014d)

In der Computerverwaltung angekommen drücken wir dann auf **„Lokale Benutzer und Gruppen“** und dann auf **„Benutzer“**

![image](https://github.com/user-attachments/assets/157ff9a8-bb5c-4183-9641-c63ca55ea54f)


Hier machen wir jetzt einen Rechtsklick auf **„Administrator“** und wählen **„Kennwort festlegen“** aus. Danach bitte auf **„Fortsetzen“** drücken und ihr könnt euer neues Kennwort festlegen.
![image](https://github.com/user-attachments/assets/db0a26d2-294f-4113-8fed-7bcd373cbbab)

So sollte es dann aussehen

![image](https://github.com/user-attachments/assets/46cd7f6a-c251-454f-918b-aa17720fad8e)


Rolle „Dateiserver“ hinzufügen
===

Geht wieder auf Rollen und Features hinzufügen. Und Klappt **"Datei-/Speicherdienste zweimal"** auf

![image](https://github.com/user-attachments/assets/f0b809f5-30c2-44cd-ae38-ff0f5658b2f6)

Routing und RAS aktivieren
===

Klickt rechts oben auf **„Verwalten“** und dann auf **„Rollen und Features hinzufügen“**

![image](https://github.com/user-attachments/assets/0a0fb96f-85b3-45e0-aeba-8423c65eaf18)

Nachdem müsst ihr dann die Rolle **„Remotezugriff“** herunterladen. Nachdem ihr auf weiter gedrückt habt lässt ihr die zweite leer also nichts anklicken und einfach auf weiter klicken!!

![image](https://github.com/user-attachments/assets/285bd9e0-ffb5-41f4-9282-d026222d1782)

Jetzt auf **„Routing“** drücken und der Rest wird automatisch ausgewählt

![image](https://github.com/user-attachments/assets/3bdf8233-a83b-4ac8-ae0f-fbf0ee6b1e8f)

Danach einfach weiter drücken und ihr seid fertig.

Unter Tools findet ihr die Option **„Routing und RAS“**

![image](https://github.com/user-attachments/assets/7ba38c3b-5b61-44aa-9f6f-b57f89844b69)

Rechtsklick auf **„DC-LAP-2“** dann auf **„Routing und RAS konfigurieren und aktivieren“** klicken.

![image](https://github.com/user-attachments/assets/1828037d-fdc3-447e-a701-37bb0ec54449)

Danach auf **„Netzwerkübersetzung (NAT)“** klicken

![image](https://github.com/user-attachments/assets/f00934d0-ef60-409c-92fc-468a61066098)

Danach wählt ihr hier bitte die **„EXTERNE Netzwerkkarte“** aus!!!

![image](https://github.com/user-attachments/assets/8339c9b8-acf3-40fd-8dde-aa24279989a0)

Dann immer weiter klicken. Und wenn ihr hier ankommt, dann einfach warten dass kann immer ein bisschen dauern

![image](https://github.com/user-attachments/assets/d0f11905-cc92-47e8-a0c5-bcf2525f2333)

Wichtig ist das hier dann ein grünes Hackerl ist

![image](https://github.com/user-attachments/assets/107115a5-eb7f-43f2-a36e-64836980058c)

Server zum Domänen Controller hochstufen
===

Unter Rollen und Features **„Active-Directory-Domänendienste“** auswählen

![image](https://github.com/user-attachments/assets/07c097d7-ff57-477f-99d2-1ed8bc028163)

Die zweite Seite leer lassen und auf Installieren klicken

Wenn ihr mit Installation fertig seid, müsst ihr hier dann auf diesen Button drücken

![image](https://github.com/user-attachments/assets/c823be6a-8025-4e59-9b73-603c0ee3a7dd)

Hier ist es wichtig eine neue Gesamtstruktur zu erstellen

![image](https://github.com/user-attachments/assets/168cca19-660a-40c1-86c9-ebfaa5045fa1)

![image](https://github.com/user-attachments/assets/d7856a51-82c7-4375-b57a-fb24aead58e3)

![image](https://github.com/user-attachments/assets/2bd28ebd-7810-498f-beab-48fe6b8f23e9)

Der NET-Bios Name wird automatisch festgelegt

![image](https://github.com/user-attachments/assets/8ca6e59e-8df4-4cc3-91fa-dbb76f9a16fa)

Nachdem der Server hochgestuft wurde ist es wichtig den DHCP-Server zu autorisieren (Hier steht normal Autorisieren anstatt Autorisierung aufheben)

![image](https://github.com/user-attachments/assets/62f8b239-4441-4f62-8cf4-8f490141f44d)

Verstärkte Sicherheitskonfiguration für IE für Administratoren deaktivieren
===

Öffnet den Server-Manager und klickt auf **„Lokaler Server“**

![image](https://github.com/user-attachments/assets/02a8085f-6bad-4759-9dfd-400cfffaad7d)

Danach drückt ihr bei der Option **„Verstärkte Sicherheitskonfiguration für IE“** auf **„Ein“**

![image](https://github.com/user-attachments/assets/490b26e2-990f-498d-a601-c3a658873073)

Hier könnt ihr dann euere Optionen auswählen. In unserem Fall müssen wir die Option für Administratoren deaktivieren

![image](https://github.com/user-attachments/assets/55d85694-0787-41fc-90fb-5ae6f1f1a84e)

Schließt und öffnet den Server Manager wieder damit dass hier angezeigt wird.

![image](https://github.com/user-attachments/assets/18b452a8-704c-42ec-9499-5a7cc3ee135e)

Ausländische Seiten blockieren
===

Damit ausländische Seiten nicht erreichbar sind muss man auf **„Firewall“** und dann auf **„Location Block“** klicken

![image](https://github.com/user-attachments/assets/66eff4f5-a067-44f4-a5b5-9fcc4a33ef45)

Nachdem ihr alle Länder, die ihr blockieren wollt angeklickt habt müsst ihr runterscrollen und auf **„Save“** klicken

![image](https://github.com/user-attachments/assets/cd38dca1-e604-4843-bdd6-865db0ac5a75)

Damit die Regel wirklich funktioniert müsst zurück zu den Firewall Regeln und auf **„Apply Changes“** klicken

![image](https://github.com/user-attachments/assets/8983a952-2f95-4a9d-8bcc-c7132b60782e)

![image](https://github.com/user-attachments/assets/2fe35b57-85d4-457f-9609-6c399c15e33c)

Backup-Datei erstellen
===

Um eine Backup-Datei zu erstellen, müsst ihr auf **„System“** und dann auf **„Backup“** klicken.

![image](https://github.com/user-attachments/assets/c368bec9-da29-4107-b32b-42ee65cdf446)

Hier angekommen drückt ihr auf **„Include log fiels“** und klickt auf das kleine **„weiße Symbol“**. Danach ladet ihr die Datei runter in dem ihr auf das **„orange Symbol“** klickt.

![image](https://github.com/user-attachments/assets/95346e6b-9de4-43f4-ba07-be9f13202f11)

Firewall Regeln
===

Um in die Firewall Regeln hineinzukommen, müssen wir auf **„Firewall“** und **„Firewall Rules“** gehen 

![image](https://github.com/user-attachments/assets/b10d3f07-50b9-407d-9736-6126e6b95900)

Jetzt müssen wir auf **„New rule“** klicken

![image](https://github.com/user-attachments/assets/8a35b88c-acef-4dc3-b5ae-773c8cc42c4f)

Hier können wir dann je nach den Anforderungen die Regeln einstellen.
(Extern – Rot, Intern – Green, DMZ – Orange)

![image](https://github.com/user-attachments/assets/456e6575-6703-4d02-bcd6-dfb3341a59bb)

Hier ist wichtig das ihr bei der Quelle und bei dem Ziel immer auf **„Standard Networks“** seid.

![image](https://github.com/user-attachments/assets/c3d38529-b79a-4372-bcd0-d8271c4bb983)

Wichtig ist hier das wir beim Protocol die Portnummer immer in das Feld **„Destination Port“** eingeben


HTTPS-Port ändern
===


Ich habe versucht den https Port zu ändern und habe es leider nicht geschafft jedoch könnt ihr diesen Screenshot bei der Prüfung einfügen.
Zuerst geht ihr auf den IP-Fire Terminal und schreibt **„nano /etc/httpd/conf/listen.conf“** 

![image](https://github.com/user-attachments/assets/9f835868-7bff-449d-9c4c-380e82b36d12)

Hier könnt ihr dann den Port ändern und den Server neustarten (Hoffentlich funktioniert es bei euch)

![image](https://github.com/user-attachments/assets/b9a73ad4-d101-4157-9f52-fd106f272245)

Spiele (Gambling)  Websites blocken
===

Um solche Sachen zu blocken, müsst ihr auf **„Network“** und dann auf **„URL Filter“** klicken

![image](https://github.com/user-attachments/assets/61bcefcf-cea4-4474-808d-6891992e17de)

Hier könnt ihr dann das Blocken was gefragt ist

![image](https://github.com/user-attachments/assets/03db3282-b8c4-42d1-be93-924238450195)

Scrollt wieder runter und klickt auf „Save“

![image](https://github.com/user-attachments/assets/bd235e60-e85b-4624-80d9-9f813ad9d6ae)

Zeit einstellen
===

Man kann den Verkehr je nach Zeit erlauben oder verhindern das geht hier in dem ihr den Checkpoint **„Use time constraints“** anklickt

![image](https://github.com/user-attachments/assets/e4635b98-94b7-4309-bbda-ec026c3f5607)

Wenn ihr fertig seid, dann klickt auf **„Add“**

![image](https://github.com/user-attachments/assets/dba04b3e-326a-48d9-9978-0575f3f8bbba)

Scrollt dann ganz hoch und klickt auf **„Apply Changes“** sonst werden eure Änderungen nicht angenommen

![image](https://github.com/user-attachments/assets/28b54fc8-c72f-4cef-b25d-b8ca99b7046a)

Zeitserver ändern
===

Um den Zeitserver zu ändern, müsst ihr auf **„Services“** und dann auf **„Time Server“** klicken

 ![image](https://github.com/user-attachments/assets/aacf9e40-7ea6-4c78-af5d-c4099f5cdd34)

Hier könnt ihr dann den Timeserver ändern. Vergesst nicht unten auf **„Save“** zu klicken

![image](https://github.com/user-attachments/assets/3df744dd-8a56-475e-a4e6-4a610c66b912)

Benutzer anlegen und Benutzer deaktivieren
===

Mit dem Befehl **„sudo adduser Anton.Steiner –allow-bad-names“** fügst du einen User hinzu

![image](https://github.com/user-attachments/assets/6cbe80a2-722b-40cc-a753-dd3130cc3feb)

Mit diesem Befehl Deaktivieren sie den Benutzer wieder

![image](https://github.com/user-attachments/assets/4fb216f8-5aab-451b-8029-0e139b1c4075)

Hostname ändern
===

Den Hostname änderst du mit dem Command **„sudo hostnamectl set-hostnamectl Name“**

![image](https://github.com/user-attachments/assets/5e967759-0051-43db-8a11-0097a53ee746)


IP-Konfiguration, freien Arbeitsspeicher und freien Speicher in eine Datei einfügen
===

Um die IP-Adresse zu bekommen, muss man den Befehl **„ip a“** in den Terminal eingeben
Um den freien Arbeitsspeicher zu bekommen, muss man den Befehl **„free -h“** in den Terminal eingeben
Um den freien Speicher zu bekommen, muss man den Befehl **„df -h“** in den Terminal eingeben

Öffnet zwei Terminals und fügt die Ausgaben der Befehle in eine Textdatei. 
Also auf der linken Seite habe ich meine Befehle und auf der rechte Seite habe ich die Textdatei die ich mit **„nano Sysinfo.txt“** öffne. Man kopiert Sachen aus dem Terminal mit **„Strg+SHIFT+C“** und fügt Sachen mit *„Strg+SHIFT+V“** ein

![image](https://github.com/user-attachments/assets/ea612cbf-f588-4237-9b9a-2a8f2dcc6aec)

Am Ende sollte die Datei so aussehen (Wir speichern die Datei mit **„Strg+X“** dann **„y“** und **„ENTER“** drücken

![image](https://github.com/user-attachments/assets/cac6a3ae-c4f7-4dc0-a9a4-a147f71338b8)


Linux Server in DMZ einbinden
===

Wichtig ist das der Linux Server im **„DMZ“** Netz ist.

![image](https://github.com/user-attachments/assets/ec7d1f89-f741-48fb-981b-9176ec532981)

Zuerst geht ihr in das Verzeichnis netplan mit dem Befehl **„cd /etc/netplan“** dann ändert ihr die Datei mit **„sudo mv 50-cloud-init.yaml 50-cloud-init.yaml.bak“** danach erstellst du eine Datei mit dem Befehl **„sudo nano static.yaml“**.

![image](https://github.com/user-attachments/assets/87623566-f6c6-48ff-8f30-b0dd90a2eee0)

Dann fügst du diesen Code hinzu 
```yaml
network:
  version: 2
  renderer: networkd
  ethernets:
    enp0s3:
      dhcp4: no
      addresses:
        - 192.168.15.99/24
      routes:
        - to: default
          via: 192.168.15.1
```

![image](https://github.com/user-attachments/assets/c676e78c-8083-4695-8438-e8e44b309c98)

(man verlässt **„nano“** in dem man **„Strg+X“** drückt dann **„y“** dann **„ENTER“** drükt)

und führst den Befehl **„sudo netplan apply“** aus. Nach einem Neustart sollte die Ip-Adresse eingezeichnet sein

![image](https://github.com/user-attachments/assets/7f68a023-16b1-456d-9fb2-1c415a5ef68f)

So sieht es nach dem neustart aus

![image](https://github.com/user-attachments/assets/b0607c10-ef6e-467f-b01e-f1e3fc4bb37b)

Passwort ändern
===

Gehe mit der Tastenkombination **„Strg+T“** in den Terminal und schreibe **„sudo su“** danach schreibst du **„sudo passwd root“** und änderst das passwort

![image](https://github.com/user-attachments/assets/f31e54aa-fa02-47c5-8e34-5d06ee4729de)

