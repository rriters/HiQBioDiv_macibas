Astotais uzdevums: GEE
================

## Termiņš

Līdz ~~(2025-01-15)~~ **2025-01-27**, izmantojot
[fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)
un [pull
request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork)
uz zaru “Dalibnieki”, šī uzdevuma direktorijā pievienojot .Rmd vai .qmd
failu, kura nosaukums ir Uzd08\_\[JusuUzvards\], piemēram,
`Uzd08_Avotins.Rmd`, kas sagatavots izvadei github dokumentā (piemēram,
YAML galvenē norādot `output: rmarkdown::github_document`), un tā radīto
izvades failu.

## Premise

*Google Earth Engine* (GEE) ir *Google* korporācijas uzturēts
mākoņskaitļošanas serviss, kas ir brīvi pieejams akadēmijai un
nekomerciāliem mērķiem. Tā sniegto iemeslu dēļ, jau neilgi kopš tā
atvēršanas ir bijusi interese komerciālu projektu iztrādei tajā, kas
nesen ir arī atvērta. Šajā resursā ir vairums brīvi pieejamo Zemes
novērošanas sistēmu datu, fokusējoties uz globālu pārklājumu, tomēr
lietotāji (korketi noformētus un ievērojot procedūru) var augšupielādēt
arī citus, piemēram, reģionāla vai nacionāla pārklājuma datus. Publiski
pieejamie resursi ir apkopoti [datu
katalogā](https://developers.google.com/earth-engine/datasets).
Vispārīgi ar šī resursa iespējām un uzbūvi var iepazīties [2017. gada
publikācijā](https://doi.org/10.1016/j.rse.2017.06.031). Darbs ar GEE
galvenokārt notiek interneta pārlūkā, izmantojot JavaScript, bet pati
Google ir radījusi arī Python saskarni. Python saskarni dažādu nozaru
pētnieku sabiedrība ir paplašinājusi un ir izveidota arī R saskarne,
tiesa to lietojot ir jārēķinās ar milzīgām sintakses atšķirībām no bāzes
R un {tidyverse}, tomēr ir iespēja izmantot arī vismaz daļu R
funkcionalitātes - [piemērs](https://csaybar.github.io/rgee-examples/),
[piemērs](https://r-spatial.github.io/rgee/reference/rgee-package.html),
[CRAN](https://cran.r-project.org/web/packages/rgee/index.html),
[github](https://github.com/r-spatial/rgee). Pamata saskarnēm ir
apjomīga un iesācējiem draudzīga dokumentācija -
[grāmata](https://www.eefabook.org/), dažādi pašmācību kursi, piemēram
[šeit](https://google-earth-engine.com/) un
[šeit](https://courses.spatialthoughts.com/end-to-end-gee.html), ir
pašas Google un lietotāju sabiedrības izstrādāti [funkciju
lietošanas](https://developers.google.com/earth-engine/guides),
[funkciju argumentu](https://developers.google.com/earth-engine/apidocs)
un [uzdevumu](https://developers.google.com/earth-engine/tutorials)
piemēri.

Galvenais iemesls GEE lietošanai ir Zemes novērošanas sitēmu dati. Tomēr
šī resursa piedāvātās skaitļošanas jaudas brīžiem liek apsvērt iespējami
plašāku tā lietošanu dažādiem, tostarp šī projekta, ģeoprocesēšanas
uzdevumiem. Par to domājot, ir jāņem vērā resursu izmantošanas
noteikumi - nekomerciāliem projektiem!, kā arī gala lietotājs -
saskarsme ar GEE nav tik vienkārša kā ar, piemēram, R vai Python pašiem
par sevi, ne visiem lietotājiem būs iespējama piekļuve GEE un
pietiekošiem Google Drive resursiem rezultātu glabāšanai. Visbeidzot,
GEE piedāvātie skaitļošanas resursi ir milzīgi, tomēr tie nav
neierobežoti un pamata lietotāju ierobežojumus sasniegt nav sevišķi
grūti, turklāt uzdevumi serveros tiek izpildīti rindas kārtībā.

## Uzdevums

Uzdevumu veiciet GEE interneta pārlūkā (JavaScript) vai ar R pakotnēm,
izmantojiet [harmonizēto Sentinel-2
kolekciju](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S2_HARMONIZED#description)
visai Latvijas teritorijai. Latvijas teritoriju definējiet ar [projekta
*Zenodo*
repozitorijā](https://zenodo.org/communities/hiqbiodiv/records?q=&l=list&p=1&s=10&sort=newest)
doto 100 m vektordatu tīklu.

1.  Aprēķinus veiciet 2024. gada jūnijam ar to raksturojošo spektrālo
    joslu mediānajām vērtībām sekojoši norādītajos trīs veidos.
    Vizualizējiet rezultātu pārlūkā, lai salīdiznātu iegūtā rezultāta
    telpisko pārklājumu un uzticamību, kas ir pamatā šīm atšķirībām?

1.1. Bez mākoņu maskas;

1.2. Ar paraugā doto mākoņu masku;

1.3. Ieviesiet *s2cloudless* mākoņu un to ēnu masku.

2.  Aprēķiniet mediāno [normalizēto starpības veģetācijas
    indeksu](https://en.wikipedia.org/wiki/Normalized_difference_vegetation_index)
    visai Latvijas teritorijai. Aprēķiniem izmantojiet tikai maija līdz
    augusta (ieskaitot) mēnešus un gadus no 2018. līdz 2024. gadam.
    Aprēķinus veiciet trīs veidos (uzskaitīti zemāk), lai salīdzinātu
    iegūtos rezultātus - skaidrojiet to atšķirības un iemeslus tām.
    Visos aprēķinos izmantojiet *s2cloudless* mākoņu un to ēnu masku.

2.1. NDVI aprēķiniet visa laika perioda spektrālo joslu mediānai pēc
mākoņu un to ēnu maskēšanas;

2.2. NDVI aprēķiniet ik satelītainas fragmentam (pikseļu-uzlidojumā),
kas palicis pēc mākoņu un to ēnu maskēšanas, noslēdzošo attēlu veidojiet
kā mediānu no ik ainai aprēķinātajām NDVI vērtībām;

2.3. Mediānu no katra gada mediānas, kas iegūta aprēķinot NDVI kā 2.2.
punktā.

3.  Lejupielādējiet 2.3. rezultātu, no tā izveidojiet vienu GeoTIFF
    slāni, kura aptvertā telpa un pikseļu izvietojums atbilst [projekta
    *Zenodo*
    repozitorijā](https://zenodo.org/communities/hiqbiodiv/records?q=&l=list&p=1&s=10&sort=newest)
    dotajam rastra slānim ar 10m izšķirtspēju. Ar starpkvartiļu
    amplitūdu raksturojiet NDVI variabilitāti ik 100 m šūnā kā rastra
    slāni, kura telpisais pārklājums un pikseļu izvietojums atbilst
    [projekta *Zenodo*
    repozitorijā](https://zenodo.org/communities/hiqbiodiv/records?q=&l=list&p=1&s=10&sort=newest)
    dotajam rastra slānim ar 100m izšķirtspēju.

Kā uzdevuma risinājumu iesniedziet RMarkdown aprakstu, kurā ir iekļautas
saites uz radītajām komandu rindām.

## Padomi

Tiks ievietoti pēc jautājumu saņemšanas.
