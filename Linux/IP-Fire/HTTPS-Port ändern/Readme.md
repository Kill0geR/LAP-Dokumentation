HTTPS-Port ändern
===


Um den HTTPS-Port zu ändern müsst ihr die ersten eine SSH Verbindung zulassen

![image](https://github.com/user-attachments/assets/2422e91f-802e-4eb1-81f1-100b9370cf21)

Hier klickt ihr nun auf alle checkboxes die hier sind

![image](https://github.com/user-attachments/assets/d8df2d46-a99b-4040-9a0f-06973600f870)

Danach geht ihr in den Terminal und verbindet euch mit ipfire 

![image](https://github.com/user-attachments/assets/34ca2d8d-7744-41e3-96d9-9ddcf51b8875)

Danach gibt ihr diesen Command ein

***„iptables -t nat -A PREROUTING -i green0 -p tcp --dport 44443 -j REDIRECT --to-port 444“***

![image](https://github.com/user-attachments/assets/563336d5-d71f-4092-a558-609e97ce733a)

Danach bitte nicht neustarten und einfach den port 44443 benutzen und es sollte alles funktionieren

![image](https://github.com/user-attachments/assets/e8b9b88b-1379-4bdc-a7ce-31f4a33895b8)
