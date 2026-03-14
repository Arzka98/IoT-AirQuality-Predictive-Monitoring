# Älykäs IoT-ilmanlaatuvalvomo ennustavalla analytiikalla

Tämä projekti on toteutettu osana Data ja Koneoppiminen kurrsia. Järjestelmä on pilvipohjainen valvomo, joka seuraa ilmanlaatua (CO2, lämpötila, kosteus) ja ennustaa tulevaa kehitystä koneoppimisen menetelmillä.

## Arkkitehtuuri
Järjestelmä hyödyntää seuraavia teknologioita:
* **Simulaattori:** MQTT-pohjainen data-lähde.
* **Väliohjelmisto:** Node-RED (FlowFuse Cloud).
* **Tietokanta:** MongoDB Atlas (NoSQL Cloud Database).
* **Visualisointi:** Node-RED Dashboard ja MongoDB Atlas Charts.

## Keskeiset ominaisuudet
1. **Reaaliaikainen seuranta:** Live-näkymä ilmanlaadun nykytilasta.
2. **Historiadata:** Järjestelmä tallentaa datan pilvitietokantaan ja mahdollistaa historiatietojen haun Dashboardille.
3. **Datan puhdistus:** Node-REDissä on toteutettu logiikka, joka suodattaa vialliset viestit ja haamuviestit pois ennen tallennusta.
4. **Ennustava analytiikka:** Järjestelmä laskee reaaliaikaisesti **lineaarisen regression** avulla CO2-pitoisuuden ennusteen 30 minuutin päähän.

## Käyttöönotto
1. Tuo repositoriosta löytyvä `.json` tiedosto Node-REDiin (Import).
2. Varmista, että tarvittavat solmut (Dashboard, MongoDB) on asennettu Palette Managerista.
3. Konfiguroi MongoDB-yhteys merkkijonollasi.

## Tekijä
Arno Linnakoski
