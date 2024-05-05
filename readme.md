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
Šis ir Node.js projekts, kas pielieto Nightwatch.js, ar mērķi veikt tīmekļa vietnes, github.com, dažādu scenāriju automātisko testēšanu. Projektā tiek pielietots Page Objects izkārtojums, ar mērķi padarīt testu uzturēšanu un rakstīšanu vieglāku.

### Izmantotās Node.js un npm versijas
Node.js versija: v20.12.2
npm versija: 10.5.2

## Projekta uzstādīšana
1. Noklonējiet šo repozitoriju uz savu lokālo datoru.
2. Pārliecinieties, ka jums ir instalētas Node.js un npm.
3. Izmantojot terminālu, pārvietojieties uz projekta mapes atrašanās vietu.
4. Izpildiet komandu `npm install`, lai instalētu projekta atkarības.

## Nightwatch Config Faila Iestatījumi
Nightwatch konfigurācijas fails (`nightwatch.conf.js`) ir konfigurēts šādi:

- `src_folders`: Norāda, kur atrodas testu faili.
- `page_objects_path`: Norāda, kur atrodas Page Objects izkārtojumu.
- `webdriver`: Konfigurē Selenium WebDriver sākšanu, norādot portu un vai vajadzētu vai nē.
- `test_settings`: Iestatījumi testiem, tostarp noklusējuma pārlūka iestatījumi un konkrēti iestatījumi konkrētiem pārlūkiem.

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
Testu palaišana (default) browserī
npm run test -- -t {src}/{test}

Testus var palaist chrome(default) browserī sekojoši:

-`npm run test -- -t .\tests\loginTests.js`

-`npm run test -- -t .\tests\repositoryTests.js`

-`npm run test -- -t .\tests\topicDescriptionTests.js`


Testu palaišana norādot browseri
npm test -- -t {src}/{test} --env {browser}

Testus var palaist chrome vai firefox browseros sekojoši:

-`npm run test -- -t .\tests\loginTests.js --env chrome`

-`npm run test -- -t .\tests\repositoryTests.js --env firefox`

-`npm run test -- -t .\tests\topicDescriptionTests.js --env firefox`



### Testu paralēla palaišana

Visu testu palaišana paralēli. Lai palaistu testus paralēli, failā `nightwatch.conf.js` uzstādiet test_settings -> default -> test_workers -> enabled=`true` un palaidiet komandu:

-`npm test`
