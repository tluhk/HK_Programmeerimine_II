## Ainekursuse sisuteemade haldamine

### Uue sisuteema lisamine:

Uue sisuteema lisamiseks tee `concepts` kausta uus alamkaust sisuteema nimega. <br />
- NB! Sisuteema kausta nimi tohib koosneda tähtedest, numbritest ja alakriipsust. Ära kasuta täpitähti ja erisümboleid. Tühikud ei ole lubatud, tühiku asemel kasuta alakriipsu "_" . <br />
- Sisuteemale saad anda unikaalse nime `config.json` failis. Sisuteema kaustale anna aga üldine nimi, soovitavalt nimeta neid lühidalt sisu järgi: "arvuti", "funktsioonid", "graafilise_disaini_ajastud" vms.
- Sisuteemade kaustad peavad olema unikaalsete nimedega. Samuti ei tohi kattuda `concepts` ja `practices` kaustas olevate alamkaustade nimed, st et loengu ja praktikumide hulgas ei tohi olla identsete nimedega alakaustu, nt  "arvuti"-nimeline kaust oleks nii `concepts` kui ka `practices` kaustas.

### Sisuteema haldamine: `concepts/sisuteema_nimi`
1) `about.md` faili lisa kogu sisuteema õppematerjal. Kasuta Markdown formaati. <br />
2) `sources.json` faili saad lisada viited allikatele, millele sisuteema materjal põhineb. Allikaid kuvatakse õppekeskkonnas iga sisuteema lehe lõpus.
    - Kui sa ei taha sisuteemale allikaid lisada, siis salvesta 'source.json' fail tühja JSON-objektina. <
3) `images` kausta lisa kõik pildifailid, millele viidatakse `about.md` failis.

## Muud nõuded

Kogu õppematerjali sisu tuleb salvestada **Markdown** (.md) formaadis. [Täpsemalt Markdown formaadist](https://github.com/tluhk/HK_Programmeerimine-II#muud-nõuded).


    
    
    
    
    
