---
title: X-tee alamsüsteemi registreerimine X-teel (turvaserveris ja X-tee keskuses)
---	

**NB! Toodangukeskkonna alamsüsteemi puhul peab olema teostatud sammud, mis on kirjeldatud juhendis: _alamsysteemi-registreerimine-RIHAs_ [pt 4.1.1.](/docs/alamsysteemi-registreerimine-RIHAs.md)**

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

**NB!** Kui alamsüsteemi omanik on välismaine ettevõtte (NEE), siis Member Code moodustamist vaata **[X-tee kasutamise juhendist](https://moodle.ria.ee/mod/page/view.php?id=288) pt 3.2.**
1. **Subsystem Code** – X-tee alamsüsteemi nimi (väikesed tähemärgid). 

RIHAs kirjeldatud  toodangu alamsüsteemi (Lühinimi: registrikood-alamsüsteemi nimetus) **sisestatakse turvaserveris ilma registrikoodita**. 
*Näide: alamsüsteemi nimi RIHAs „[70006317-riha](https://www.riha.ee/Infos%C3%BCsteemid/Vaata/70006317-riha)“ ja turvaserveris  SUBSYSTEM CODE „riha“.*
**DHX X-tee alamsüsteemide** nimetamise reeglit vaata **[Reserveeritud nimi DHX](https://e-gov.github.io/DHX/)** 
1. Esita X-tee alamsüsteemi registreerimis taotlus RIA'le vastavalt [kasutusjuhendile](http://x-road.eu/docs/x-road_v6_security_server_user_guide.pdf)  (Registering a Security Server Client in the X-Road Governing Authority)

**Erisused arendus- ja testkeskkonnas:** registreeritavaid X-tee alamsüsteeme ei ole vajalik RIHAs kirjeldada.
