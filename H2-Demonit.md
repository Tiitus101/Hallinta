# H2 Demonit

Tein tehtävät kotona omalla läppärillä Lenovo IdeaPad 5 15ALC05. Käyttöjärjestelmänä Windows 10 Home. (Raportti)

Tein tehtävät virtualboxin sisällä Linux koneella. VM koneen käyttöjärjestelmä Ubuntu desktop. (Tehtävät)

## x)

- Daemonien kontrollointi saltilla

- Create ssh state (sshd.sls, sshd_config)   -->  apply state (state.apply)  -->  Test ($ nc -vz)

- install, replace, restart


## a)

OpenSSH asennus

![image](https://user-images.githubusercontent.com/130304789/234930711-cab268ef-6407-4d41-ae7c-bb41b942b3f8.png)

![image](https://user-images.githubusercontent.com/130304789/234930813-4a61ca8c-5109-47c5-aeb8-e61ceffa3b12.png)


/etc/ssh hakemistosta löytyvän sshd_config tiedoston muokkaus (portin lisäys).
Tiedoston sisältö:

![image](https://user-images.githubusercontent.com/130304789/234946765-b1e65890-40aa-4ed5-a4d8-6d397e5b306f.png)

Nyt toimii kahdella portilla 22 ja 2222

![image](https://user-images.githubusercontent.com/130304789/235530409-8456b7c2-1532-454b-85c0-1576f1121731.png)

Tässä kohtaa yrittäessäni yhdistää ssh-palvelimelle minulle tuli ongelmia liittyen public keyn kanssa. Minulla meni muutama tunti yrittäessäni ratkaista ongelmaa. Ongelman ratkomisen raportoiminen olisi ollut painajaista sillä se kesti niin kauan joten jätin sen raportoimatta. Lopulta kuitenkin pääsin yhdistämään. 


## b)

Koneet päälle ja masterille ssh yhteys

![image](https://user-images.githubusercontent.com/130304789/234932678-95ced5c6-659e-4882-9f84-3101b40052ce.png)

![image](https://user-images.githubusercontent.com/130304789/234932839-ac0ca1fe-0a47-48f3-a223-f7a89bf02889.png)



![image](https://user-images.githubusercontent.com/130304789/235554131-0315b6c7-1a53-4f25-9906-698eaf577a6e.png)

Masterilla sshd_config tiedosto. tiedosto otettu https://terokarvinen.com/2018/pkg-file-service-control-daemons-with-salt-change-ssh-server-port/?fromSearch=salt%20ssh

![image](https://user-images.githubusercontent.com/130304789/236050327-7a44a7df-c005-4505-b0e1-a687a3add7d1.png)

ja sshd.sls

![image](https://user-images.githubusercontent.com/130304789/236089137-f67a076a-8ea3-4d68-af3f-ecea9bbfbe10.png)

ja ajetaan sudo salt '*' state.apply sshd

![image](https://user-images.githubusercontent.com/130304789/236089369-8d727f0f-56f5-49d7-b893-2f02003481e1.png)


![image](https://user-images.githubusercontent.com/130304789/236089570-4ef7c4b4-949e-43b7-8cae-7f6ab9f05db9.png)


![image](https://user-images.githubusercontent.com/130304789/236089666-4f098cde-50c2-47f4-be6e-d4b1520cfdec.png)


## c) 

Uudet portit mukaan 

![image](https://user-images.githubusercontent.com/130304789/236090554-6b90d0d7-47e4-4e31-be81-6751ca41e7bd.png)

Uudet lisäykset:

![image](https://user-images.githubusercontent.com/130304789/236090793-999a8589-e470-4b91-b46c-0afed8b3dde7.png)


![image](https://user-images.githubusercontent.com/130304789/236090840-6e07cee5-6799-4867-8ace-b89954f59059.png)


![image](https://user-images.githubusercontent.com/130304789/236091055-60518d83-bca5-4266-9f8d-b17e3d9308b6.png)



