---
name: oppimispeli
description: Rakenna lukiolaiselle yhden tiedoston harjoituspeli oppikirjan sivusta, kokeen kartasta tai muusta kuvatusta materiaalista. Käytä aina, kun käyttäjä pyytää harjoituspeliä, interaktiivista oppimisympäristöä, kertaus- tai koeharjoittelua mihin tahansa lukion aineeseen (maantiede, biologia, historia, kemia, kielet, yhteiskuntaoppi...), tai lähettää kuvan koulumateriaalista ja haluaa siitä jotain, jolla voi harjoitella. Myös silloin, kun pyyntö on "tee tästä peli" tai "miten tätä voisi harjoitella". Erityisesti kun oppijalla on oppimisen, keskittymisen tai hahmottamisen vaikeuksia.
---

# Oppimispeli

Tämä ei ole sääntökirja. Se on kuvaus siitä, mitä yhdessä iltapäivässä opittiin, kun rakennettiin karttapeli lukion maantieteen kokeeseen (merialueet ja merivirrat). Valmis peli on tässä repossa: `merivirrat/index.html`, julkaistuna osoitteessa https://juhanajuhana.github.io/oppimispelit/merivirrat/. Lue se, kun haluat nähdä, miltä nämä ajatukset näyttävät koodina. Älä kopioi sitä sellaisenaan – uuden aineen peli on oma pelinsä. Kopioi ajattelu.

## Mitä yritetään saada aikaan

Lukiolainen, joka istuu kokeen edellä kartan, kaavan tai luettelon kanssa ja jolle irralliset faktat eivät tartu. Peli onnistuu, jos hän tekee 10 minuutin session vapaaehtoisesti toisenkin kerran ja kokeessa tunnistaa asiat, ei vain muistele nimiä.

Pelin arvo ei ole kysymysten määrässä vaan siinä, että jokainen kohde on kytketty johonkin: paikkaan, naapuriin, ryhmään, syyhyn. Merivirtapelissä Golfvirta ei ollut nuoli kartalla vaan "se, jonka takia Suomessa on leudompaa kuin Grönlannissa samalla leveysasteella" ja "Pohjois-Atlantin kehän lämmin haara, joka kiertää myötäpäivään". Jälkimmäinen kytkös teki kolmestatoista nuolesta viisi kehää.

## Miten tänään edettiin, ja mitä siitä kannattaa toistaa

**Ensin kartta, sitten kysymykset.** Ensimmäinen versio oli pelkkä klikattava kartta, jossa jokaisella kohteella oli nimi ja lyhyt "miksi tällä on väliä". Vasta kun se toimi, tuli testi. Tämä järjestys on oikea myös siksi, että Tutki-tilassa sisällön virheet näkyvät heti – ja niitä tuli.

**Sisältö tarkistetaan materiaalia vasten, ei muistista.** Ensimmäinen lista merialueista tuli oppilaan käsin täyttämästä vastauspaperista. Se osoittautui osittain vääräksi: numerot ja nimet olivat ristissä, ja kartta oli kuvattu kyljellään. Vasta suora kuva opettajan numeroimasta pohjakartasta antoi totuuden, ja silloin pallojen paikat ratkaisivat, eivät kirjoitetut nimet. Kysy siis aina, mikä osa materiaalista on opettajalta ja mikä oppilaalta, ja pyydä suora kuva, jos ensimmäinen on vino tai rypyssä. Sano ääneen, mitkä kohdat ovat tulkintaa.

**Vaikeus rakennetaan kerroksina, ei säätämällä.** Perustaso kysyy vain paikkoja – ei suuntia, ei ominaisuuksia – ja siinä saa valita, harjoitteleeko merialueita vai virtoja. Keskitasolla tulevat molemmat ja värit näkyvät vihjeenä. Vaikealla kaikki on sekaisin ja vihjeet piilossa. Sama kolmijako toimii missä tahansa aineessa: *missä* ennen *mitä*, *mitä* ennen *miksi*.

**Flow-sessio on se, mikä koukuttaa.** Sekalaiset kysymykset, aikapalkki, putki, kannustavat mutta lyhyet viestit ("Läheltä. Tämä tulee kohta uudestaan."), väärin mennyt palaa 3–5 kysymyksen päästä, ja lopussa yksi onnistuminen ja muutama kertauskohde – ei lista kaikista virheistä. Oikean vastauksen jälkeen siirrytään sekunnissa eteenpäin, virheen jälkeen kartta näyttää oikean kohdan hetken.

**Tuki on valinnaista ja piilossa, mutta se on ajateltu valmiiksi.** Rauhallinen tila (ei automaattista siirtymää, virhe heti uudestaan, luvut vasta lopussa, animaatio vain korostetussa kohteessa), lähennys kysytyn kohteen seutuun, eteneminen naapuri kerrallaan tutusta kohteesta alkaen (Itämerestä), lyhyt sijaintivihje jokaiselle kohteelle ("Iso koukku Yhdysvaltain eteläpuolella"), tavutus, nimen ääneen luku, kolmesti oikein osattu kohde värjäytyy vihreäksi, session pituus 3/5/10 min. Kaikki tämä on "Tuki ja asetukset" -otsikon takana, koska se, joka ei tarvitse, ei saa nähdä yhtään ylimääräistä valintaa.

**Ensinäkymässä on kaksi nappia.** Tutki karttaa ja Harjoittele. Kerrosvalinnat, selite, yksittäiset harjoitukset ja tuki avautuvat vasta tarvittaessa. Tähän päädyttiin vasta kolmannella kierroksella – tee se heti.

**Yksi HTML-tiedosto, ei riippuvuuksia, ei selaimen tallennusta.** Toimii puhelimessa, jaettavissa linkkinä tai Netlify Dropilla, korjattavissa kuka tahansa. Jokainen uusi tiedostoversio on uusi artefakti omalla julkaisulinkillään – kerro tämä käyttäjälle ennen kuin hän jakaa linkin. Pysyvän linkin saa GitHub Pagesista: pelit ovat repossa `juhanajuhana/oppimispelit` kukin omassa kansiossaan (`merivirrat/index.html`), ja push `main`-haaraan päivittää saman osoitteen parissa minuutissa. Tämä ohje ja pelit ovat samassa repossa, joten uusi peli ja ohjeen päivitys menevät samaan commitiin.

## Sudenkuoppia, joihin astuttiin

- Todellinen rantaviiva-aineisto (Natural Earth 110m, npm-paketti `world-atlas`) oli paljon parempi kuin käsin piirretty, mutta 180. pituuspiirin ylittävät viivat (Siperia–Alaska, Antarktis, Fidži) piirtyivät kartan poikki ja selain täytti puolet merestä maan värillä. Katkaise viivat kartan reunassa ja tarkista lopputulos renderöimällä kuvaksi (resvg) ennen kuin luotat siihen.
- Kartan reunassa halkeava kohde (Beringinmeri) pitää piirtää molempiin reunoihin, muuten lähennys näyttää tyhjää.
- Kaksi eri asiaa samalla tunnisteella (Labradorinvirta ja Labradorinmeri) sekoittivat lisäykset. Tunnisteet erilleen alusta asti.
- Sanan "kuten aiemmin" -päivitykset menivät hukkaan, kun tiedostoa muokattiin muualta samaan aikaan. Tarkista tiedoston sisältö ennen kuin päivität sitä uudestaan.
- Virrat piirretään merialueiden päälle, joten ympyrän keskelle osuva klikkaus meni virralle (Korallimeri, Labradorinmeri, Norjanmeri, Tyynimeri) ja oikea vastaus tulkittiin vääräksi. Kun kysymys koskee merialuetta, virran klikkauskäsittelijä tarkistaa, onko piste jonkin ympyrän sisällä, ja antaa vastauksen sille. Testaa jokaisen kohteen keskipiste selaimessa (`elementFromPoint`) ennen kuin luotat karttaan – koodia lukemalla tätä ei näe.
- Tilaluokat kirjoitettiin `className`-arvoon kokonaisina, jolloin kolmesti osatun kohteen vihreä merkintä pyyhkiytyi heti seuraavassa kysymyksessä eikä koskaan näkynyt. Pysyvä tila liitetään luokkaan joka kerta, kun luokka rakennetaan, ei erillisellä toggle-kutsulla jälkikäteen.
- Viiva harmaannettiin CSS:llä, mutta nuolenkärki (SVG `marker`) piti punaisen tai sinisen värinsä ja paljasti lämpötilan Vaikea-tasolla. Jokaiselle väritilalle oma marker, ja `marker-end` vaihdetaan samoissa CSS-säännöissä kuin viivan väri.
- Oikean vastauksen jälkeinen automaattinen siirtymä oli `setTimeout`, jota tilanvaihto ei perunut: "Tutki karttaa" heti vastauksen jälkeen toi harjoituskysymyksen takaisin paneeliin ja jätti kartan lähennetyksi. Ajastimen tunniste talteen ja peruutus jokaisessa tilanvaihdossa; session lopetus merkitään myös tilaan.
- Puhelimessa (375 px) pienet merialueet olivat 5–9 px halkaisijaltaan, eli niitä ei voinut näpäyttää. Jokaiselle pienelle kohteelle näkymätön suurempi osuma-alue (ei niin suuri, että naapurit menevät päällekkäin), ja kapealla kartalla lähennys kysytyn kohteen alueeseen kaikilla tasoilla, ei vain perustasolla. Mittaa osuma-alueet mobiilinäkymässä, älä arvioi.
- Tyhjän meren tai maan klikkaus ei tehnyt mitään, mikä tuntuu jumilta. Ohiklikkaus antaa lyhyen vihjeen ("Klikkaa ympyrää tai nuolta") ilman virhettä. Valtamerten ympyrät eivät kattaneet koko allasta, joten "Missä on Tyynimeri?" epäonnistui, kun klikkasi Japanin edustaa. Valtamerille näkymättömiä lisäosuma-alueita niin, että koko allas kelpaa.

## Kun aloitat uuden aineen

Katso materiaalia ja kysy itseltäsi, mikä on sen "kartta": biologiassa solukuva tai elimistö, historiassa aikajana, kemiassa jaksollinen järjestelmä tai reaktiokaavio, kielissä sanaston teemakartta. Kohteet sijoitetaan siihen. Sitten sama polku kuin tänään: tutkittava näkymä, kolme kerrosta kontekstia jokaiselle kohteelle (sijainti/vihje, ryhmä, miksi sillä on väliä), kolmen tason harjoittelu, Flow-sessio, tuki piilossa. Näytä käyttäjälle ensin Tutki-tila ja pyydä tarkistamaan sisältö, ennen kuin puhutte harjoittelusta. Valmis peli tallennetaan tähän repoon omaan kansioonsa nimellä `index.html`, ja siihen lisätään linkki etusivulle (`index.html`) ja README:n taulukkoon.

## Toinen peli: ruotsin sanajärjestys (kielioppi ilman karttaa)

Toinen peli tehtiin ruotsin päälauseen sanajärjestyksestä (`sanajarjestys/index.html`). Se osoitti, että sama runko toimii, kun "kartta" ei ole kuva vaan kaavio. Mitä siitä kannattaa ottaa mukaan seuraavaan kielioppipeliin:

**Kaavio on kartta.** Neljä saraketta – Alku | Verbi | Subjekti | Loput – ja rivit ovat saman lauseen eri versiot (suora, ajanmääre alussa, paikanmääre alussa, kysymyssana, kysymys ilman kysymyssanaa). Kun rivit ovat samassa ruudukossa, verbisarake pysyy paikallaan ja subjekti näkyy siirtyvän. Se on koko sääntö yhdellä silmäyksellä, eikä sitä tarvitse selittää.

**Yksi peruslause, monta muunnosta.** Lauseet tallennettiin lohkoina rooleineen (subjekti, verbi, toinen verbi, inte, objekti, paikka, aika, kysymyssana), ja kaikki versiot sekä väärät vaihtoehdot generoidaan koodilla. 18 lauseesta tuli 91 muunnosta, ja jokainen väärä vaihtoehto on juuri se suomalaisen tyypillinen virhe (subjekti ennen verbiä alun jälkeen). Kysymyksissä "jag" vaihtuu "du":ksi, muuten kysymys kuulostaa oudolta. Aja generaattori Nodella ja lue kaikki lauseet läpi ennen selainta – siinä näkyy heti, jos lopun järjestys (inte → toinen verbi → objekti → paikka → aika) tuottaa jotain, mitä kukaan ei sanoisi.

**Järjestäminen napauttamalla, ei raahaamalla.** Lohkot ovat sanaryhmiä ("till Stockholm", "i morgon"), eivät yksittäisiä sanoja, jotta harjoitus koskee järjestystä eikä sanastoa. Alku on annettu valmiiksi (kysymyksessä ilman kysymyssanaa se on tyhjä viiva), ja viimeinen lohko asettuu itsestään, koska sille ei ole vaihtoehtoa. Väärän vastauksen palaute kertoo, mikä kerros petti: verbi ei ollut toisena, subjekti ei ollut verbin jälkeen, tai vain loppuosan järjestys. Oma järjestys ja oikea näytetään rinnakkain.

**Kerrokset kieliopissa.** Perus tunnistaa (suora vai käänteinen, kumpi lause on oikein), Keski järjestää kaavioon otsikoiden ja värien avulla, Vaikea järjestää ilman kaaviota ja lisää inte-lauseet ja kaksi verbiä. "Miksi"-kysymys on tässä "mikä on alussa", ja se kuuluu Keski- ja Vaikea-tasoille.

**Yhden asian harjoitukset kannattaa tehdä samalla koneistolla.** Sen sijaan, että jokaiselle harjoitustyypille tehtäisiin oma tila, Flow-sessio saa parametrin: kysymystyypit ja kysymysmäärä (12 kysymystä, ei ajastinta). Sama palaute, sama kertaus ja sama loppuyhteenveto ilman kopiokoodia.

**Ääneen luku on ruotsiksi.** `SpeechSynthesis` kielellä `sv-SE`, oikean lauseen kuuntelu on nappina jokaisessa palautteessa ja Tutki-tilassa, ja tukiasetuksena se luetaan automaattisesti.
