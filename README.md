## Juhend, kuidas hallata õppeaine veebikursust Githubi kaudu

Valikpraktika aine raames loodud [õppekeskkond](https://github.com/tluhk/rif20-valikpraktika-1) loeb infot `tluhk` organisatsiooni Githubi kontolt. Rakendus loeb Githubist ainult õppeaineid, mille repositooriumite nimed algavad eesliidesega **`HK_`**, nagu näiteks "HK_Riistvara-alused", ja mille `config.json` failis on `active: true`.

**Iga õppeaine jaoks tuleb luua uus ainekursuse repositoorium**, lisada selle kaustadesse sisu ja seadistada `config.json` fail. <br />

Selleks, et lisada uue ainekursuse repositooriumi, kasuta mallina (_template_-ina) käesoleva repositooriumi (**HK_Ainekursuse_mall**) struktuuri. Seda saad teha käesoleva repositooriumi **master** branchist selle nupu kaudu: 
<img width="919" alt="Screenshot 2022-12-13 at 11 27 04" src="https://user-images.githubusercontent.com/62253084/207279361-51b2979b-7c1f-48de-9d13-544030d05161.png">

### Uue ainekursuse repositooriumi kloonimine kohalikku arvutisse

Kui uue ainekursuse repositoorium on loodud, siis saad hakata sinna lisama enda õppematerjalide sisu. Seda on parem teha lokaalses arvutis.

Järgi [seda juhendit](https://kbroman.org/github_tutorial/pages/init.html), et käivitada kohalikus arvutis git ja kloonida uue ainekursuse repositoorium kohalikku arvutisse. NB! Ära klooni seda ainekursuse malli, vaid see repositoorium, mille sa lõid malli põhjal Githubis!

Kui sa oled lokaalses repositooriumis õppematerjalid ära uuendanud, siis saada muudatused välisesse repositooriumisse [sama juhend](https://kbroman.org/github_tutorial/pages/init.html).

### Ainekursuse repositooriumi struktuur

Kursuse sisu üles laadimiseks on repositooriumis 4 kausta: `docs`, `lessons`, `concepts` ja `practices`. <br />
- `docs` kaust on mõeldud ainekursuse üldinfo hoiustamise jaoks. <br />
- `lessons` kaust on mõeldud loengute üldinfo hoiustamise jaoks. <br />
- `concepts` kaust on mõeldud aine sisuteemade hoiustamise jaoks. <br />
- `practices` kaust on mõeldud praktikumide sisu hoiustamise jaoks.<br />

Kõigis kaustades on olemas `README.md` fail, kus on täpsustav info, kuidas nendesse kaustadesse sisu lisada. <br />

`config.json` on repositooriumi olulisim fail, mille sisu määrab, kuidas kuvatakse kaustadesse lisatud sisu õppekeskkonnas.
`config.json` täitmisel on abiks fail `config-faili-juhend.md`, kus on selgitatud lahti `config.json` faili osad ja kuidas seda õigesti seadistada.

**`config.json` faili paremaks mõistmiseks vaata järgmisi Figma prototüüpe:**
- [Config.json faili seos õppeaine Githubi repositooriumiga – näitab, millistele Githubi kaustadele/failidele viitab config.json fail](https://www.figma.com/proto/YKYDrXYCWBnNZypDfyG3zT/Ainekursuse_mall_figma?node-id=26%3A121&scaling=min-zoom&page-id=26%3A94&starting-point-node-id=26%3A121)
- [Config.json faili seos eesrakendusega – näitab, millistele eesrakenduse lehekülgedele/osadele viitab config.json fail](https://www.figma.com/proto/YKYDrXYCWBnNZypDfyG3zT/Ainekursuse_mall_figma?node-id=1%3A9&scaling=min-zoom&page-id=0%3A1&starting-point-node-id=1%3A9)

## Muud nõuded

Kogu õppematerjali sisu tuleb salvestada **Markdown** (.md) formaadis. Kõik Markdown failid peavad lähtuvama [üldistest Markdown reeglitest](https://www.markdownguide.org/basic-syntax/).

### Markdown elemendid:

Siin on mõned käesoleva rakendusega spetsiifilised elemendid ja nende Markdown formaat, mida saad kasutada Markdown (.md) failides, et luua mitmekülgset õppematerjali:
- Pildi lisamine:
    - `![Pildi allkiri](images/faili_nimi.jpg)` <br />
- URL linkide lisamine:
    - `[Lehekülje nimetus](https://duckduckgo.com)`
- Viide Youtube'i videole:
    - `@[youtube](_y9oxzTGERs)`
    - sulgudes on Youtube'i video kood, mis järgneb `v=`-le, nt https://www.youtube.com/watch?v=_y9oxzTGERs
- Viide _embed iFrame_ sisule, nt H5P failid:
    - `/i/https://sisuloome.e-koolikott.ee/h5p/1985/embed`
    - viitab [sellele Sisuloome harjutusele](https://sisuloome.e-koolikott.ee/h5p/1985/embed)
- Viide mõnele _embed code environment_ sisule, näiteks JSFiddle või Codepen:
    - `@[jsfiddle](http://jsfiddle.net/rykeller/y4848ak7/8/embedded/html,css,result/)`
    - viitab [sellele JSFiddle harjutusele](http://jsfiddle.net/rykeller/y4848ak7/8/embedded/html,css,result/)
- Koodi kuvamine: 
    - \``` {
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
} \```
    - sümbolid **```** enne ja pärast koodiosa, kuvab koodi nõnda: 
    <img width="285" alt="Screenshot 2022-12-13 at 13 03 30" src="https://user-images.githubusercontent.com/62253084/207300996-967e45ef-1b2e-45c5-9ef9-e1d78c7f2e5e.png">

Samad elemendid on välja toodud ka [näitefailis](https://github.com/tluhk/HK_Programmeerimine-II/blob/master/concepts/sisu-loomise-juhend/about.md). Sama näitefaili sisu kuvatakse eesrakenduses: `Kursuse näide > Loeng 1 (näidisfailid) > Sisu loomise juhend` . Eesrakenduses saab vaadata, kuidas neid elemente õppekeskkonnas kuvatakse.
Soovitame paremini arusaamiseks avada näitefail redigeerimiseks.


