# Frontend perusteet

## Mitä on frontend?

Frontend on sovelluksen käyttäjälle näkyvä osuus eli käyttöliittymä.

Frontend-kehittäminen on siis käyttöliittymän kehittämisestä. Kehitystyö tehdään yhdistämällä kolmea ohjelmointikieltä: HTML, CSS ja JavaScript. Näistä HTML-kielellä luodaan sivuston/sovelluksen rakenne, CSS:llä muokataan sen ulkonäköä ja JavaScriptillä sivustolle/sovellukselle saadaan toiminnallisuuksia.

## Miten käyttöliittymää kehitetään?

Vanha tapa on luoda sovellukseen omat HTML-, CSS- ja JS-tiedostot, jotka linkitetään yhteen. Jokainen sivunäkymä on oma HTML-tiedosto, jolla on oltava HTML-rakenne (<!DOCTYPE html> <html> <head> <body>). Alla on koodin pätkä HTML-tiedoston head-tagin sisällöstä.

```html
<head>
  <meta charset="UTF-8" />
  <meta name="description" content="Treenataan html-koodausta" />
  <meta name="keywords" content="HTML, CSS, kissat" />
  <meta name="author" content="Hullu kissanainen" />
  <title>Kissimissi Patu</title>
  <!--NÄMÄ LINKITYKSET LINKITTÄVÄT HTML-SIVUUN CSS-TIEDOSTON MUOTOILUT JA JAVASCRIPTIN TOIMINNALLISUUDET -->
  <link href="kissimissi_muotoilut.css" rel="stylesheet" type="text/css" />
  <script type="text/javascript" src="snowstorm.js"></script>
  <!--JavaScript-koodi joka lisää sivustolle lumisateen-->
</head>
```

Jos sovelluksessa olisi esimerkiksi 10 sivua, tämä jouduttaisiin kirjoittamaan 10 kertaa. Ja jos myöhemmin huomattaisiin, että pitää lisätä esimerkiksi lisää JS-tiedostoja sovellukseen, muokkaukset pitäisi tehdä kaikkiin kymmeneen HTML-tiedostoon erikseen. Tai jos sovelluksessa on navigaatio sivulta toiselle, sen koodin joutuu kopioimaan jokaiseen HTML-tiedostoon.

Tällaisen sovelluksen ylläpito vaatii tarkkuutta ja riski tehdä virheitä on suuri.

Jotta säästyttäisiin toistuvan koodin kirjoittamiselta, on kehitelty **framework** eli ohjelmistokehys. Frameworkit kokoavat HTML-, CSS- ja JavaScript-koodit samaan pakettiin. Nämä paketit ovat **komponentteja**.

<img src="./Kuvat/Perusteet/komponentti.PNG">
