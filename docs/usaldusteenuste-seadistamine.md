---
title: Usaldusteenuste seadistamine
---

Eelnevalt vaata p 3.1.2.

1. Ajatempliteenuse seadistamist vaata turvaserveri [kasutusjuhendis](http://x-road.eu/docs/x-road_v6_security_server_user_guide.pdf) (System Parameters).
1. Turvaserveri autentimissertifikaadi (AUTH) ja e-templi sertifikaadi (SIGN) tellimiseks usaldusteenuse osutajalt on vaja genereerida turvaserveris sertifikaadipäringud vastavalt turvaserveri [kasutusjuhendile](http://x-road.eu/docs/x-road_v6_security_server_user_guide.pdf) (Security Server Registration).
1. Sertifitseerimispäringud (AUTH ja SIGN csr) tuleb salvestada ja edastada usaldusteenuse osutajale.
1. Usaldusteenuse osutaja väljastab sertifikaadi, mis tuleb seadistada turvaserveris

Toodangkeskkonna  SIGN ja AUTH sertifikaatide taotlemise viis sõltub usaldusteenuse pakkujast.
Nt. sertifikaatide taotlemisel SK ID Solutions AS, saab tellimused teha nende e-teeninduskeskkonna www.sk.ee kaudu. 

* [Telli X-tee turvaserveri kliendi sertifikaadid](https://sk.ee/teenused/teenused-x-tee-turvaserveri-omanikule/?service/x_tee_member). Kui te ei ole ise turvaserveri omanik ning ostate turvaserveri majutuse teenust sisse, tellige teenused turvaserveri kliendina.
* [Telli X-tee turvaserveri pidaja sertifikaadid](https://sk.ee/teenused/teenused-x-tee-turvaserveri-omanikule/?service/x_tee_hoster). Kui käitate ise oma X-tee turvaserverit, tellige teenused turvaserveri pidajana. 

Taotluse peab allkirjastama tellimuse vormistaja. 

**Erisused test- ja arenduskeskkonnas**

Testkeskkonna sertifikaatide taotlemine sõltub usaldusteenuse pakkujast.

Nt. testkeskonna sertifikaatide taotlemisel SK ID Solutions AS saab tellimused teha nende e-teeninduskeskkonna www.sk.ee kaudu.

* Test autentimissertifikaadi (AUTH) [tellimiseks](https://sk.ee/teenused/autentsertifikaat/?service/auth_cert) märgi väli "Tellin testsertifikaadi"
* e-Templi test sertifikaadi (SIGN) [tellimiseks](https://sk.ee/teenused/digitempli-teenus/e-tempel/?service/digital_stamps) märgi väli "Tellin testsertifikaadi"

Taotluse peab allkirjastama tellimuse vormistaja.

NB! Teatud usaldusteenuse osutajate testsertifikaatide korral võib olla vajalik testsertifikaadi käsitsi lisamine test-OCSP nimekirja (nt SK ID Solutions AS teenuste korral on seda võimalik teha [siit](https://demo.sk.ee/upload_cert/)). 

**Arenduskeskkonna** sertifikaadi taotlemiseks, edasta taotlus e-postile help@ria.ee

Taotlus pealkirjaga „Turvaserveri sertifikaatide taotlus ja registreerimine arenduskeskkonnas“ järgmise infoga:

asutuse nimi, registrikood, turvaserveri nimi, genereeritud sertifitseerimispäringud (AUTH ja SIGN csr-id) manusena. 
