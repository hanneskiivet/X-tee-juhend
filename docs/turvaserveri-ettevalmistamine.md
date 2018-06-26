---
title: Turvaserveri paigaldamise ettevalmistused
---

Enne turvaserveri ettevalmistamist pead [X-teega liituma](liitumine.md).

### 3.1.1.	Riistvaraline allkirjastamisseade ja selle valik

X-tee andmevahetuse terviklikkuse tagamiseks ning X-teel vahendatud sõnumi ja X-tee liikme seose tuvastamiseks tuleb kasutada kvalifitseeritud e-templi või täiustatud e-templi kvalifitseeritud sertifikaate. Riistvaralise allkirjastamisseadme (HSM - hardware secure module) nõue võib tuleneda usaldusteenuse pakkuja poolt. Kvalifitseeritud e-templi puhul peab see olema väljastatud ainult kvalifitseeritud allkirjastamisseadmele (QSCD). Täiustatud e-templi puhul ei ole allkirjastamiseks vaja QSCD nõuetele vastavat allkirjastamisseadet – sel juhul otsustab usaldusteenuse pakkuja, millised tingimused ta sertifikaadi väljastamiseks kehtestab. 

Nt SK ID Solutions AS [sertifitseerimispoliitika](https://www.sk.ee/upload/files/SK-CP-OS-EN-v6_0-20160701.pdf) nõuab riistvaralise allkirjastamisseadme olemasolu e-templi sertifikaadi väljastamisel. Täpsemalt peab seade olema sertifitseeritud vastavalt FIPS 140-2 Level 2 tasemele või Common Criteria sertifitseering vastavalt Protection Profile'ile EN 419211. Kõige ajakohasema loetelu FIPS 120-2 Level 2 taseleme nõuetele vastavatest seadmetest leiad aadressilt: http://csrc.nist.gov/groups/STM/cmvp/documents/140-1/140val-all.htm

RIA'le teadaolevad seadmete maaletoojad Eestis on:

* Altacom (Utimaco), http://www.altacom.eu/
* Fujitsu Eesti (Gemalto), http://www.fujitsu.com/ee/
* Võrguvara (Gemalto), https://www.vorguvara.ee/
* TopSüstems (Thales), http://www.top-systems.eu/

RIA poolt on nõue, et allkirjastamisseade toetaks PKCS#10 protokolli, sel juhul on see turvaserveriga ühildatav.

Erisused arendus- ja testkeskkonnas: riistvaralist allkirjastamisseadet ei pea kasutama.

### 3.1.2.	Usaldusteenuste valik

Turvaserveri seadistamisel pead märkima kasutatava ajatempliteenuse osutaja. Pärast turvaserveri paigaldamist tuleb taotleda sertifikaat. 

Vajalikud on järgmised usaldusteenused:
1. Turvaserveri **autentimissertifikaat** (turvaserveri omaniku autentimiseks, nn AUTH-sertifikaat) – iga turvaseveri kohta üks. Sertifikaate on võimalik soetada kõigilt [Euroopa usaldusnimekirjas](http://sr.riik.ee/et/tl.html) olevatelt sertifitseerijatelt, kui nende usaldusteenused vastavad [Infosüsteemide andmevahetuskihi usaldusteenuste tingimustele](https://www.ria.ee/public/x_tee/usaldusteenuste_tingimused.pdf). Hetkel on RIA tunnustanud ainult SK ID Solutions AS, kuid oleme valmis lisama ka muid teenusepakkujaid.
1. Asutuse/ettevõtte **e-templi sertifikaat** (sõnumite allkirjastamiseks, nn SIGN-sertifikaat) – iga asutuse/ettevõtte kohta üks. Juhul kui turvaserver on majutuses, siis võib e-templi sertifikaate olla ühes turvaserveris mitu. Sel juhul peab turvaserveris olema turvaserveri omaniku e-templi sertifikaat ja lisaks iga majutatava liikme kohta üks e-templi sertifikaat ühes turvaserveris.
1. **Sertifikaadi kehtivuskinnituse teenus** (OCSP – Online Certificate Status Protocol) . Näiteks SK ID Solutions ASilt OCSP teenust tellides tuleb silmas pidada, et tegemist on suletud teenusega ehk OCSP lepingu sõlmimise käigus tuleb määrata ära IP(d), mille pealt on teenustele ligipääs. Märgitud IPd peavad olema unikaalsed. Juhul kui tasulist OCSP teenust ei tellita SK ID Solutions ASilt, pöördub turvaserver SK ID Solutions ASilt tasuta OCSP responderi poole.
1. **Ajatempiteenus**

**[Turvaserveri kehtivuskinnitus- ja ajatempliteenuse konfiguratsioon](https://www.ria.ee/ee/x-tee-keskkonnad.html)** antakse ette RIA poolt ja see ei ole muudetav turvaserveris.

**Kehtivuskinnitus- ja ajatempliteenuse kasutus maht ühes kuus** sõltub kasutatavate turvaserverite ja sertifikaatide arvust. Näiteks:
* liikmele, kes peab enda jaoks ühte turvaserverit (1 SIGN-sertifikaat, 1 AUTH-sertifikaat), on OCSP teenuse maht ühes kuus 1860 päringut.
* ajatempliteenuse kasutus maht on kuni 930 päringut kuus. Teenuse maht ei sõltu partnerite, teenuste ega sõnumite arvust.

Vt ka [X-teega kaasnevad kulud](https://moodle.ria.ee/mod/page/view.php?id=384)

**Erisused test- ja arenduskeskkonnas:**

* Testkeskkonnas kasuta usaldusteenuse pakkuja testsertifikaati. Sõltuvalt usaldusteenuse pakkujast võib test sertifikaatide tellimine erineda.
* Arenduskeskkonnas kasuta [RIA väljastatud sertifikaatidega](https://www.ria.ee/ee/liitumine-xtee-arendus.html) . 
* Arendus- ja testkeskkonna kehtivuskinnituse ja ajatembeldamise intervallid erinevad toodangukeskkonna omadest, vt täpsemalt [siit](https://www.ria.ee/ee/x-tee-keskkonnad.html). 
* Arendus- ja testkeskkonnas ei ole kohustus kasutada riistvaralist allkirjastamise seadet. Seda asendab turvaserveris olemasolev tarkvaraline allkirjastamise seade (nn soft token).
