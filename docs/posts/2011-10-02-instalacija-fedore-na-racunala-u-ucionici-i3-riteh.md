---
title: "Instalacija Fedore na računala u učionici I3 (RiTeh)"
date: 2011-10-02
categories: 
  - sveuciliste
tags: 
  - deltarpm
  - fedora
  - gnome3
  - kdenlive
  - ns
  - pygraphviz
  - riteh
authors: 
  - vedranm
---

Tijekom ovog tjedna zajedno s [LinuxLabovcima](http://linuxlab.riteh.hr/) instalirali smo [Fedoru 15](https://fedoraproject.org/wiki/F15_one_page_release_notes) na računala u računalnoj učionici I3 na [Tehničkom fakultetu Sveučilišta u Rijeci](http://www.riteh.uniri.hr/). Namjera nam je bila za potrebe radionica na konferenciji [LKLK](http://lklk.eu/) i budućih vikend aktivnosti zamijeniti Ubuntu 10.10 nečim modernijim, nečim što ima [GNOME 3](https://www.gnome.org/gnome-3/), pa je odluka pala da to ovaj put bude Fedora.

<!-- more -->

Učionica I3 sastoji se od 20 računala za studente i 1 računala za nastavnika. Konačni rezultat je sljedeći: 15 računala ima 64-bitnu verziju Fedore 15, 5 račuanala ima 32-bitnu, a nastavničko ima pre-release verziju Fedore 16 (koja radi sasvim solidno).

Jedina veća poteškoća javila se zbog toga što dio računala učionici ima za Linux predviđenu root particiju od 5 GiB, što je na Fedori, zbog korištenja [deltarpma](https://github.com/rpm-software-management/deltarpm), nedovoljno da bi se uspješno mogli instalirati updateovi nakon instalacije OS-a. To smo riješili tako da smo reinstalirali i zamijenili particije predviđene za root i home; 9 GiB pokazalo se za Fedoru sasvim dovoljno.

Problema s podrškom za hardver nije bilo, a konfiguracija mreže i automatskog logiranja pod GNOME-om 3 još je jednostavnija nego prije. [ns-3](https://www.nsnam.org/), instaliran ručno u korisnikovom kućnom direktoriju, uredno radi (uz iznimku ns-ovog modula **pyviz** koji zahtijeva [pygraphviz](https://pygraphviz.github.io/), koji Fedora nekim čudom nema u repozitorijima).

Vrijedi spomenuti problem s [Kdenliveom](https://kdenlive.org/) (dostupnim iz [RPM Fusiona](https://rpmfusion.org/)) koji se uredno ne želi pokrenuti. Međutim, David se snašao i otkrio da alternativa, [OpenShot](https://www.openshot.org/), uredno radi tako da je radionica održana neometano.

Ipak, bez obzira na ove stvari, vrlo smo zadovoljni i konferencijom, i radionicama, i Fedorom u I3.
