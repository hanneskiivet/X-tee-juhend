---
title: X-tee liikme alamsüsteemi registreerimine (X-teega liidestumine)
---

X-tee versioonis 6 toimub andmeteenuste osutamine ja kasutamine läbi X-teega liitunud asutuse infosüsteemi alamosa - X-tee alamsüsteemi (turvaserveris objekt SUBSYSTEM). 

Erinevalt X-tee versioonist 5 antakse pääsuõigusi vaid X-tee liikmete alamsüsteemidele, mitte X-tee liikmele kui asutusele.

X-tee alamsüsteemidena registreeritakse X-tee liikme infosüsteemi ja turvaserveri liidestuskohad, mida on võimalik andmeteenuse osutaja või kasutajana kindlaks määrata. 

X-tee alamsüsteemi(d) defineerib iga asutus ise, arvestades asutuse tervikinfosüsteemi. X-tee alamsüsteemi(de) defineerimisel tuleb eelkõige mõelda sellele, kuidas saaks asutus oma (teenuseid osutavaid või kasutavaid) infosüsteeme käitlemise mõttes kõige paremini dekomponeerida ja jagada, võttes näiteks arvesse järgmisi aspekte:

* süsteemid, mis toimivaid samadel õiguslikel alustel
* süsteemid, millele juurdepääs on samal turvatasemel
* süsteemid, mis toimivad tehniliselt samal põhimõttel (nt on välises majutatuses). 

Soovitame seda kasutada üksnes juhul, kui teie asutuse infosüsteem on väike ning objektiivseid aluseid asutuse infosüsteemis tükeldamiseks pole. Muudel juhtudel soovitame dekomponeerida oma infosüsteem X-teel paremini adresseeritavateks osadeks.

Näiteks: RIA riigiportaali www.eesti.ee tarbitavad teenused on käsitletavad eraldi X-tee alamsüsteemide poolt:

* Turvserveris 'EE / GOV / 70006317 / riigiportaal-citizen' – kodanikele avatud teenused.
RIHAs registreeritud alamsüsteemina: [70006317-riigiportaal-citizen](https://www.riha.ee/Infos%C3%BCsteemid/Vaata/70006317-riigiportaal-citizen)
* Turvserveris 'EE / GOV / 70006317 / riigiportaal-official' – ametnikele avatud teenused.
RIHAs registreeritud alamsüsteemina: [70006317-riigiportaal-official](https://www.riha.ee/Infos%C3%BCsteemid/Vaata/70006317-riigiportaal-official)
* Turvserveris 'EE / GOV / 70006317 / riigiportaal-system' – riigiportaali toimimiseks tarvilikud teenused (teavituskalender, ametlik e-post jmt).
RIHAs registreeritud alamsüsteemina: [70006317-riigiportaal-system](https://www.riha.ee/Infos%C3%BCsteemid/Vaata/70006317-riigiportaal-system)


## 4.1. X-tee toodangkeskkonna alamsüsteemi kirjeldamine ja registreerimine RIHAs

**X-tee v5 ajal registreeritud andmekogud/infosüstemid, millele väljastati X-tee v5 andmekogu sertifikaati ei ole X-tee v6 alamsüsteemid. 

X-tee toodangkeskkonna X-tee keskuses on võimalik registreerida ainult sellist X-tee alamsüsteemi:** 

* mis on kirjeldatud RIHAsse vt p 4.1.1
* millele on määratud X-tee alamsüsteemi toimimise eest vastutaja kontaktisik, alamsüsteemi teenindava turvaserveri administraatori andmed ja X-tee alamsüsteemi turvameetmete süsteem. Riigi- ja kohaliku omavalitsuse asutustel on kohustus määrata turvaklass vastavalt avaliku teabe seaduse § 439 lõike 1 punkti 4 alusel kehtestatud määrusele.
Selle info [RIHAs](https://www.riha.ee/Infos%C3%BCsteemid) ajakohasena hoidmine on hädavajalik, et andmeteenuse osutajatel oleks kanal, mille kaudu tuvastada andmeteenuse kasutajate turvameetmesüsteem ja turvaklass.

**Erisused arendus- ja testkeskkonnas:**

* turvaserveris registreeritud X-tee alamsüsteemidele kontrolle ei rakendata.
* alamsüsteeme RIHAs ei registreerita

### 4.1.1. X-tee toodangkeskkonna (EE) alamsüsteemi registreerimine RIHAs

**Alusta RIHAs X-tee alamsüsteemi kirjeldamist [siit](https://abi.riha.ee/X-tee-alamsysteem)**

**NB!** Infosüsteemi märksõnade lahtrisse kirjuta: **X-tee alamsüsteem**

Alamsüsteem on registreeritud RIHAs kui sellel on märge **"Süsteem on kasutusel"** ja infosüsteemi valdkond **"X-tee alamsüsteem"**. Eraõigusliku asutuse alamsüsteemi puhul peab olema üles laetud digiallkirjastatud "[Nõuetele vastavus kinnitus](https://www.ria.ee/public/x_tee/xtee_nouetele_vastavus_kinnitus.pdf)"

X-tee alamsüsteemi andmete RIHAs kirjeldatust kontrollib X-tee keskus turvaserveri liidese kaudu esitatud alamsüsteemi registreerimise taotluse menetluse käigus. Juhul kui alamsüsteemi ei ole RIHAs või pole selle kohta kirjeldus piisav/täielik, ei registreerita seda X-tee keskuse poolt. 
Seetõttu on oluline toodangu keskkonna alamsüsteemi registreerimine [RIHAs](https://abi.riha.ee/X-tee-alamsysteem) enne turvaserveris registreerimistaotluse esitamist.

Välismaisete organisatsioonide puhul (X-tee Member Class on NEE) tuleb RIHAs "Lühinimi" kasutada

X-tee Member Code, selle koodi moodustamist vt ptk **3.2.**

Näide: 

Malta ettevõtte X-tee Member Code on NTRMT-C56249,  alamsüsteemi nimi "ehma". RIHAs  alamsüsteemi **Lühinimi** on **NTRMT-C56249-ehma**

X-tee toodangkeskkonna alamsüsteemide loend on leitav [siit](https://www.riha.ee/Infos%C3%BCsteemid?topic=x-tee%20alams%C3%BCsteem)

## 4.2.	X-tee alamsüsteemi registreerimine X-teel (turvaserveris ja X-tee keskuses)

**NB! Toodangu keskkonna alamsüsteemi puhul peab olema teostatud p 4.1.1.**

X-tee andmeteenuste osutamine ja kasutamiseks, peab X-tee alamsüsteemi registreerima X-tee keskuses. 
Selleks peab asutus lisama X-tee alamsüsteemi turvaserverisse ja esitama taotluse registreerimiseks X-tee keskusele.
Kui X-tee liige kasutab turvaserveri [majutusteenust](https://moodle.ria.ee/mod/page/view.php?id=381), registreerib X-tee alamsüsteemi turvaserveri omanik.

Turvaserverisse sisestatakse alamsüsteemi vastavalt [kasutusjuhendile](http://x-road.eu/docs/x-road_v6_security_server_user_guide.pdf) (Security Server Clients):

1. **Member Class** - liikme klass.
GOV– Eesti asutused
COM– Eesti äriühingud
NGO– Eesti sihtasutused ja mittetulundusühingud
NEE– teiste riikide asutused/ettevõtted 
1. **Member Code – alamsüsteemi omaniku** asutuse registrikood

**NB!** kui alamsüsteemi omanik on välismaine ettevõtte (NEE), Member Code moodustamist vaata. pt **3.2.** 
1. **Subsystem Code** – X-tee alamsüsteemi nimi (väikesed tähemärgid). 

RIHAs kirjeldatud  toodangu alamsüsteemi (Lühinimi: registrikood-alamsüsteemi nimetus) **sisestatakse turvaserveris ilma registrikoodita**. 
*Näide: alamsüsteemi nimi RIHAs „[70006317-riha](https://www.riha.ee/Infos%C3%BCsteemid/Vaata/70006317-riha)“ ja turvaserveris  SUBSYSTEM CODE „riha“.*
**DHX X-tee alamsüsteemide** nimetamise reeglit vaata **[Reserveeritud nimi DHX](https://e-gov.github.io/DHX/)** 
1. Esita X-tee alamsüsteemi registreerimis taotlus X-tee keskusele vastavalt [kasutusjuhendile](http://x-road.eu/docs/x-road_v6_security_server_user_guide.pdf)  (Registering a Security Server Client in the X-Road Governing Authority)

**Erisused arendus- ja testkeskkonnas:** registreeritavaid X-tee alamsüsteeme ei ole vajalik RIHAs kirjeldada.
