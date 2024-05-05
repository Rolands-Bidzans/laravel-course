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
Šis ir Node.js projekts, kas izmanto Nightwatch testus, lai automātiski testētu tīmekļa lietotnes. Projekts izmanto Page Objects izkārtojumu, kas padara testu uzturēšanu un izpildi vieglāku.

### Izmantotās Node.js un npm versijas
Node.js versija: 14.17.0
npm versija: 6.14.13

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
Lai palaistu testus, izmantojiet šādas komandas:

### Konkrēta testa palaišana
