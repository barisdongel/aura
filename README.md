# Aura - GDG[x]
[![MadeWithVueJs.com shield](https://madewithvuejs.com/storage/repo-shields/1444-shield.svg)](https://madewithvuejs.com/p/aura/shield-link)
[![Build Status](https://travis-ci.org/gdg-x/aura.svg?branch=master)](https://travis-ci.org/gdg-x/aura)

<img width="100%" src="https://i.hizliresim.com/qlqn50.png">

GDGler için standart web uygulaması. <br>
[Demo](https://aura-client-master.firebaseapp.com/) <br>
Version: 1.0.6

## Genel Bakış

Aura GDG'ler için standart olarak oluşturulmuş, birkaç dakika içinde kurulabilen bir Web şablonu.

Bu şablon [GDG Jalandhar](https://meetup.com/GDG-Jalandhar/) takımı tarafından hazırlanmıştır. GDG Konya ekibi olarak da kurulumu Türkçeleştirilmiştir.

## Özellikleri
| Özellik | Açıklama |
|---|---|
| **Hızlı ve optimize** | PWA on Lighthouse |
| **Offline Çalıştırılabilir** | Offline çalışabilir. |
| **Mobil uyumlu** | Mobo Friendly Web app can be installed as a native app on your phone |
| **SEO öptimizasyonu** | index all content and get to the top in search results |
| **Yönetimi kolay** | keep and update all information in the JSON File |


## Başlangıç
1. Projeyi forklayın (https://github.com/barisdongel/aura) ve bilgisayarınıza indirin.
1. Proje bağımlılıklarını indirin. Projenizin olduğu dizinde bir komut satırı çalıştırın ve: `npm install` 
1. `urlname` Alan adını (`CHAPTER_URL_NAME`)  [here](/src/config/key.js) ve Chapter url name kısmını projede ki dosyalardan düzenleyin.
1. Projenizi localhost'da çalıştırmak isterseniz konsola: `npm run serve` yazın.
1. `Meta Tag`, `Title Tag` ve [Google Analytics Code](https://analytics.google.com/analytics/web/#/) Bu kısımları projenizde ki index.html dosyasından düzenleyin. [Basic Info](/public/index.html), [manifest.json](/public/manifest.json) ve [Resources](/src/assets/data)
1. Değişikliklerin kayıt olması yani projenizin üretilmesi için: `npm run build`.
1. Test etmek için: `npm run test`

## Firebase Hosting'e Gönderme

1. Firebase dağıtımı için Kurulum:
   *Firebase CLI'yı yükleyin: `npm i -g firebase-tools`
1. Bir firebase hesabı oluşturun. [Firebase account](https://console.firebase.google.com) ve giriş yapın [Firebase CLI](https://firebase.google.com/docs/cli/): `firebase login`
1. terminali açın /CMD/Powershell in your dir.
1. Şimdi `firebase login` yazın ve açılan pencerede kullanmak istediğiniz firebase hesabınızı seçip (İzin Ver) diyin.
1. `firebase init` yazın.
1. Ok tuşlarını kullanarak projeyi seçin.
1. Daha sonra `Hosting` butonunun üzerine gelip SPACE basın. Hosting seçili olduğunda ENTER.
1. “What do you want to use as your public directory? (public)” diye bir soru gelicek. `dist`. yazın
1. Gelen sorulara `No` diyin. (for Single page web app.)
1. Varsayılan olarak dosyalar başarıyla oluşturulacaktır.
1. Local'de çalıştırın
   * `firebase serve` ya da `npm run serve`
1. Firebase.json dosyası
    ```js
        {
            "hosting": {
                "public": "dist",
                "rewrites": [ {
                    "source": "**",
                    "destination": "/index.html"
                } ],
                "ignore": [
                    "firebase.json",
                    "**/.*",
                    "**/node_modules/**"
                ]
            }
        }
    ```
1. Tamamlanması ve Deploy edilmesi
   * `firebase deploy` yazarak sitenizin Firebase Hosting'e deploy edilmesini sağlayın. Ve bitti...

### Documentation
1. The [Getting Started guide](#getting-started) is probably a good first point of call! <br>
1. [Full documentation](/docs).

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

## Technology Stack

* [VueJS](https://vuejs.org/)
* [Vuetify](https://vuetifyjs.com/en/)
* [Firebase](https://firebase.google.com/)
* [Service Worker & PWA](https://www.npmjs.com/package/vue-pwa)
* [Workbox](https://developers.google.com/web/tools/workbox)

## Contributing

Awesome! Contributions of all kinds are greatly appreciated. To help smoothen the process we have a few non-exhaustive guidelines to follow which should get you going in no time.

### Using GitHub Issues

- Feel free to use GitHub issues for questions, bug reports, and feature requests
- Use the search feature to check for an existing issue
- Include as much information as possible and provide any relevant resources (Eg. screenshots)
- For bug reports ensure you have a reproducible test case
  - A pull request with a breaking test would be super preferable here but isn't required

### Submitting a Pull Request

- Squash commits
- Lint your code with eslint (config provided)
- Include relevant test updates/additions

## Contributors
<b>Maintainer:</b> [Vrijraj Singh](https://github.com/vrijraj)

### View Website Built with Projects

| Community Name | Web App Link |
| --- | --- |
| GDG Jalandhar | [View Now](https://gdgjalandhar.com) |
| GDG Kuala Lumpur | [View Now](https://www.gdgkl.dev/) |
| GDG Fortaleza | [View Now](http://gdgfortaleza.com.br/) |
| GDG Kozhikode | [View Now](https://gdgkozhikode.org/) |
| GDG Delta | [View Now](https://gdgdelta.com/) |
| GDG Tokyo | [View Now](https://tokyo.gdgjapan.org/) |
| GDG Yangon | [View Now](https://gdgyangon.org/) |
| GDG Gran Canaria | [View Now](https://gdggrancanaria.org/) |
| GDG Santander | [View Now](https://gdgsantander.com/) |
| GDG Ciudad del Este | [View Now](http://gdgcde.org/) |
| GDG Ilorin | [View Now](https://gdg-ilorin-d9f0d.firebaseapp.com/) |
| GDG Chetumal | [View Now](https://gdg-chetumal.firebaseapp.com/) |
| GDG Porto | [View Now](https://gdgporto-aura.firebaseapp.com/) |
| GDG Istanbul | [View Now](https://gdgist.firebaseapp.com/) |
| GDG Port-of-Spain | [View Now](https://gdgpos.com/) |
| GDG Jeddah | [View Now](https://www.gdgjed.com/home) |
| GDG Sevilla | [View Now](https://www.gdgsevilla.com/) |
| GDG Madeira | [View Now](https://gdgmadeira.xyz/) |
| GDG Chandigarh | [View Now](https://gdg-chd.web.app/) |
| GDG Rochester | [View Now](https://gdgrochester.com/) |
| GDG Sri Lanka | [View Now](https://gdgsrilanka.org) |
| GDG Lafia | [View Now](https://lafia.gdg.ng/) |
| GDG Kinshasa | [View Now](https://gdg-kin.firebaseapp.com/) |
| Dev Cluster Goa | [View Now](https://beta.devcluster.community/) |
| GDG Cloud Calgary | [View Now](https://gdgyyc.com/) |
| GDG Cloud SF | [View Now](https://cloudsf.withgdg.com/) |
| GDG Nagpur | [View Now](https://gdgnagpur.com/) |
| GDG Kolkata | [View Now](https://gdgkolkata.org/) |
| GDG Ahmedabad | [View Now](http://gdgahmedabad.com/) |
| GDG Fremont | [View Now](https://gdg-fremont.firebaseapp.com/) |
| GDG Savannah | [View Now](https://gdgsavannah.com/) |
| GDG San Salvador | [View Now](https://gdgsansalvador.dev/) |
| GDG Indore | [View Now](https://gdgindore.in/) |
| GDG Pescara | [View Now](https://gdgpescara.it/en/) |
| GDG CDE | [View Now](http://gdgcde.org/) |
| GDG Galicia | [View Now](https://gdggalicia.com/) |
| GDG Campobasso| [View Now](https://gdgcampobasso.it/) |
| GDG Galway | [View Now](https://gdg-galway.com/) |
| GDG Nizhny Novgorod | [View Now](https://gdgnnsite-62ac7.firebaseapp.com/) |
| GDG Madurai | [View Now](https://www.gdgmadurai.in/) |
| GDG Bristol | [View Now](https://gdgbristol.org/) | 
| GDG Ranchi | [View Now](https://www.gdgranchi.in/) |
| GDG Chennai | [View Now](https://gdgchennai.in)|
| GDG Kano | [View Now](http://kano.gdg.ng/)|
| GDG Gandhinagar |[View Now](https://gdggandhinagar.org/) |
| GDG Craiova | [View Now](https://gdgcraiova.dev/) |
| GDG Houston | [View Now](https://gdghoustontx.org/) |
| GDG Cloud Ahmedabad | [View Now](https://gdgahmedabad.cloud/) |
| GDG Cloud Hanoi | [View Now](https://gdgcloudhanoi.com/) |
| GDG Ulaanbaatar | [View Now](https://gdgub.org/) |
| GDG Ado-Ekiti | [View Now](https://gdgadoekiti.com) |
| GDG Gwalior | [View Now](https://gdggwalior.in/) |
| GDG Pune | [View Now](https://gdgpune.org/) |
| GDG Aalborg | [View Now](https://gdgaalborg.dk/) |
| GDG Reading | [View Now](https://www.gdgreading.dev/) |
| GDG Kolachi | [View Now](https://www.gdgkolachi.com/) |
| GDG Denizli | [View Now](https://gdgdenizli.com/) |
| GDG Little Rock | [View Now](https://gdglittlerock.web.app/) |
| GDG Vilnius | [View Now](https://gdg-vilnius-aura.firebaseapp.com/) |
| GDG Osijek | [View Now](https://www.gdg-osijek.com/) |
| GDG Vienna | [View Now](https://gdgvienna-c9011.web.app/) |
| GDG Konya | [View Now](https://gdgkonya.com) |



Project is published under the [MIT license](/LICENSE.md).  
Feel free to clone and modify repo as you want, but don't forget to add reference to authors :)
