# H3 Git

## a) Online

Aloitin tehtävän menemällä Githubiin ja Tekemällä uuden varaston joka sisältää README ja GNU General Public License 3 tiedostot.

![github summer](https://user-images.githubusercontent.com/130304789/232325296-08f1bc8e-dca1-45ae-ad8f-192f77f6636e.PNG)






## b) Dolly

Aloitin tekemään tehtävää teron ohjeilla https://terokarvinen.com/2016/publish-your-project-with-github/?fromSearch=publish%20your%20project%20with%20github


sudo apt-get update

![image](https://user-images.githubusercontent.com/130304789/232345785-1cc8a0cf-f5f0-4697-b563-4318f0285b8e.png)

suod apt-get -y install git

![image](https://user-images.githubusercontent.com/130304789/232345896-aefdb255-5142-4768-afff-0b0e0c3a8247.png)

git config --global user.email "bgx175@myy.haaga-helia.fi"

![image](https://user-images.githubusercontent.com/130304789/232346349-3d8c42f8-38bf-4272-91b7-688991b2830e.png)

git config --global user.name "Tiitus Hakkinen"

![image](https://user-images.githubusercontent.com/130304789/232346784-7d84a38a-071b-49ed-99a5-1c7382155c45.png)

git config --global credential.helper "cache --timeout=3600"

![image](https://user-images.githubusercontent.com/130304789/232346910-3eff039f-2317-47d5-b201-42b44df7a645.png)

git clone https://github.com/Tiitus101/Summer.git

![image](https://user-images.githubusercontent.com/130304789/232347175-bba2f242-425a-46f4-a919-dfd137e57141.png)

![image](https://user-images.githubusercontent.com/130304789/232348200-ad4abd55-8776-4a85-b989-8dba53a24c1a.png)


"nano README.md" -komennolla pääsin muokkaamaan tiedostoa. Lisäsin pätkän tekstiä.

![image](https://user-images.githubusercontent.com/130304789/232348590-801cfeab-9418-44cd-98df-7ab675d892cb.png)

git add . && git commit; git pull && git push komento vaati kirjautumisen joka epäonnistui -->  ssh avaimen luonti

Tässä vaiheessa huomasin, että tiedostojen muokkaaminen ei onnistu https:llä sillä github on ottanut pois käytöstä
password autenticationin 13.8.2021. Video jossa tämä kerrottiin ---->  https://www.youtube.com/watch?v=8X4u9sca3Io&ab_channel=VictorGeislinger
Joten aloin tekemään ssh avainta jonka avulla saisin lopulta työnnettyä muutokset läpi.

ssh avaimen luonti. generatesin ensin avaimen jonka syötin githubissa tekemääni ssh avaimeen.

![image](https://user-images.githubusercontent.com/130304789/232350799-0e9c530b-9aae-4042-acd5-97bda82369d4.png)

Tein muutokset uudestaan ja tällä kertaa komento "git add . && git commit; git pull && git push" toimi ja sain tehtyä muutokset.

![image](https://user-images.githubusercontent.com/130304789/232353410-5963d412-b5d1-4aa1-8bff-2355ca33062a.png)

Kävin tarkistamassa weppiliittymästä että muutokset olivat tulleet voimaan.

![image](https://user-images.githubusercontent.com/130304789/232353519-19ab9477-2cd1-43c3-b18e-3ee85b8bdc14.png)



## c) Doh!

Ensin tein muutoksen README.md tiedostoon

![image](https://user-images.githubusercontent.com/130304789/232353914-0044acdd-21fb-4b95-b393-47dc51837a46.png)

Muutokset näkee git diff "tiedoston nimi" - komennolla. 

Tässä omat muutokset.

![image](https://user-images.githubusercontent.com/130304789/232354960-f762eec8-89c3-4be0-ae15-100c5373780b.png)

Ajetaan "git reset --hard" -komento 

![image](https://user-images.githubusercontent.com/130304789/232355876-9cb05257-68d8-4cc8-b465-637171f6c899.png)


Muutokset ovat kadonneet.

![image](https://user-images.githubusercontent.com/130304789/232355769-94ec83a3-7009-4b80-9128-a755bf597657.png)

"git reset --hard" -komentoa pitää käyttää varoen sillä peruutusta ei ole ja Esim. päivien/viikojen/kuukausien työt voi mennä hukkaan.


## d) Tukki

"git log" -komento jolla näkee varaston kaikki commitit joita on tehty. 

Kuvassa näkyy kolme committia joista ensimmäinen on inital commit (alkuperäinen) ja kaksi muuta muokkauksia.
Muokkauksien tekijä on kirjannut mitä muokkauksia on tehnyt commitissaan. git log:in avulla näkyy myös committien julkaisuaika, julkaisijan nimi sekä julkaisian sähköpostiosoite.

![image](https://user-images.githubusercontent.com/130304789/232357426-224b7c2a-1f29-4b83-ad42-8e6b5330b408.png)

Jos ennen committia halua nähdä mitä muutoksia olet tehnyt niin komento: git diff 

![image](https://user-images.githubusercontent.com/130304789/232358513-40539970-0548-4fa2-893c-917bc8e3e199.png)
