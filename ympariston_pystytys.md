## Ympäristön pystyttäminen

### Kuinka päästään alkuun?

Ensin laitetaan kehitysympärisö kuntoon. Tähän tarvitaan:

- [VSCode](https://code.visualstudio.com/)
- [NodeJS](https://nodejs.org/en/)

Luo koneellesi kansio, johon tulet luomaan tulevan projektisi, esim. Frontend.

<img src="./Kuvat/Ymparisto/uusi_kansio.PNG">

Avaa VS Code ja avaa uusi terminaali.

<img src="./Kuvat/Ymparisto/uusi_terminaali.PNG">

Varmista terminaalissa, että olet äsken luomassasi Frontend-kansiossa.

<img src="./Kuvat/Ymparisto/oikea_kansio.PNG">

Tämän jälkeen terminaaliin annetaan komento:

```
npm install –g degit
```

Tämä asentaa (install) tarvittavan degit-paketin globaalisti (-g) koneelle. Npm-komennot eivät toimi ilman nodeJS:n asentamista.

Kun tämä on asennettu, voidaan antaa komento joka luo projektin:

```
degit sveltejs/template ekaprojekti
```

Nyt projekti on luotu! Näet sen vasemmalla, jos avaat kansiorakennetta.

<img src="./Kuvat/Ymparisto/projekti_luotu.PNG">

Kannattaa siirtyä luotuun tiedostoon, joko terminaali komennolla:

```
cd ekaprojekti
```

Tai avaamalla VSCoden yläkulmasta File -> Open Folder ja avaamalla siellä ekaprojekti-kansion

<img src="./Kuvat/Ymparisto/avaa_kansio.PNG">

### Lisäapuja ohjelmointiin

Jotta koodaaminen olisi helpompaa, asennetaan VS Codeen pari lisäosaa:

**Svelte for VS Code**

<img src="./Kuvat/Ymparisto/svelte_lisaosa.PNG">

**Prettier**

<img src="./Kuvat/Ymparisto/prettier_lisaosa.PNG">
Prettier ei alunperin ole luotu tukemaan Svelteä, joten joudumme laittamaan terminaaliin vielä komennon:

```
npm i --save-dev prettier-plugin-svelte prettier
```

Näillä päästään alkuun!

Sovellus käynnistyy komennolla:

```
npm run dev
```
