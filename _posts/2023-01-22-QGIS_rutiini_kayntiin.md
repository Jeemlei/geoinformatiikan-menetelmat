---
title: "1.1 QGIS rutiini käyntiin"
date: 2023-01-22
layout: post
---

Ensimmäinen työpaja antoi hyvän lähtölaukauksen kurssille.
QGIS oli minulle jo hieman entuudestaan tuttu Johdatus geinformatiikkaan -kurssilta, jonka kävin lukuvuoden ensimmäisessä periodissa. Varsinaista käyttörutiinia ei kuitenkaan tuona aikana ehtinyt syntyä, joten pieni kertaus perusteista oli paikallaan.
<!--excerpt_end-->

### Itämeren typpipäästöt

Ensimmäinen tehtävä palautti hyvin mieleen, mistä valikoista QGIS:n perus työkalut löytyvät. Kartta syntyi helposti ja suurimpana opetuksena olikin järkevän visualisoinnin pohtiminen teknisen toteutuksen sijaan.
Koska työpaja eteni aikalailla esimerkkiä seuraten, jäi muutama asia karttatulosteessa epähuomiossa viimeistelemättä. Päädyinkin samaan kuin mm. T. Sahlberg ja P. Matero, jotka tekivät tulosteen uudestaan kotona.
Tässä tehtävässä päädyin kirjoittamaan karttaselitteet englanniksi, sillä aineistokin oli englanniksi ja kartan aihe oli kansainvälinen.

<img src="{{ site.base_url }}{% link /assets/imgs/GIS1/N_osuus.png %}" width="100%">

> Kuva 1: Itämeren typpipäästöjen osuus valtioittain

### Opiskelijat väistötiloissa

Toisessa tehtävässä oli tarjolla kaksi vaikeustasoa: valmiin aineiston ja vektorikartan käyttäminen tai omavalintaisen aineiston etsiminen ja yhdistäminen rajapinnan kautta haettuun vektorikarttapohjaan.

Aloin ensin toteuttamaan karttaa valmiilla aineistolla, mutta totesin nopeasti toistavani vain ensimmäistä tehtävää uudella aineistolla. Tein kuitenkin kartan nopeasti loppuun vahvistaakseni rutiinia ja siirryin sen jälkeen tarkastelemaan vaikeampaa vaihtoehtoa.

<img src="{{ site.base_url }}{% link /assets/imgs/GIS1/Tyoikaiset_kunnissa.png %}" width="50%">

> Kuva 2: Valmiista aineistosta toteutettu karttatuloste

Kurssimateriaalissa oli annettu valmiiksi avoimen rajapinnan osoite, josta kartan kuntapohjan pystyi lataamaan suoraan QGISiin.
Etsiessäni tietoa miten rajapintayhteys QGISiin asetetaan, harhauduin melkein heti tutkimaan mitä muita rajapintoja pystyn löytämään ja mitä kryptiset kirjainyhdistelmät rajapintojen yhteydessä tarkoittivat. Paljon Suomeen liittyvää dataa ja rajapintoja löysinkin [avoindata.fi](https://www.avoindata.fi)-palvelusta ja kirjainyhdistelmiä selvensi paikkatietoikkunan dokumentti "[Mitä ovat WMS, WFS, WCS – ja mihin niitä tarvitaan?](https://www.paikkatietoikkuna.fi/c/document_library/get_file?uuid=2dbacd1a-d2d1-448b-bfb2-0d9ef1fb56aa&groupId=10128)".

Aineistoksi päätin valita Ylen julkaiseman "Väistötiloissa opiskelevat peruskoululaiset syksy 2018", jonka sain ladattua csv-tiedostona.

Harjoitus lisäsi erityisesti ymmärrystäni WFS-rajapintojen toiminnasta, csv-tiedostojen tuomisesta QGIS-projektiin ja uuden datan liittämisestä olemassa oleviin geometrioihin.

<img src="{{ site.base_url }}{% link /assets/imgs/GIS1/Opiskelijat_vaistotiloissa.png %}" width="75%">

> Kuva 3: Opiskelijat väistötiloissa vuonna 2018

---

**Lähteet:**
- Sahlberg, T. 2023. Geoinformatiikan menetelmät- kurssi alkaa. Kirjoitus TUOMAS SAHLBERG – KURSSIBLOGEJA -blogissa 17.1.2023. Viitattu 22.1.2023. [https://blogs.helsinki.fi/tsahlber/2023/01/17/geoinformatiikan-kurssi-alkaa/](https://blogs.helsinki.fi/tsahlber/2023/01/17/geoinformatiikan-kurssi-alkaa/).
- Matero, P. 2023. Ensimmäinen postaus. Kirjoitus GEOINFORMATIIKAN MENETELMIÄ HARJOITTELEMASSA -blogissa 20.1.2023. Viitattu 22.1.2023. [https://blogs.helsinki.fi/matero/2023/01/20/kurssin-ensimmainen-viikko/](https://blogs.helsinki.fi/matero/2023/01/20/kurssin-ensimmainen-viikko/).
- Kuntapohjaiset tilastointialueet - Ladattu 19.1.2023. [https://www.avoindata.fi/data/fi/dataset/kuntapohjaiset-tilastointialueet1](https://www.avoindata.fi/data/fi/dataset/kuntapohjaiset-tilastointialueet1)
- Mitä ovat WMS, WFS, WCS – ja mihin niitä tarvitaan? (PDF) - Ladattu 19.1.2023. [https://www.paikkatietoikkuna.fi/c/document_library/get_file?uuid=2dbacd1a-d2d1-448b-bfb2-0d9ef1fb56aa&groupId=10128](https://www.paikkatietoikkuna.fi/c/document_library/get_file?uuid=2dbacd1a-d2d1-448b-bfb2-0d9ef1fb56aa&groupId=10128)
- Väistötiloissa opiskelevat peruskoululaiset syksy 2018 - Ladattu 19.1.2023. [https://www.avoindata.fi/data/fi/dataset/vaistotiloissa-opiskelevat-peruskoululaiset-syksy-2018](https://www.avoindata.fi/data/fi/dataset/vaistotiloissa-opiskelevat-peruskoululaiset-syksy-2018)
- How to Specify Data Types of CSV Columns for Use in QGIS - Vierailtu 19.1.2023. [https://anitagraser.com/2011/03/07/how-to-specify-data-types-of-csv-columns-for-use-in-qgis/](https://anitagraser.com/2011/03/07/how-to-specify-data-types-of-csv-columns-for-use-in-qgis/)
- Performing Table Joins - Vierailtu 19.1.2023. [https://www.qgistutorials.com/en/docs/performing_table_joins.html](https://www.qgistutorials.com/en/docs/performing_table_joins.html)
