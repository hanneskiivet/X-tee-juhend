---
title: Turvaserveri registreerimine X-tee keskuses
---

1. Taotle turvaserveri registreerimist turvaserveri liidese kaudu vastavalt turvaserveri [kasutusjuhendile](http://x-road.eu/docs/x-road_v6_security_server_user_guide.pdf). (Registering the security server in the X-road Governing Authority).
  * **NB!** Turvaserveri registreerimise taotluse esitamiseks (AUTH sertifikaadi registreerimiseks) peab turvaserveris SIGN sertifikaadi OCSP response olema "good" ja status "registered". Turvaserveri registreerimis taotlus e-Tembeldatakse.
1. X-tee keskus registreerib turvaserverit. Registreerimise oleku info on nähtav turvaserverist (Security Server Clients, vt Name ringi värvust) .

**Erisused testkeskonnas**

**Testkeskkonna** AUTH-sertifikaat tuleb manusena edastada RIA'le aadressil help@ria.ee. 
Taotlus pealkirjaga „Testkeskkonna turvaserveri  AUTH-sertifikaat “ järgmise infoga: asutuse nimi, registrikood, turvaserveri nimi (server code), manustada AUTH-sertifikaat.
