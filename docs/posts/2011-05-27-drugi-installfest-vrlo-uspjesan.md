---
title: "Drugi InstallFest vrlo uspješan!"
date: 2011-05-27
categories: 
  - sveuciliste
tags: 
  - broacom
  - fedora
  - firefox
  - flash
  - gnome
  - installfest
  - iptables
  - libreoffice
  - yum
authors: 
  - vedranm
---

Održan je i naš drugi InstallFest, uspješniji od prvog. Instalirali smo 3 dual-boot [Fedore](https://fedoraproject.org/) i zaključili da [ntfsresize](http://www.linux-ntfs.org/) ne radi uvijek savršeno, pa nije preporučljivo u instalaciji raditi promjenu veličine particije, a ako se dogodi da se Windowsi ne bootaju nakon neuspješnog `ntfsresize`, [testdisk](https://www.cgsecurity.org/wiki/TestDisk) + Windows Rescue spašava stvar.

<!-- more -->

Ipak, "reklo bi se da nije problem u Fedori" (u prijevodu, ako ne koristite `ntfsresize`, stvar uredno radi).

[GNOME 3](https://www.gnome.org/gnome-3/), [Firefox](https://www.mozilla.com/firefox/) 4 i [LibreOffice](https://www.libreoffice.org/) uredno rade. Ovaj prvi je naročito zapalio ekipu i od svuda se moglo čuti "i jaa bii GNOOMEE 3!". LibreOffice nije dio standardnog LiveCD-a, pa smo ga na jednom laptopu naknadno instalirali (`yum groupinstall "Office/Productivity"`).

Kad već govorimo o GNOME 3, moramo reći da je tajni agent pod pseudonimom JJ u nekom trenutku spomenuo, sasvim nonšalantno, kako je tipka "Alt" vrlo korisna jer omogućuje Shutdown i Reboot u GNOME 3 umjesto u zadanim postavkama omogućenog Suspenda. To je šokiralo sve prisutne, a jednog od voditelja nagnalo da kaže nešto u stilu "JJ, ti si kralj! Oprošteno ti je što mi nisi poslao [Anacondu](https://fedoraproject.org/wiki/Anaconda)."

Ugodno smo iznenađeni činjenicom da nije bilo ama baš nikakvih problema sa 3D-om i KMS-om (osim kod određenih pehista s Radeonom HD 5xxx, op.a.). To smo riješili instalacijom rawhide 2.6.39 kernela (`yum --enablerepo=rawhide update kernel\*`).

Ovaj puta nismo imali `b43` kartica; zezali smo se malo s jednom `broadcom-wl` karticom (BCM4313), koja je nakon instalacije modula is [RPMFusiona](https://rpmfusion.org/) uredno proradila.

Bilo nas je desetak, i imali smo 5 laptopa. Eksperimentirali smo s `iptables`-om i forwardingom paketa, kako bi dobili vezu na internet i izbjegli RPM dependancy hell kod instalacije `broadcom-wl` paketa.

Bilo je opet sitnih problema sa VIP/Vodafone Huawei E620 adapterom; treba paket `usb-modeswitch` koji je instaliran u zadanim postavkama instalacije i naredbu `modprobe option`; ovo drugo je doslovno `modprobe option`, modul jezgre se zove `option`. Marko je pronašao rješenje na [Red Hatovoj Bugzilli](https://bugzilla.redhat.com/show_bug.cgi?id=698975).

Flash je uredno instaliran s Adobeove stranice. Tu nije bilo baš nikakvih problema.

Krajnji rezultat je 3:0 za Fedoru, ali to je manje važno; važniji je uspjeh koji ovo predstavlja za zajednicu slobodnog sofvera u cjelini. Sve u svemu, jedva čekamo [Fedoru 16](https://fedoraproject.org/wiki/Releases/16/Schedule) i još ovakvih evenata.
