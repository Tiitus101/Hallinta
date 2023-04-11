# H1 Suolaa

## x)

- Oman verkkosivun julkaisu (Github)

- Repositoryt (Projektiin liittyvät tiedostot)

- Yksinkertainen ja helppokäyttöinen

- Useiden koneiden kontrollointi ja kofigurointi

- Kolme konetta (2 orjaa ja 1 Master)

Tein tehtävät kotona omalla läppärillä Lenovo IdeaPad 5 15ALC05.
Käyttöjärjestelmänä Windows 10 Home.
Tein teheävät kuitenkin linux koneella virtualboxin sisällä. 
VM koneen käyttöjärjestelmä Ubuntu desk.

## a) 

Aluksi ajoin uudella koneella komennot "sudo apt-get update" jolla hain uusimmat paketit ja "sudo apt-get upgrade" jolla latasin ja asesin ne. 
Nämä komennot kannatta ajaa aina uudella koneella.

![image](https://user-images.githubusercontent.com/130304789/230974544-8a578297-ddf3-43c1-825a-d77abd0d952b.png)
![image](https://user-images.githubusercontent.com/130304789/230975347-3252b3a7-1b6c-49dc-ac2b-c885e47736b0.png)


Asensin Virtual boxin ja vagrantin komennolla "sudo apt-get -y install virtualbox vagrant micro"
Kirjoitusvirheen takia komento epäonnistui aluksi mutta huomasin sen ja korjasin virheen jonka jälkeen asennus alkoi.

![image](https://user-images.githubusercontent.com/130304789/230976838-5303ac53-e460-4460-9151-f7e65cd846b0.png)


## b)

Loin uuden directoryn "saltdemo" komennolla "mkdir saltedmo" jonka jälkeen siirryin tähän directoryyn jossa micro text editorilla 
tein konfiguraatio asetukset jotka kopioin ohjeesta Teron sivuilta. # Copyright 2014-2023 Tero Karvinen http://TeroKarvinen.com
Text filessä on konfiguraatiot kahdelle slave koneelle ja yhdelle master koneelle.

![image](https://user-images.githubusercontent.com/130304789/231009866-ac5c7df3-c6c5-4e0f-869e-03640bcdba43.png)

Tämän jälkeen tuli ensimmäinen ongelma.
Yritin saada koneet päälle komennolla "vagrant up" sain vastaukseksi virhekoodin 

![image](https://user-images.githubusercontent.com/130304789/231011774-025eb704-af63-4295-bb07-a9dd06464640.png)

Tämän ongelma korjasin muuttamalla koneiden ip-osoitteita.
Tämän jälkeen yritin käynnistää koneet uudestaan mutta nyt tuli toinen ongelma.

En tajunnut ottaa ongelmasta kuvakaappausta mutta errori oli seuraavan lainen: AMD-V is not available (verr_svm_no_svm).
ongelma liityi jotenki prosessoriin. Yritin aluksi vaihtaa biosissa olevia asetuksia, mutta 
se ei toiminut. Loppujen lopuksi löysin VirtualBoxin prosessori asetuksista oikean asetuksen
joka piti laittaa päälle.

![image](https://user-images.githubusercontent.com/130304789/231021793-fe554b6d-5c62-4d4a-91c9-8943219f6365.png)

Tämän jälkeen sain koneet onnistuneesti päälle.
Testasin vielä koneita ottamalla niihin ssh yhteyden komennoilla "vagrant ssh" ja
"vagrant ssh t001"

![image](https://user-images.githubusercontent.com/130304789/231022714-0ccb8cd7-d909-4bf5-9771-59dd3d13fd52.png)

## c)

Seuraavaksi oli vuorossa orjien avaimien hyväksyminen. Avaimet hyväksyin komennolla
"sudo salt-key -A"

![image](https://user-images.githubusercontent.com/130304789/231023926-8f82928d-276a-4e54-bbde-6f92641da4ce.png)

Pingi testi:

![image](https://user-images.githubusercontent.com/130304789/231024336-be2d6930-7d82-4c94-82ea-7fcbd0971683.png)

## d)

Apache2 asennus orjille:

![image](https://user-images.githubusercontent.com/130304789/231029865-d936b530-6c09-4317-afcc-71676dac811f.png)

![image](https://user-images.githubusercontent.com/130304789/231029952-7eeee9b4-a229-4057-b411-9d02f8c8cc50.png)

Service running:

![image](https://user-images.githubusercontent.com/130304789/231030413-56785993-83c4-4803-8111-46a92c2d4d6a.png)

Uuden filen luonti:

![image](https://user-images.githubusercontent.com/130304789/231031005-f76637ef-67e4-434e-ba82-2b23dd6e1ef3.png)

User:

![image](https://user-images.githubusercontent.com/130304789/231031780-05446025-7966-479c-ac9d-9efcb17ebccf.png)


# Infra as Code


![image](https://user-images.githubusercontent.com/130304789/231038547-9ee7b9ca-97f3-40b0-a0b4-4d7faf5e6f5f.png)
