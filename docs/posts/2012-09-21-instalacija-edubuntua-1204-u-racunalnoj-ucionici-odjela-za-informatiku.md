---
title: "Instalacija Edubuntua 12.04 u računalnoj učionici Odjela za informatiku"
date: 2012-09-21
categories: 
  - sveuciliste
tags: 
  - edubuntu
  - libreoffice
  - ltsp
  - ubuntu
authors: 
  - vedranm
---

Popodnevni dio današnjeg dana iskoristili smo za nadogradnju instalacije Edubunuta 10.10 u računalnoj učionici 117 na [Odjelu za informatiku Sveučilišta u Rijeci](https://www.inf.uniri.hr/).

<!-- more -->

Navedena učionica sastoji se od poslužitelja koji ima postavljen [LTSP](https://ltsp.org/) i 20 terminala koji se pokreću preko [PXE](https://en.wikipedia.org/wiki/Preboot_Execution_Environment)\-a. Razmotrili smo [Skolelinux](http://www.slx.no/) 6.0.4 i [Edubuntu](https://www.edubuntu.org/) 12.04.1 i odlučili se za ovaj potonji zbog jednostavnije instalacije, atraktivnijeg izgleda i popularnosti distribucije [Ubuntu](https://ubuntu.com/). Kako bi pojednostavili postupak instalacije i izbjegli eventualne probleme koje može uzrokovati nadogradnja, odlučili smo se za čistu instalaciju.

Jedan od noviteta koje vrijedi spomenuti, u odnosu na 10.10, je automatsko postavljanje LTSP-a tijekom instalacije u slučaju da korisnik tako želi. Pored toga, korisniku se u procesu instalacije nudi odabir grafičkog sučelja: pored standardnog Unityja, nudi se i GNOME 3 Fallback ("failback", ako pitate našeg Domagoja :-) ).

Nakon instalacije [iskoristili smo `gconftool-2` da bi isključili zaključavanje ekrana](https://wiki.ledhed.net/index.php/Gnome_Lockdown#Disable_Lock_Screen), a zatim `lts.conf` datoteci specificirali automatsku prijavu. Iz nekog razloga tipkovnica je nakon automatske prijave bila postavljena na američku; to smo riješili dodavanjem `.desktop` datoteke unutar `/etc/xdg/autostart` koja vrši `setxkbmap hr`.

Naposlijetku, na isti način omogućili smo da LTSP klijent izvši isključivanje računala umjesto odjave korisnika; naredba je `xprop -root -f LTSP_LOGOUT_ACTION 8s -set LTSP_LOGOUT_ACTION HALT` (može se naći na nekoliko mjesta na internetu, nama je pomogao [ovaj Debian bug report](https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=564264)).

Prvi dojmovi o Edubuntuu 12.04 su vrlo dobri, radi jednako brzo kao 10.10, ako ne i brže, a puno je ljepši. Nadamo se da će se i studentima svidjeti te da će uživati u radu. :-)
