## Ainekursuse loengute haldamine
    
### Uue loengu lisamine: `lessons/loeng_XX` kaustad

1) Uue loengu tegemiseks lisa `lessons` kausta uus alamkaust ja lisa sellele vastav nimi, näiteks "loeng_03".
    - NB! Loengu kausta nimi tohib koosneda tähtedest, numbritest ja alakriipsust. Ära kasuta täpitähti ja erisümboleid. Tühikud ei ole lubatud, tühiku asemel kasuta alakriipsu "_" . <br />
    - Loengule saad anda unikaalse nime `config.json` failis. Loengu kaustale anna aga üldine nimi, soovitavalt nimeta neid järjest numbritega: "loeng_01", "loeng_02" jne.
2) Loengu kausta sisse tee fail `about.md`, kus kirjeldad üldiselt loengu sisu: loengu eesmärke ja õpiväljundeid. <br />
3) Loengu kausta loo fail `lisamaterjalid.md`. Selles failis viita loenguga soenduvatele lisamaterjalidele, võid seda teha tekstina või URL-linkidena. Selle faili sisu kuvatakse õppekeskkonnas "Loengu lisamaterjalid" lehel.
4) Loengu kaustas olevasse `files` kausta saad lisada loenguga seonduvaid faile, mis kuuluvad loengu lisamaterjalide hulka. Kui `files` kaustas on mõni fail, siis  kuvatakse need automaatselt õppekeskkonnas "Loengu lisamaterjalid" lehel. 
    - `lisamaterjalid.md` failis ei ole vaja `files` kausta sisule viidata.
    - NB! `files` kaustas peab olema vähemalt üks fail, Githubi kaust ei või olla tühi! Vaikimisi on igas `files` kaustas fail `.gitkeep`, mida õppekeskkonnas ei kuvata. St, et sul pole kohustust lisada igale loengule mõnda seonduvat faili, kuid kontrolli, et `.gitkeep` fail oleks alati `files` kaustas olemas.

### Loengule sisuteemade ja/või praktikumide lisamine: `config.json` fail
Loeng koosneb sisuteemadest ja/või praktikumidest.

`config.json` failis tuleb lisada loengu `components` massiivi soovitud järjekorras sisuteemade ja praktikumide nimed, millest loeng koosneb:

<img width="630" alt="Screenshot 2022-12-28 at 13 17 07" src="https://user-images.githubusercontent.com/62253084/209804141-f415d370-be9a-43a8-bfda-cfa31282fe52.png">
    
Kui sa lisad loengu `components` massiivi nimesid, siis peab sama nimi esinema kindlasti `config.json` failis kas `concepts` või `practices` massiivis:

<img width="329" alt="Screenshot 2022-12-28 at 13 27 27" src="https://user-images.githubusercontent.com/62253084/209805446-42bb6750-ad33-4079-8b7f-ae50d20c6b17.png">

### Soovitus:

**Uue loengu lisamiseks** soovitame kopeerida juba olemasolevate loengute kaustasid, nimetada kopeeritud kaustad ümber uue loengu numbriga ning uuendada kopeeritud kaustade sisu uue loengu sisuga. Siis ei pea sa alati üksikasjalikult looma eraldi uusi `about.md`, `lisamaterjalid.md` faile ega `files` kaustasid. Lihtsalt kopeeri ja muuda olemasolevate failide/kaustade sisu.

## Muud nõuded

Kogu õppematerjali sisu tuleb salvestada **Markdown** (.md) formaadis. [Täpsemalt Markdown formaadist](https://github.com/tluhk/HK_Programmeerimine-II#muud-nõuded).
    
