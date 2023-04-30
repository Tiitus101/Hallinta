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

Koitin testata toimiiko ssh uudella portilla.
publick keyn kanssa ongelmia








## b)

Koneet päälle ja masterille ssh yhteys

![image](https://user-images.githubusercontent.com/130304789/234932678-95ced5c6-659e-4882-9f84-3101b40052ce.png)

![image](https://user-images.githubusercontent.com/130304789/234932839-ac0ca1fe-0a47-48f3-a223-f7a89bf02889.png)

