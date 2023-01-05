## Juhend, kuidas redigeerida `config.json` faili, et kuvada ainekursust õppekeskkonnas

`config.json` fail peab vastama json-formaadi nõuetele. Kui sa oled config-failis muudatused ära teinud, siis kontrolli, et selle sisu vastab json-formaadi nõutele: http://jsonlint.com . Vastasel juhul ainekursust õppekeskkonnas ei kuvata.

Kõik kommentaarid, mis on siin juhendis algusega "//" kuuluvad ainult juhendi faili – `config.json` peab olema puhtas json-formaadis. <br />
Muudatused teha otse `config.json` faili <br />

## Terminite tähendus:

- _slug_ – unikaalne lühike nimi objekti kohta, mida viidatakse ka URL aadressis. Ingl. keeles: _the unique identifying part of a web address, typically at the end of the URL._

### Terminite tähendused `config.json` failis:


``` js
{ 
  "courseName": "Kursuse näide", // "Kursuse nime" asemele kirjuta kursuse nimi 
  "courseCode": "HK1234.HK", // "Ainekood" asemele kirjuta ainekood 
  "slug": "kursuse_naide", // "kursuse-nimi" asemel kirjuta aine lühinimi, mida millele viitab rakenduse URL aadress. See on ainekursuse põhiaadress.
                           // Näide: https://github.com/tluhk/HK_Programmeerimine-II/blob/master/docs/files/kursuse-nimi-example.png. 
                           // Kasuta ainult tähti. Tühiku asemel kasuta sidekriipsu "-". Lubatud pole tühikud, numbrid, muud sümbolid. 
  "courseUrl": "https://ois2.tlu.ee/tluois/aine/HK1234.HK", // Lisa siia ainekursuse ainekava link (ÕIS-i link)
                                                            // Näide: "https://ois2.tlu.ee/tluois/aine/HKI5003.HK". 
  "active": true, // Määra, kas ainekursus on aktiivne või mitte. Kui "true", siis seda kursust kuvatakse rakenduses. Kui "false", siis ei kuvata. 
  "docs": [
    {
      "slug": "about", // Viitab docs kaustas asuvale about.md failile, kus saab lahti kirjeldada kursuse ülesehituse ja hindamismudeli 
      "name": "Ainekursusest" // Pole vaja muuta 
    }
  ],
  "additionalMaterials": [
    {
      "slug": "lisamaterjalid", // Viitab docs kaustas asuvale lisamaterjalid.md failile, kus saab lahti kirjeldada kõik üldised ainega seotud lisamaterjalid 
      "name": "Aine lisamaterjalid" // Pole vaja muuta 
    }
  ],
  
  // Algab loengute massiiv. Nii palju kui on docs kaustas loengute kaustasid, peaks olema ka siin massiivis viiteid loengute kohta. Kausta nimi ja siinne loengu slug peavad kattuma.
  // NB! Loengute kaustu võib olla rohkem kui siinseid viiteid kaustadele, kuid viiteid kaustadele EI TOHI olla rohkem kui kaustu ise. 
  "lessons": [
    {
      "name": "Loeng 1 (näidisfailid)", // Kuidas kuvatakse rakenduses loengu nime. Võid muuta. 
      "slug": "loeng_01", // Viitab docs kaustas asuvale loengukaustale. Slug peab kattuma ühe loengukausta nimega!
                          // Ühtlasi kasutatakse loengu slug-i selle URL aadressis, näiteks localhost:3000/kursuse-nimi/loeng_01. 
      "components": ["numbrid", "sisu-loomise-juhend", "praktikum_01"], // Massiiv, mis kirjeldab millised sisuteemad ja/või praktikumid kuuluvad loengu alla.
                                                                 // Massiivi tuleb lisada config.json faili concepts või practices osades nimetatud elementide slug-e. Nende slug-id viitavad omakorda repositooriumi concepts või practices kaustades olevatele alamkaustadele. 
      "additionalMaterials": [
        {
          "slug": "lisamaterjalid", // Viitab docs/loeng_XX kaustas asuvale lisamaterjalid.md failile, kus saab lahti kirjeldada loenguga seotud lisamaterjalid.
          "name": "Loengu lisamaterjalid" // Pole vaja muuta 
        }
      ]
    },
    // Peale koma tuleb järgmise loengu info: 
    {
      "name": "Loeng 2",
      "slug": "loeng_02",
      "components": ["funktsioonid", "praktikum_02"],
      "additionalMaterials": [
        {
          "slug": "lisamaterjalid",
          "name": "Loengu lisamaterjalid"
        }
      ]
    }
  ], // Selle nurksuluga lõppeb loengute massiiv. Kui on soov lisada rohkem loenguid, siis tuleb loengute massiivi lisada uus loengu objekt kirjeldatud struktuuri alusel.

   // Algab sisuteemade massiiv. Massiiv sisaldab sisuteemade objekte, igas objektis on vajalik name ja slug võtmed. Nii palju kui on concepts kaustas sisuteemade kaustasid, peaks olema ka siin massiivis viiteid nendele kaustadele. Kausta nimi ja siinne concept slug peavad kattuma!
   // NB! Sisuteemade kaustu võib olla rohkem kui siinseid viiteid kaustadele, kuid viiteid kaustadele EI TOHI olla rohkem kui kaustu ise. 
  "concepts": [
    {
      "slug": "naidis-sisuteema", // Viitab concepts kaustas asuvale sisuteema kaustale. Slug peab kattuma ühe sisuteema kausta nimega!
                                  // Ühtlasi kasutatakse seda slug-i sisuteema URL aadressis, nt localhost:3000/kursuse-nimi/loeng_01/naidis-sisuteema. 
      "name": "Näidis Sisuteema" // Kuidas kuvatakse rakenduse menüüs sisuteema nime. Võid muuta. 
    },
    {
      "slug": "sisu-loomise-juhend",
      "name": "Sisu loomise juhend"
    },
    {
      "slug": "funktsioonid",
      "name": "Funktsioonid"
    }
  ], // Selle nurksuluga lõppeb sisuteemade massiiv. Kui on soov lisada rohkem sisuteemasid, siis tuleb sisuteemade massiivi lisada uus sisuteema objekt kirjeldatud struktuuri alusel. 
  
  // Algab praktikumide massiiv. Massiiv sisaldab praktikumide objekte, igas objektis on vajalik name ja slug võtmed. Nii palju kui on practices kaustas praktikumide kaustasid, peaks olema ka siin massiivis viiteid nendele kaustadele. Kausta nimi ja siinne concept slug peavad kattuma!
  // NB! Praktikumide kaustu võib olla rohkem kui siinseid viiteid kaustadele, kuid viiteid kaustadele EI TOHI olla rohkem kui kaustu ise. 
  "practices": [
    {
      "slug": "praktikum_01", // Viitab practices kaustas asuvale praktikumi kaustale. Slug peab kattuma ühe praktikumi kausta nimega! 
                              // Ühtlasi kasutatakse seda slug-i praktikumi URL aadressis, nt localhost:3000/kursuse-nimi/loeng_01/praktikum_01. 
      "name": "Näidis Praktikum" // Kuidas kuvatakse rakenduse menüüs praktikumi nime. Võid muuta. 
    },
    {
      "slug": "praktikum_02",
      "name": "Praktikum 2"
    }
  ] // Selle nurksuluga lõppeb praktikumide massiiv. Kui on soov lisada rohkem praktikume, siis tuleb praktikumide massiivi lisada uus praktikumi objekt kirjeldatud struktuuri alusel. 
}

```
