---
title: Turvaserveri paigaldamine
---

* Turvaserveri tarkvara paigaldatakse vastavalt [paigaldusjuhisele](http://x-road.eu/docs/x-road_v6_security_server_installation_guide.pdf).
* Tuleb laadida vastava keskkonna konfiguratsiooniankur, mis on kättesaadav [siin](https://www.ria.ee/ee/x-tee-keskkonnad.html). 
* Tuleb paigaldada riistvaraline allkirjastamisseade turvaserverile (*arendus- ja testkeskkonnas ei ole kohustus kasutada riistvaralist allkirjastamise seadet*). 
* Turvaserveri seadistamisel tuleb arvestada Eesti X-tee keskkonna nõudeid, mis on kirjeldatud [siin](https://www.ria.ee/public/x_tee/Eesti_keskkonna_tehnilised_tingimused.pdf).  

**NB!** Kui turvaserveri omanik või majutatav klient on välismaine organisatsioon, tuleb turvaserveris valida Member Class "NEE" ning Member Code moodustada järgmiselt: 
"**NTRRIIGIKOOD-REGISTRIKOOD**" - (tühikud peab eemaldama).
Kus 
1) NTR - Juriidilise isiku identifikaatori prefiks ETSI EN 319 412-1 klausli 5.1.4 järgi 
2) RIIGIKOOD - Riigikood ISO 3166 (Alpha 2) järgi
3) \- sidekriips
4) REGISTRIKOOD - Organisatsiooni registrikood asukohariigis 

Näide: Maltas registreeritud organisatsioon Lexbyte Digital Limited 
Member Name: "Lexbyte Digital Limited"
Member Class: "NEE"
Member Code: "NTRMT-C56249" (tühikud peab eemaldama)

Sellised nõuded Member Code'ile tulenevad vajalikkusest tagada X-teel välismaiste organisatsioonide Member Code'ide unikaalsus. Lisaks peab X-tee liikme Member Code vastama SK ID Solutions AS e-Templi sertifikaadi profiili Organisation Identifier (2.5.4.97) väljale. 

Viited: 
* SK ID Solutions AS sertifikaadi profiil: https://sk.ee/upload/files/SK-CPR-KLASS3-EN-v8_0-20171130.pdf
* ETSI EN 319 412-1: http://www.etsi.org/deliver/etsi_en/319400_319499/31941201/01.01.00_30/en_31941201v010100v.pdf 
* Alpha 2 riigikoodid: https://www.iso.org/obp/ui/#search 
* Malta ettevõtete register http://rocsupport.mfsa.com.mt/pages/SearchCompanyInformation.aspx

### 3.2.1. Turvaserveri IP muutmine

Juhul kui X-tee liikmel tekib vajadus **toodangukeskkonna** turvaserveri IP-aadressi muutmiseks, tuleb toimida järgmiselt.

1. Liige esitab X-tee keskusele (RIHAs märgitud X-tee alamsüsteemi kontaktisiku või asutuse esindusõigust omava isiku poolt) allkirjastatud taotluse IP-aadressi muutmiseks keskserveris. Taotluse vormi saab [siit](https://www.ria.ee/public/x_tee/Turvaserveri_IP_muutmise_taotlus.pdf).
Taotlus tuleb saata aadressile help@ria.ee. Taotluse menetlemise käigus lepitakse liikmega täpsemalt kokku vajalikud tegevused ja aeg IP-aadressi muutmiseks.
1. iige teavitab usaldusteenuse osutajat IP muutmise kohta (tagamaks OSCP ja ajatempliteenuse toimimine). 
X-tee keskus teavitab liiget taotluse otsusest.

Erisused arendus- ja testkeskkonnas

* Arendus- või testkeskkonna IP-aadressi muutmiseks saadetakse X-tee keskusele sooviavaldus e-posti aadressile help@ria.ee, lisades järgmise info: asutuse nimi ja registrikood, turvaserveri nimi (server code), keskkond, mille IP-aadressi muudetakse, turvaserveri vana ja uus IP, kontaktisiku andmed (nimi, e-post, telefon).
* Testkeskkonnas turvaserveri IP muutmise vajadusest teavitatakse ka usaldusteenuse osutajat.
