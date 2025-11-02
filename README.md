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



c)


d)





## Lähteet

Karvinen 2014: Hello Salt Infra-as-Code. https://terokarvinen.com/2024/hello-salt-infra-as-code/

Salt Contributors: Salt overview – Rules of YAML, YAML simple structure, Lists and dictionaries - YAML block structures. https://docs.saltproject.io/salt/user-guide/en/latest/topics/overview.html#rules-of-yaml



