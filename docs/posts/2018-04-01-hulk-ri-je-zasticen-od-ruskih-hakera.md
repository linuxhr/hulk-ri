---
title: "HULK-Ri je zaštićen od ruskih hakera"
date: 2018-04-01
categories: 
  - podruznica
tags: 
  - apache
  - hakiranje
  - nginx
  - openra
authors: 
  - vedranm
---

Brojni su [članci napisani zadnjih mjeseci](https://www.nytimes.com/news-event/russian-election-hacking) o utjecaju ruskih hakera na demokratske izbore i druge institucije diljem svijeta. Zbog toga će vam zasigurno biti drago čuti da je [Riječka podružnica](../podruznica.md) [Hrvatske udruge Linux korisnika](http://www.linux.hr/) poduzela brojne mjere predostrožnosti kako bi se zaštitila od te vrlo zabrinjavajuće prijetnje.

<!-- more -->

Jedan od renomiranih ruskih hakera u zajednici slobodnog softvera otvorenog koda je Igor Vladimirovich Sysoev, [bivši student](https://en.wikipedia.org/wiki/Igor_Sysoev) [Baumanke](https://bmstu.ru/) u Moskvi, začetnik [nginxa](https://nginx.org/) i mogući dalji ili bliži rođak, a možda i sin Vladimira Sysoeva, upravitelja [Tesla Towera](https://www.rt.com/news/170704-tesla-tower-lightning-russia/) [preostalog iz sovjetskoga doba](https://www.rt.com/news/181748-tesla-marx-generator-lightning/) u šumi pored Moskve. Sličan je toranj čak i danas dostupan za kupnju u manjoj varijanti za 1500$ i to u [Red Alertu](https://cnc.fandom.com/wiki/Tesla_coil_(Red_Alert_1)), a ta igra radi na modernim Linux distribucijama zahvaljujući projektu [OpenRA](https://www.openra.net/about/).

Igor Vladimirovich je toliko ruski da ima [osobnu web stranicu na .ru domeni](http://sysoev.ru/), a toliko haker da je isprogramirao značajan dio nginxa, tako da je svakako reprezentativan za govoriti u ime svih ruskih hakera. Zamolili smo ga za komentar o sigurnosti web stranica i druge infrastrukture HULK-Ri, na što nam je rekao sljedeće:

> Kada sam u pauzi za kavu i cigaretu od hakiranja izbora u Kambodži i programiranja [NGINX Unita](https://unit.nginx.org/) [čučeći kao obično](https://www.slavorum.org/gopniks-why-do-slavs-squat/) pokušao hakirati HULK-Ri, shvatio sam da to neće biti nešto što ću uspjeti napraviti u 5 minuta kao i druge stvari. Naime, pokrenuvši [cURL](https://curl.se/) naredbom `curl` vidio sam
>
> `$ цурл -И www.ри.линух.хр`  
> `ХТТП/1.1 200 ОК`  
> `Дате: Сун, 01 Апр 2018 20:58:24 ГМТ`  
> `Сервер: Апаче`
>
> oh pardon, vi u Hrvatskoj imate drugačija slova, dakle, pokrenuvši `curl` vidio sam
>
> `$ curl -I www.ri.linux.hr`  
> `HTTP/1.1 200 OK`  
> `Date: Sun, 01 Apr 2018 20:58:24 GMT`  
> `Server: Apache`
>
> nakon čega sam shvatio da mi ovdje ne može pomoći moj izrazito super jako tajni totalno nondisclosed backdoor prisutan u svakoj [instanci nginxa](https://www.similartech.com/technologies/nginx) (da da čak i u onima koje koriste stranice s video materijalom i puno posjeta koje nisu YouTube ako me kužite hehehe). Iznimka je ona instanca nginxa koju sam specifično kompajlirao za [Russia Today](https://www.rt.com/about-us/), propagan... medijsku kuću pod upravom našeg velikog vo... predsjednika Vladimira Putina.
>
> Međutim, HULK-Ri koristi [Apache](https://httpd.apache.org/) tako da sam se prilikom pokušaja hakiranja osjećao kao Napoleon u maršu na Moskvu te se razočaran vratio na hakiranje izbora u Kambodži i doradu [naše implementacije gRPC-a](https://www.nginx.com/resources/webinars/nginx-http2-server-push-grpc/) pustivši ovo za neku drugu priliku.

Mi smo se u HULK-Riju zahvalili Igoru na ovoj detaljnoj analizi i želimo mu puno sreće u daljnjem radu na nginxu i drugim projektima, a svima koji nas prate želimo sretan prvi april.
