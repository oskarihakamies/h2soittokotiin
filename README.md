# h2soittokotiin


## Karvinen 2014: Hello Salt Infra-as-Code

- Artikkelissa kerrotaan, miten luodaan Saltin "Hello world" eli toisin sanoen yksinkertainen esimerkki Saltin konfiguraatiohallintajärjestelmästä
- "Hello world" - esimerkki kirjoitetaan init.sls tiedostoon.
- Lopussa selitys, miten idempotenssi toimii ajamalla komentoja uudestaan terminaalissa. 


## Salt Contributors: Salt overview – Rules of YAML, YAML simple structure, Lists and dictionaries - YAML block structures.

- Simppeli ohjerakenne YAML:in pelisäännöistä esimerkiksi data on muotoiltu key: value pareihin YAML:issa 
- YAML koostuu kolmesta perus elementistä. Scalars eli avain-arvo-pareista, joissa arvo on numero, merkkijono tai boolearinen arvo. Lists, eli avain (key:) seurattuna arvojen listalla jokainen arvo omalla rivillään, edeltää kaksi välilyöntiä ja viivan. Ja viimeisenä sanakirjat eli vain-arvo-parien ja listojen kokoelma.
- YAML on myös järjestetty lohkorakenteisiin




## Salt contributors: The top file - Introduction and A Basic example

- Johdannossa lyhyt tiivisitelmä siitä, miten useimmat infrastruktuurit toimivat.
- Tehokkaaseen hallintaan tarvitaan ryhmien roolien määrittelyä, kuten Apache-palvelimen asennus ja käynnistys front-end-koneille
- Saltin top.sls-tiedosto yhdistää koneiden ryhmät konfiguraatio rooleihin ja on state tree-hierarkian huipulla.
- Top tiedoistoissa on kolme eri komponenttia. Ympäristö, kohde ja tilatiedostot. 




a)

Aloitin tehtävän tarkastamalla oliko minulla salt-minion ladattuna. 

<img width="355" height="89" alt="image" src="https://github.com/user-attachments/assets/bad87590-f1be-4d41-b233-3940fb2a374f" />

Tämän jälkeen latasin micro editorin. 

<img width="304" height="79" alt="image" src="https://github.com/user-attachments/assets/3e359bfa-654c-48ff-ac2e-8034932055f7" />

Tehtävän tarkoituksena oli paikallisesti kokeilla infraa koodina. Loin siis alkuun kansion "Hello" moduuliin 

<img width="253" height="56" alt="image" src="https://github.com/user-attachments/assets/85957c2b-1441-4a23-bcc4-9f1d12c8180f" />

Olin tällä hetkellä oikeassa kansiossa myös ja avasin sitten microeditorin. Microeditoriin ajoin idempotentin koodin saltin omalla kielellä. Tämän jälkeen ajoin koodin salt-call --localilla ja varmistin, että se oli onnistunut. 


<img width="362" height="212" alt="image" src="https://github.com/user-attachments/assets/dbc4d804-a8b6-4fc7-9030-60f3addb48fb" />


Kuten huomaamme, niin esimerkkitiedoston luominen onnistui. Varmistetaan vielä, että Salt teki mitä se sanoi tekevänsä. 

<img width="259" height="31" alt="image" src="https://github.com/user-attachments/assets/63c5ec5b-fd94-4144-ada7-8d2320ddcaeb" />

Tehtävä siis onnistui. 








b)


Tehtävä topping. Aloitin tehtävän siirtymällä salttiin ja varmistin myös aluksi, että hakemisto oli olemassa. 

<img width="163" height="20" alt="image" src="https://github.com/user-attachments/assets/3e42cd9d-1e23-47e7-9ecb-b7e6f2010a3d" />


Loin tämän jälkeen tiedoston nanolla ja lisäsin Top files sivulla annetun koodin. tiedoston sisälle. 


<img width="271" height="62" alt="image" src="https://github.com/user-attachments/assets/0f3f515f-dc9c-46a3-8a61-939a97a106ca" />

Seuraavaksi lähdin luomaan tiedostoja core.sls ja edit.sls, jotta jokainen tila päästäisiin ajamaan kerralla läpi. * merkki alkuperäisessä top- tiedostossa ajaa kaikki tiedostot hakemistosta /srv/salt/



<img width="275" height="71" alt="image" src="https://github.com/user-attachments/assets/7ae65b0d-5831-4b83-ba16-b72763d04c9c" />


Käytin edit.sls kohdalla pkg.installed nanoa, mutta sillä ei ollut tehtävänannon kannalta väliä, mitä editoria käytin vaan se, että top filen ajaminen toimii. 



Seuraavaksi kokeilin, että toimiiko se peruskomennolla salt-call --localilla ja vastaukseksi sain: 



<img width="500" height="322" alt="image" src="https://github.com/user-attachments/assets/f2fffafd-dff9-497d-b37e-3b8c269aaf4c" />



<img width="452" height="155" alt="image" src="https://github.com/user-attachments/assets/e82c01e4-7835-428a-b5fe-2d0affe8c5ae" />


Eli sain ajettua molemmat samalla kertaa. Siinä kesti vain hieman päälle 9s, mutta tehtävä onnistui.






c)

Seuraavaksi viisikko tiedostossa tehtävä edessä. Eli tässä teen erilliset esimerkit jokaisesta tilafunktiosta. 












d)





## Lähteet

Karvinen 2014: Hello Salt Infra-as-Code. https://terokarvinen.com/2024/hello-salt-infra-as-code/

Salt Contributors: Salt overview – Rules of YAML, YAML simple structure, Lists and dictionaries - YAML block structures. https://docs.saltproject.io/salt/user-guide/en/latest/topics/overview.html#rules-of-yaml



