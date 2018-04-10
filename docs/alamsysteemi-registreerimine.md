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
