---
title: "InstallFest uspješan!"
date: 2010-10-28
categories: 
  - sveuciliste
tags: 
  - 3g
  - audio
  - b43
  - codec
  - compiz
  - fedora
  - firmware
  - installfest
  - multimedija
  - openoffice
  - rijeka
  - ubuntu
  - usb
  - video
  - wireless
authors: 
  - vedranm
---

Održali smo naš prvi InstallFest, i to prilično uspješno. Instalirali smo 2 dual-boot Ubuntua i dodali potreban softver na 2 [Wubi](https://www.ubuntu.com/desktop/get-ubuntu/windows-installer) Ubuntua. Zanimljivo je kod ovih potonjih da je C:\\ disk od Windowsa po defaultu uredno mountan u /host.

<!-- more -->

Ugodno smo iznenađeni činjenicom da nije bilo ama baš nikakvih problema sa 3D-om i KMS-om (radilo se o ATI i Intel grafikama), a Broadcomove kartice BCM4312 LP-PHY su uredno proradile sa driverom `b43` nakon instalacije firmwarea (kojeg Ubuntu ima u repozitorijima, tako da nije potrebno koristiti alat `fwcutter`).

Bilo je malo problema sa CarNET/VIP/Vodafone Huawei E620 adapterom, koji smo uz Davidove sugestije uspjeli učiniti da radi (treba paket `usb-modeswitch` i naredbu `modprobe option`; ovo drugo je doslovno `modprobe option`, modul jezgre se zove `option`). Čini se da i Fedora ima neke probleme s dozvolama kod tih uređaja (treba dodati korisnika u grupu `dialout`). David, naš kolega iz [LinuxLaba](http://linuxlab.riteh.hr/), imao je odgovor na to i na skoro svako drugo pitanje i uvelike je pomogao.

Flash i audio/video codeci su uredno instalirani iz Ubuntuovih repozitorija i zvuk je svim prisutnima uredno radio.

Bilo je vrlo čudnih situacija sa Touchpadom i USB mišem na jednoj Toshibi kod koje su na oba tipke nakon određenog vremena otkazivale poslušnost, što nismo uspjeli riješiti. Moglo bi se razumijeti da Touchpad ima problema zbog pregrijavanja, ali USB miš ne.

Pored toga su neki od prisutnih zaključili kako "ponekad USB 3G modemi prorade kad ih samo ištekaš i uštekaš", "Ctrl + D \[u Nautilusu\] je vrlo koristan", "Windowsi su spori", "OpenOffice je skoro isti kao Office", "treba redovito čistiti laptop" i "ne treba kupovati Toshibu". Ove tvrdnje samo navodimo kao zanimljive reakcije sudionika, i one ne predstavljaju naše stavove.

Posjećenost je bila odlična. Broj ljudi se u prosjeku kretao između 15 i 20, i većinom su to bili studenti.
