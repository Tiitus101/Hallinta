# Komennus

H4 Tehtävät https://terokarvinen.com/2023/palvelinten-hallinta-2023-kevat/

Tein tehtävät kotona omalla läppärillä Lenovo IdeaPad 5 15ALC05. Käyttöjärjestelmänä Windows 10 Home. (Raportti)

Tein tehtävät virtualboxin sisällä Linux koneella. VM koneen käyttöjärjestelmä Ubuntu desktop. (Tehtävät)

## a) Hello.sh

Aluksi tein hello.sh skriptin nanolla (texteditor), jonka jälkeen annoin sille suoritusoikeudet komennolla "chmod +x hello.sh".

![image](https://user-images.githubusercontent.com/130304789/233870869-7612624a-f6da-495f-a17f-d720af195714.png)

Siirsin vielä skripti tiedoston hakemistoon "files"

![image](https://user-images.githubusercontent.com/130304789/233879869-9f160c97-b95c-4e3b-9829-417bf297eaf8.png)


hello.sh sisältö

![image](https://user-images.githubusercontent.com/130304789/233878981-11e43b29-097b-4bf1-9305-12c1e8d6693b.png)

ja lopuksi testasin että toimi

![image](https://user-images.githubusercontent.com/130304789/234040501-cc50b283-bcfe-4323-849b-89135b3daea9.png)


## b) Hello.py

Aloitin tehtävän luomalla hello.py tiedoston.
hello.py tiedoston sisätö.

![image](https://user-images.githubusercontent.com/130304789/233883486-67e62813-05c2-4eef-aeba-2cf3cfe997c7.png)

Tämän jälkeen suoritusoikeudet.

![image](https://user-images.githubusercontent.com/130304789/233884583-9842ee01-290c-47a6-8653-cf4e5f77a7e5.png)


Kokeilin että toimiiko skripti komennolla "hello.py". Skripti ei aluksi toiminut sillä en ollut ansentanut pythonia.

Joten asensin pythonin.

![image](https://user-images.githubusercontent.com/130304789/233883042-d239cab3-c7d6-458c-a6dd-b73f98a35467.png)

Jonka Jälkeen skripti toimi normaalisti.

![image](https://user-images.githubusercontent.com/130304789/233884295-dcc43e16-9776-4206-a37f-651b4477378d.png)




## c) Automatisointi

Tässä tehtävässä minulle tuli monta ongelmakohtaa jonka takia en raportoinut kaikkea raporttiin, mutta sain lopulta ongelmat ratkottua ja 
ohjelmat orjakoneille.

Aluksi käynnistin virtuaalikoneet vagrant up- komennolla jonka jälkeen otin ssh yhteyden master koneeseen vagrant ssh komennolla.

Sitten sijoitin master koneen /srv/salt hakemistoon skripti tiedostot hello.sh ja hello.py


![image](https://user-images.githubusercontent.com/130304789/234015809-e061b041-253a-4e55-86b0-55d440196a45.png)

![image](https://user-images.githubusercontent.com/130304789/234016636-4c2bb35f-d49c-4df1-85a4-88635c2e9d57.png)

![image](https://user-images.githubusercontent.com/130304789/234016761-a4be28de-05bc-425b-8abc-2b72b5eeb80c.png)

Kokeilin vielä lopuksi että skripti toimii orja koneella t001

![image](https://user-images.githubusercontent.com/130304789/234025180-4e5fb50c-0b56-4696-870b-b5b08afa92a4.png)


## d) Asennus

Lähdin asentamaan "Htop" ohjelmaa joka on "top" ohjelman korvaava prosessinvalvonta ohjelma.

Aluksi master koneella lisäsin tiedoston htop.sls masterin /srv/salt hakemistoon.

htop.sls sisältö.

![image](https://user-images.githubusercontent.com/130304789/234036748-7de3d19b-9ade-4b85-b841-8cfdc9e45188.png)

Päivitin Masterin tilat.
Tästä sain vastauksen true molemmilta orjilta joka tarkoittaa että orjat ovat vastaanottaneet päivitykset ja päivittäneet tilat masterilta.

![image](https://user-images.githubusercontent.com/130304789/234037831-7c66e153-0ce2-430e-bdc2-cb7c01cf119d.png)

Sitten suoritin salt tilan orjille. Aluksi epäonnistui, jonka jälkeen sudolla onnistui.

![image](https://user-images.githubusercontent.com/130304789/234038293-91e26136-d793-4c7b-bf02-9677acd8bc08.png)

t001:

![image](https://user-images.githubusercontent.com/130304789/234038623-c9d819d9-20d0-4290-ba4e-13405ce3749f.png)

t002:

![image](https://user-images.githubusercontent.com/130304789/234038783-821ee772-1400-4122-92da-62fa8c3eae13.png)


Testasin vielä että toimi orjilla.
Eli ajoin "htop".

![image](https://user-images.githubusercontent.com/130304789/234039380-2b35d9d2-7b01-45e3-867d-0167998f4981.png)



