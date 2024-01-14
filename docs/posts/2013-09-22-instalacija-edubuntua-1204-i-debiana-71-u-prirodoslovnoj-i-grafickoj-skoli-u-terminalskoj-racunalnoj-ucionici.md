---
title: "Instalacija Edubuntua 12.04 i Debiana 7.1 u Prirodoslovnoj i grafičkoj školi u terminalskoj računalnoj učionici"
date: 2013-09-22
categories: 
  - sveuciliste
tags: 
  - debian
  - edubuntu
  - instalacija
  - linux
  - ltsp
  - ubuntu
authors: 
  - vedranm
---

U već uobičajenom stilu sredili smo još jednu terminalsku učionicu instalacijom nama jako dragog [Edubuntua](https://www.edubuntu.org/) [12.04](https://old-releases.ubuntu.com/releases/edubuntu/12.04.0/release/) na LTSP poslužitelj, ovaj puta u [Prirodoslovnoj i grafičkoj školi u Rijeci](http://ss-prirodoslovna-graficka-ri.skole.hr/). Ovo je naša treća instalacija te verzije Edubuntua, nakon [one na Odjelu za informatiku Sveučilišta u Rijeci](2012-09-21-instalacija-edubuntua-1204-u-racunalnoj-ucionici-odjela-za-informatiku.md) i [one na Tehničkom fakultetu Sveučilišta u Rijeci](2013-03-24-instalacija-edubuntua-1204-na-ritehu-u-terminalskoj-racunalnoj-ucionici-i8.md).

<!-- more -->

Učionica se sastoji od poslužitelja na kojem je postavljen [LTSP](https://ltsp.org/) te 16 terminala koji se pokreću preko [PXE](https://en.wikipedia.org/wiki/Preboot_Execution_Environment)\-a. Za instalaciju smo razmotrili i [Debian Edu (Skolelinux)](https://wiki.debian.org/DebianEdu) 7.1 beta, ali smo se zasad odlučili za Edubuntu, prvenstveno zato što je Debian Edu 7.1 još uvijek beta.

Međutim, Debian Edu 7.1 u našim se eksperimentima pokazao izrazito dobar, a posebno cijenimo da se iz verzije u verziju smanjuje [broj paketa koji se razlikuju od istoimenih paketa standardnog Debiana](http://ftp.skolelinux.org/skolelinux/wheezy_needs_love.html), te da je vremenski odmak izdavanja finalne verzije Debian Edua od izdavanja finalne verzije standardnog Debiana sve kraći. Odlučili smo ga temeljitije istestirati u budućnosti, konkretnije kod iduće serije nadogradnji usporedno sa Edubuntuom 14.04 LTS.

Instalacija je protekla ugodno i glatko, što nije iznenađujuće. Na poslužitelj smo instalirali [GNOME 3](https://www.gnome.org/gnome-3/) Fallback grafičko sučelje, i postavili da se isto grafičko sučelje pokreće na terminalima. Osim GNOME sučelja, poinstaliran je softver potreban za školske predmete: [Firefox](https://www.mozilla.org/firefox/), [Chromium](https://www.chromium.org/), [Bluefish](https://bluefish.openoffice.nl/), [PHP](https://www.php.net/), [MySQL](https://www.mysql.com/) i još ponešto. Veseli nas da se ovako mnogo slobodnog softvera koristi u nastavi.

Layout tipkovnica je po zadanim postavkama bio engleski, no podesili smo adekvatno na hrvatski layout automatskim izvršavanjem `setxkbmap hr`. Postavili smo NAT na poslužitelju kako bi terminali u učionici mogli pristupati internetu bez obzira koristi li se LTSP ili ne.

Na Samsung 730XT terminale smo instalirali odličan [Debian 7.1](https://www.debian.org/News/2013/20130615) wheezy sa Xfce sučeljem, zbog ograničenog prostora od 2GB koliko ima prostora za pohranu unutar terminala. Unatoč tome što [službena dokumentacija](https://www.debian.org/releases/stable/i386/apds02.html.en) navodi da je za instalaciju potrebno više od 2GB, pojedine _Recommended_ pakete koji nam nisu potrebni moguće je ne instalirati i time smanjiti ukupnu veličinu instalacije. Debian je moguće dodatno smanjiti prema [uputama](https://wiki.debian.org/ReduceDebian) dostupnim na službenom wikiju.

Ovo je druga Linux instalacija na istim terminalima, nakon [instalacije Debiana 6.0 pred nešto više od dvije godine](2011-04-12-poziv-na-predavanje-linux-na-samsung-730xt-terminalima.md). Ciklus izdavanja novih stabilnih, odnosno LTS verzija koji su prihvatili Ubuntu i Debian nam, očito, jako paše.
