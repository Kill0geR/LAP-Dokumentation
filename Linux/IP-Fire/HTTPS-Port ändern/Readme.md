HTTPS-Port ändern
===
Gib diesen command in ipfire ein

***„iptables -t nat -A PREROUTING -i green0 -p tcp --dport 44443 -j REDIRECT --to-port 444“***

![image](https://github.com/user-attachments/assets/563336d5-d71f-4092-a558-609e97ce733a)

Danach bitte nicht neustarten und einfach den port 44443 benutzen und es sollte alles funktionieren

![image](https://github.com/user-attachments/assets/e8b9b88b-1379-4bdc-a7ce-31f4a33895b8)
