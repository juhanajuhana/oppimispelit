# Oppimispelit

Yhden tiedoston harjoituspelejä lukion kokeisiin. Jokainen peli on yksi HTML-tiedosto ilman riippuvuuksia: toimii selaimessa, puhelimessa ja jaettavissa linkkinä.

Pelit ovat julkaistuna GitHub Pagesissa: https://juhanajuhana.github.io/oppimispelit/

## Pelit

| Peli | Aine | Linkki |
| --- | --- | --- |
| Maailman meret: merialueet ja merivirrat | Maantiede | [merivirrat/](https://juhanajuhana.github.io/oppimispelit/merivirrat/) |
| Ruotsin sanajärjestys: suora ja käänteinen | Ruotsi | [sanajarjestys/](https://juhanajuhana.github.io/oppimispelit/sanajarjestys/) |
| Maapallo ja ilmakehä: GE1-kertaus (planetaarisuus, ilmakehä, tuulet, sade, ilmasto, syklonit, ilmastodiagrammi) | Maantiede | [maapallo/](https://juhanajuhana.github.io/oppimispelit/maapallo/) |

## Skilli

Pelien rakentamisohje on skillinä kansiossa `.claude/skills/oppimispeli/`. Claude Code lataa sen automaattisesti, kun työkansio on tämä repo. Ohje viittaa esimerkkinä repon omaan peliin, joten sitä ei tarvitse kopioida erikseen.

Claude-sovellukseen ladattava ohut versio, joka vain ohjaa lukemaan ohjeen täältä, on kansiossa `app-skill/oppimispeli/`. Kun ohje muuttuu, muutos tehdään vain tähän repoon.

## Uuden pelin lisääminen

1. Tee kansio pelin nimellä, esimerkiksi `solu/`, ja tallenna peli sinne nimellä `index.html`.
2. Lisää linkki etusivulle (`index.html`) ja tähän taulukkoon.
3. Committaa ja pushaa `main`-haaraan. GitHub Pages julkaisee muutoksen parissa minuutissa.
