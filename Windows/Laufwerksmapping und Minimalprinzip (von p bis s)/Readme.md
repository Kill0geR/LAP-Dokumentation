Laufwerksmapping und Minimalprinzip (von p bis s bei den "Lernunterlagen")
====

![image](https://github.com/user-attachments/assets/46dd1e6e-72d3-4ace-853c-a9973531041a)

![image](https://github.com/user-attachments/assets/30182417-92af-4c06-9679-522ed2c5e4d4)

![image](https://github.com/user-attachments/assets/a6a21a33-8ea1-4956-a163-21df6b8b8d2e)

![image](https://github.com/user-attachments/assets/4879c158-af12-423a-ba20-7a942912e640)

![image](https://github.com/user-attachments/assets/85a7d153-5bb4-4394-abfa-4587284286d5)

![image](https://github.com/user-attachments/assets/5fc6ccd4-9d8c-4b35-a14d-82c91961ab34)

Rechtsklick auf neue Freigabe

![image](https://github.com/user-attachments/assets/a30e8883-3694-4d55-a7e4-47e45710cd82)

![image](https://github.com/user-attachments/assets/715538f5-7898-4e7d-9bf7-37060819b240)

Den Pfad zu „Temp“ finden

![image](https://github.com/user-attachments/assets/70c4c71e-4a12-4799-86e7-9c05806b99e6)

![image](https://github.com/user-attachments/assets/f6b4f0c9-69cd-40fe-bc46-56a3bc790985)

![image](https://github.com/user-attachments/assets/6b5639d6-99d8-45c2-ba92-a8bbdbdc4004)

![image](https://github.com/user-attachments/assets/6a2f7f67-e34d-493f-b131-79a628c00f77)

Bei Home machen wir das gleiche wie bei Temp jedoch setzen wir bei Home am Ende ein Dollar Zeichen damit die Freigabe versteckt bleibt

![image](https://github.com/user-attachments/assets/7b8a8d89-0232-4752-bcb7-c786bea33c6b)

![image](https://github.com/user-attachments/assets/3faba94c-8843-415e-9c27-f54c215c647d)

Hier macht ihr dann für jedes Verzeichnis eine OU eine OU

![image](https://github.com/user-attachments/assets/7887aaa7-90d4-4207-806b-8d6e958b05f6)

Hier macht ihr dann zwei domänen lokale gruppen und eine globale gruppe. Den Benutzer gibt ihr in die Globale Gruppe und die Globale Gruppe macht ihr ein Mitglied von allen Domänen lokalen gruppen

![image](https://github.com/user-attachments/assets/377865d1-8c76-45b9-adfc-887eed56dbaf)

So sollte das aussehen

![image](https://github.com/user-attachments/assets/d4ee707d-b3d4-488a-ab10-e33ff5344849)

![image](https://github.com/user-attachments/assets/e87d2991-cd9d-444a-a3b5-900b718836a5)

Jetzt geht ihr zurück zu eurem Explorer und macht das hier

![image](https://github.com/user-attachments/assets/20206005-cb03-4d05-8fa8-4cc4b3719f1e)

![image](https://github.com/user-attachments/assets/245ea536-6a16-42a3-814c-7dd3aba0b56e)

![image](https://github.com/user-attachments/assets/206a86fe-631b-433b-90fc-453f585acc11)

Alle bis auf dem Administrator entfernen

![image](https://github.com/user-attachments/assets/540c060c-ac61-472b-9c7f-cb84110f972d)

![image](https://github.com/user-attachments/assets/603377e5-6853-4218-b14a-51c64c930005)

![image](https://github.com/user-attachments/assets/9767979d-02bc-4b0d-aa8f-263431352b6a)

Unter Homeverzeichnes ein Verzeichnis user_management machen

![image](https://github.com/user-attachments/assets/4f4a1acf-4d41-4d05-99be-011584c009d9)

Rechte nur für den User

![image](https://github.com/user-attachments/assets/4cac2649-31de-433e-9da9-37a90afda0d1)

Im Active Directory fenster machen drücken wir dann auf Eigenschaften

![image](https://github.com/user-attachments/assets/75d12c0e-4cb0-4c5b-bc52-dbf911ea0617)

![image](https://github.com/user-attachments/assets/0ca1c7d9-7d66-4bdc-9612-4cc41a2d3ecc)

Hier kopieren wir den Pfad und fügen ihn beim Profil ein

![image](https://github.com/user-attachments/assets/7ded70d5-943f-4250-8477-ba056666ab57)

![image](https://github.com/user-attachments/assets/48d29e77-8a4d-4161-b797-a541d33b08f8)

![image](https://github.com/user-attachments/assets/eebc1d96-80d8-4177-9ce3-dceaf08521dc)

Rechtsklick auf „LAP.intern“

![image](https://github.com/user-attachments/assets/c8efb299-2c16-4619-9c95-f661a9969c34)

In Daten erstellen wir eine neues Verzeichnis namens „Script“ und in dem Verzeichnis erstellen wir eine neue Datei „script.txt“
In der Datei schreiben wir „net use T: (Den Pfad vom temp Verzeichnis)“

![image](https://github.com/user-attachments/assets/abb7e5f9-f962-43c8-b25f-85cb32b6c369)

![image](https://github.com/user-attachments/assets/2f5448c8-34f7-4822-8fbd-e2faf8db24a7)

So sieht es dann am Ende aus

![image](https://github.com/user-attachments/assets/315c2399-0ddc-4ed7-8eda-8c3fbb749cd1)

![image](https://github.com/user-attachments/assets/65b3a7c7-6372-4e20-87d1-9060ae996367)

„script.bat“ und dann auf „Alle Dateien“ umstellen

![image](https://github.com/user-attachments/assets/a5e531e1-cbb9-4ee9-bc8f-632d4301c2d0)

![image](https://github.com/user-attachments/assets/5fcad8bd-5f66-4c8c-98b6-49e84a39ce51)

![image](https://github.com/user-attachments/assets/370e3f57-544c-40c9-9102-d3d95912e82b)

![image](https://github.com/user-attachments/assets/605fd5f1-250b-43cc-b08e-de29a67e72be)

![image](https://github.com/user-attachments/assets/f4b5dc79-3895-4e6d-bc12-6edff20bcca4)

![image](https://github.com/user-attachments/assets/19693bb3-9f57-47c1-a7a1-38c0e5abb037)

Wenn ihr euch mit dem User anmeldet sollte das so ausschauen

![image](https://github.com/user-attachments/assets/8d07b9f9-9b77-47f5-bbb2-851ad25912c1)

Wenn das nicht funktioniert dann macht ihr einfach ein script wieder mit bat Funktion und schreibt dann wieder „net use T: (Den Pfad vom temp Verzeichnis)“ und führt dann dieses Script aus
