---
title: Turvaserveri paigaldamise ettevalmistused
---

Turvaserveri paigaldamise eeldused:

1. X-tee liikmelisuse olemasolu (ptk 2)
1. Riistvaralise allkirjastamisseadme olemasolu (ptk 3.1.1)
1. X-tee keskuse nõuetele vastavate usaldusteenuste kasutusvõimaluse olemasolu turvaserveris (ptk 3.1.2).

### 3.1.1.	Riistvaraline allkirjastamisseade ja selle valik

Riistvaralise allkirjastamisseadme (HSM - hardware secure module) nõue võib tuleneda usaldusteenuse pakkuja poolt.

Nt SK ID Solutions AS nõuab riistvaralise allkirjastamisseadme olemasolu X-tee v6 toodang keskkonna e-Templi sertifikaadi väljastamisel.

**Allkirjastamise vahendi valiku kriteeriumid on leitavad** [siit](https://moodle.ria.ee/course/view.php?id=13)

X-tee päringute allkirjastamiseks ei ole vaja soetada QSCD nõuetele vastavat allkirjastamisseadet, sest X-tee päringute allkirjad on [eIDAS](http://eur-lex.europa.eu/legal-content/ET/TXT/HTML/?uri=CELEX:32014R0910&from=EN)e mõistes täiustatud e-templid, mis põhinevad kvalifitseeritud sertifikaadil (vt täpsemalt ptk 3.1.2). 

RIA poolt on nõue, et allkirjastamisseade toetaks PKCS#10 protokolli, sel juhul on see turvaserveriga ühildatav.

Erisused arendus- ja testkeskkonnas: liikmel ei ole kohustust kasutada riistvaralist allkirjastamisseadet.

### 3.1.2.	Usaldusteenuste valik

Turvaserveri seadistamise alguses on vajalik märkida kasutatava ajatempliteenuse osutaja. Sertifikaate on võimalik taotleda turvaserveri paigalduse järel. Sertifikaate on võimalik soetada kõigilt [Euroopa usaldusnimekirjas](http://sr.riik.ee/et/tl.html) olevatelt sertifitseerijatelt, kui nende usaldusteenused vastavad [Infosüsteemide andmevahetuskihi usaldusteenuste tingimustele](https://www.ria.ee/public/x_tee/usaldusteenuste_tingimused.pdf)  


Andmevahetuse terviklikkuse tagamiseks ning X-teel vahendatud sõnumi ja X-tee liikme seose tuvastamiseks peab turvaserveris olema seadistatud ja kasutatavad X-tee keskuse nõuetele vastavad kvalifitseeritud usaldusteenuse osutajate kõik järgmised teenused.
1. Liikme **e-templi sertifikaat** (nn SIGN-sertifikaat) – e-templi sertifikaatidest sobivad kasutamiseks kvalifitseeritud e-templi või täiustatud e-templi kvalifitseeritud sertifikaadiga loomiseks mõeldud sertifikaadid. Kvalifitseeritud e-templi puhul tuleneb eIDASest nõue, et vastav kvalifitseeritud sertifikaat tohib olla väljastatud ainult QSCD-le. Täiustatud e-templi puhul ei ole allkirjastamiseks vaja QSCD nõuetele vastavat allkirjastamisseadet – sel juhul otsustab usaldusteenuse pakkuja, millised tingimused ta sertifikaadi väljastamiseks kehtestab. Juhul kui turvaserver on majutuses, siis võib e-templi sertifikaate olla ühes turvaserveris mitu. Sel juhul peab turvaserveris olema turvaserveri omaniku e-templi sertifikaat ja lisaks iga majutatava liikme kohta üks e-templi sertifikaat ühes turvaserveris. E-templi sertifikaatide tellimine võib toimuda eraldi.
1. Turvaserveri **autentimissertifikaat** (turvaserveri omaniku autentimiseks; nn AUTH-sertifikaat) – iga turvaseveri kohta üks.
**Sertifikaadi kehtivuskinnituse** (OCSP – Online Certificate Status Protocol) **teenus**. *Näiteks SK ID Solutions ASilt OCSP teenust tellides tuleb silmas pidada, et tegemist on suletud teenusega ehk OCSP lepingu sõlmimise käigus tuleb määrata ära IP(d), mille pealt on teenustele ligipääs. Märgitud IPd peavad olema unikaalsed.*
1. Juhul kui tasulist OCSP teenust ei tellita SK ID Solutions ASilt, pöördub turvaserver SK ID Solutions ASilt tasuta OCSP responderi poole.
1. **Ajatempiteenus**

*Näiteks SK ID Solutions AS täiustatud e-templi sertifikaatide puhul peab olema täidetud üks järgmistest nõuetest (1. juulist kehtima hakkavad nõuded leiab [siit](https://www.sk.ee/upload/files/SK-CP-OS-EN-v6_0-20160701.pdf)): 

* CC (Common Criteria) sertifitseering vastavalt EN 419 211 standardile või
* FIPS (Federal Information Processing Standards Publication) 140-2 level 2 või parem.*

**Turvaserveri kehtivuskinnitus- ja ajatempliteenuse vaikimisi konfiguratsiooni vaata [siit](https://www.ria.ee/ee/x-tee-keskkonnad.html)**

Konfiguratsioon ei ole muudetav turvaserveris.

**Kehtivuskinnitus- ja ajatempliteenuse kasutus maht ühes kuus** sõltub kasutatavate turvaserverite ja sertifikaatide arvust.

Näiteks liikmele, kes peab enda jaoks ühte turvaserverit (1 SIGN-sertifikaat, 1 AUTH-sertifikaat), on OCSP teenuse maht ühes kuus 1860 päringut.

Ajatempliteenuse kasutus maht on kuni 930 päringut kuus. 

Teenuse maht ei sõltu partnerite, teenuste ega sõnumite arvust. Vt ka ["X-teega kaasnevad kulud"](https://moodle.ria.ee/mod/page/view.php?id=384)

**Erisused arendus- ja testkeskkonnas**

* Testkeskkonnas tuleb kasutada usaldusteenuse pakkuja testsertifikaati. 
* Sõltuvalt usaldusteenuse pakkujast võib test sertifikaatide tellimine erineda.
* Arenduskeskkonnas on testimine võimalik [RIA väljastatud sertifikaatidega](https://www.ria.ee/ee/liitumine-xtee-arendus.html) . 
* Arendus- ja testkeskkonna kehtivuskinnituse ja ajatembeldamise intervallid erinevad toodangukeskkonna omadest, vt täpsemalt [siit](https://www.ria.ee/ee/x-tee-keskkonnad.html). 
* Arendus- ja testkeskkonnas ei ole kohustus kasutada riistvaralist allkirjastamise seadet. Seda asendab turvaserveris olemasolev tarkvaraline allkirjastamise seade (nn soft token).
