
_Tegemist on näitefailiga, mis näitab, kuidas lisada Markdown failis elemente. Eesrakenduses saab vaadata, kuidas neid elemente õppekeskkonnas kuvatakse. Soovitame paremini arusaamiseks avada antud Markdown fail redigeerimiseks._

# Pealkiri 1

Lorem ipsum dolor sit amet, consectetuer adipiscing elit.

## Pealkiri 2

Lorem ipsum dolor sit amet, consectetuer adipiscing elit.

### Pealkiri 3

Lorem ipsum dolor sit amet, consectetuer adipiscing elit.

### Näide, kuidas lisada veebilinki:

[Google avaleht](https://www.google.com)

## Näide, kuidas lisada pilti:
Pildifail tuleb lisada sisulehe kaustas olevasse `images` alamkausta. Sisulehe failis viita `images/pildifaili-nimi`.
Nurksulgudesse saad lisada pildiallkirja.

![Protsessor](images/Protsessor_Martti_Raaveli_foto.jpg)

## Näide, kuidas kuvada koodi

```
// add handlebars helpers: https://stackoverflow.com/a/32707476
const handlebars = require('./src/helpers/handlebars')(exphbs);

app.engine('handlebars', handlebars.engine);
app.set('view engine', 'handlebars');
app.set('views', path.join(__dirname, '/views'));
```

## Näide, kuidas lisada videot

Toetatud platvormid on Youtube, Vimeo, Vine, Prezi. Rohkem infot, kuidas kuvada teisi platvorme peale Youtube'i: [markdown-it-block-embed](https://github.com/rotorz/markdown-it-block-embed)

@[youtube](_y9oxzTGERs)

## Näiteid, kuidas kuvada H5P malle

Interaktiivseid H5P malle saab luua näiteks Sisuloome keskkonnas. Siin on juhend, kuidas luua Sisuloome keskkonnas H5P malle: [https://projektid.edu.ee/display/koolikott/Sisuloome+juhend](https://projektid.edu.ee/display/koolikott/Sisuloome+juhend)

Siin on viide ühele H5P mallile: [https://sisuloome.e-koolikott.ee/h5p/1985/embed](https://sisuloome.e-koolikott.ee/h5p/1985/embed)

**Kuidas sama H5P malli kuvada interaktiivselt eesrakenduses:** 

NB! teksti ja malli vahel peab olema tühi rida, see tuleneb Markdowni formaadi reeglitest.

/i/https://sisuloome.e-koolikott.ee/h5p/1985/embed

NB! H5P malle kuvatakse eesrakenduses **alati 500px kõrgusega**. Kui malli sisu kõrgus on üle 500px või alla 500px, siis kuvab eesrakendus mallile vastavalt kas kerimisriba või tühja ruumi.

**Näide, kus H5P malli sisu on üle 500px:** 

Lahenda eelmine H5P harjutus, et näha, kuidas malli sisu ületab 500px ja tekib kerimisriba.

**Näide, kus H5P malli sisu on alla 500px:** 

/i/https://sisuloome.e-koolikott.ee/h5p/3027/embed

## Näide, kuidas kuvada koodikeskkonna sisu

Toetatud platvormid on JSFiddle ja Codepen. Rohkem infot, kuidas kuvada teisi koodiplatvorme peale JSFiddle'i: [markdown-it-playground](https://www.npmjs.com/package/markdown-it-playground)

@[jsfiddle](http://jsfiddle.net/rykeller/y4848ak7/8/embedded/html,css,result/)

## Näide, kuidas kuvatakse sisuteema allikaid

Allikaid, millele sisuteema materjal põhineb, saad lisada ja muuta sisuteema kaustas olevas `sources.json` failis. Allikaid kuvatakse õppekeskkonnas iga sisuteema lehe lõpus.

- Kui sa ei taha sisuteemale allikaid lisada, siis salvesta 'source.json' fail tühja JSON-objektina.


