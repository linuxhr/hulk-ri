---
title: "Instalacija Edubuntua 12.04 na RiTehu u terminalskoj računalnoj učionici I8"
date: 2013-03-24
categories: 
  - sveuciliste
tags: 
  - edubuntu
  - ltsp
  - riteh
  - ubuntu
authors: 
  - vedranm
---

Subotnje jutro i rano popodne jučerašnjeg dana iskoristili smo za instalaciju i konfiguriranje [Edubuntua 12.04](https://www.edubuntu.org/), koji se pokazao odličnim za terminalske računalne učionice. Instalaciju smo izvršili u prostoriji I8 na [Tehničkom fakultetu Sveučilišta u Rijeci](http://www.riteh.uniri.hr/).

<!-- more -->

Učionica I8 sastoji se od poslužitelja na kojem je postavljen [LTSP](https://ltsp.org/) te 20 terminala koji se pokreću preko [PXE](https://en.wikipedia.org/wiki/Preboot_Execution_Environment)\-a. Za instalaciju smo razmotrili i [Skolelinux 6.0.4](http://www.slx.no/), no odlučlili smo se za Edubuntu zbog stabilnosti i [već steknutog pozitivnog dojma](2012-09-21-instalacija-edubuntua-1204-u-racunalnoj-ucionici-odjela-za-informatiku.md) o toj distribuciji. Prethodna verzija instalirana u učionici je bila kombinacija Ubuntua 10.10 (na poslužitelju) i 11.04 (na klijentima).

Instalacija je protekla ugodno i glatko, što nije iznenađujuće. Na poslužitelja smo instalirali [KDE](https://www.kde.org/), [GNOME 3](https://www.gnome.org/gnome-3/) Fallback i [Unity](http://unity.ubuntu.com/) grafička sučelja, ostavljajući korisnicima izbor po želji, dok se na terminalima pokreće GNOME 3 Fallback, koji je dovoljno lightweight da radi solidno brzo. U slučaju eventualnih problema može se naknadno zamijeniti za [Xfce](https://xfce.org/) ili [LXDE](https://lxde.org/). Osim navedenog softvera, poinstaliran je softver potreban za kolegije koji se održavaju na RiTehu: osnovne build i mrežne alate, [CORE](https://www.nrl.navy.mil/itd/ncs/products/core), [ns-3](https://www.nsnam.org/), [Quagga](https://www.nongnu.org/quagga/), [iptables](https://en.wikipedia.org/wiki/Iptables), [Wireshark](https://www.wireshark.org/), [Geany](https://www.geany.org/), [NetBeans C++](https://netbeans.org/features/cpp/), [Eclipse](https://www.eclipse.org/), [PHP](https://www.php.net/), [MySQL](https://www.mysql.com/), [Qt Creator](https://wiki.qt.io/Qt_Creator), [VTK](https://www.vtk.org/) i još ponešto. Veseli nas da se ovako mnogo slobodnog softvera koristi u nastavi.

Automatska prijava studenata je napravljena, i pritom je onemogućeno automatsko uključivanje screensavera sa zaključavanjem ekrana na terminalima. Layout tipkovnica je po zadanim postavkama bio engleski, no podesili smo adekvatno na hrvatski layout automatskim izvršavanjem `setxkbmap hr`.

Edubuntu 12.04 nas nije razočarao, a vjerujemo da će i studenti koji budu u učionici slušali pojedine predmete uvidjeti napredak koji je postignut u samo godinu i pol koliko je prošlo od izdanja verzije 10.10.
