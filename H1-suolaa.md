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





