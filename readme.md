<p align="center"><img src="https://laravel.com/assets/img/components/logo-laravel.svg"></p>

Full source code of the Laravel Essentials course on Udemy

**[Get it here!](https://www.udemy.com/laravel-beginner-fundamentals/?couponCode=SOURCE_CODE)**

## Laravel Essentials Course on Udemy

This repository contains the full source code of the upcoming Udemy course.

For each lecture there is a separate branch with changes made during that lecture to clone or download.

The course is live now, get if with a discount (9.99\$):

**[Get it here!](https://www.udemy.com/laravel-beginner-fundamentals/?couponCode=SOURCE_CODE)**



# Nightwatch Testu Projekts

## Apraksts
Šis ir Node.js projekts, kas pielieto Nightwatch.js, ar mērķi veikt tīmekļa vietnes, github.com, dažādu scenāriju automātisko testēšanu. Projektā tiek pielietots Page Objects izkārtojums, ar mērķi padarīt testu rakstīšanu un uzturēšanu strukturētāku un vieglāku.

### Izmantotās Node.js un npm versijas
Node.js versija: v20.12.2
npm versija: 10.5.2

## Projekta uzstādīšana
1. Noklonējiet šo repozitoriju uz savu lokālo datoru.
2. Pārliecinieties, ka jums ir instalētas Node.js un npm.
3. Izmantojot terminālu, pārvietojieties uz projekta mapes atrašanās vietu.
4. Izpildiet komandu `npm install`, lai instalētu projekta atkarības.
5. Failā `config.js` iestatiet Jūsu, GitHub, derīgu lietotāja vārdu un paroli.
   
    ```
    validCredentials: {
   
          email: 'DerīgaisLietotājaVārds',
   
          password: 'DerīgaParole',
   
    },
    ```

## Nightwatch Config Faila Iestatījumi
Nightwatch konfigurācijas fails (`nightwatch.conf.js`) ir konfigurēts šādi:

- `src_folders`: Norāda, kur atrodas testu faili.
- `page_objects_path`: Norāda, kur atrodas Page Objects izkārtojumi.
- `webdriver`: Konfigurē Selenium WebDriver, norādot portu un iespējojot to.
- `test_settings`: Konfigurē iestatījumus testiem. Konfigurē iestatījumus noklusētam(default) pārlūkam(browserim) un chrome, firefox pārlūkiem.
- 
#### Pārlūku iestatījumi
Noklusētam(`Default`) pārlūkam tika iestatīts `webdriver`, kur definējam WebDriver iestatījumus, norādot uz `DhromeDriver` izpildāmo failu, pēc noklusējuma testiem tiks izmantots `chrome` pārlūka. Tad `screenshots` definējam to, ka testu neveiksmīgas izpildes gadījumā tiks veikts ekrānšāviens un saglabāts `./screens` direktorijā/mapē. Beidzot `test_workers` konfigurējam, ka vienlaicīgi tiks izpildīti vairāki testi, ja `enabled` ir iestatīts uz `true`.

`chrome` pārlūkam tika iestatīts `webdriver`, kas ir `DhromeDriver`, tas pats, kas tiek lietots pēc noklusējuma. Tad objektā `desiredCapabilities`, kur norāda pārlūkas iespējas instances, mēs norādam, ka testi tiks veikti `chrome` pārlūkā.

`firefox` pārlūkam tika iestatīts `webdriver`, kas ir `geckodriver`. Tad objektā `desiredCapabilities`, kur norāda pārlūkas iespējas instances, mēs norādam, ka testi tiks veikti `firefox` pārlūkā.
                

## Testu Palaišana
Lai palaistu testus, izmantojiet:

### Visu testu palaišana
Visu testu palaišana crome browserī(default):

-`npm run test`

Visu testu palaišana norādot browseri:

-`npm run test -- --env firefox`

vai

-`npm run test -- --env chrome`

### Konkrēta testa palaišana
Testus var palaist chrome(default) browserī sekojoši:

-`npm run test -- -t .\tests\loginTests.js`

-`npm run test -- -t .\tests\repositoryTests.js`

-`npm run test -- -t .\tests\topicDescriptionTests.js`

### Konkrēta testa palaišana, konkrētajā browserī
Testus var palaist chrome vai firefox browseros sekojoši:

-`npm run test -- -t .\tests\loginTests.js --env chrome`

-`npm run test -- -t .\tests\repositoryTests.js --env firefox`

-`npm run test -- -t .\tests\topicDescriptionTests.js --env firefox`

### Testu paralēla palaišana

Visu testu palaišana paralēli. Lai palaistu testus paralēli, failā `nightwatch.conf.js` uzstādiet `test_settings` -> `default` -> `test_workers` -> `enabled=true` un palaidiet komandu:

-`npm test`
