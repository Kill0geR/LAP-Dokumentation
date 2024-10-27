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
