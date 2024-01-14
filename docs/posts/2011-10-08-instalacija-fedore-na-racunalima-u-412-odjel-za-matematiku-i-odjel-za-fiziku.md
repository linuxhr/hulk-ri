---
title: "Instalacija Fedore na računalima u 412 (Odjel za matematiku i Odjel za fiziku)"
date: 2011-10-08
categories: 
  - sveuciliste
tags: 
  - fedora
  - yum
  - fortran
  - emacs
  - gnuplot
authors: 
  - vedranm
---

Ovaj tjedan smo za potrebe izvođenja nastave iz kolegija **Računalna fizika** na [Odjelu za fiziku](https://www.phy.uniri.hr/) [Sveučilišta u Rijeci](https://uniri.hr/) instalirali [Fedoru 15](https://fedoraproject.org/wiki/F15_one_page_release_notes). Naš [David Dubrović](https://www.antares.hr/o-nama/) je na tu informaciju reagirao sa "znači, postajemo Fedora-Ri umjesto HULK-Ri" :-D

<!-- more -->

Šalu na stranu, način razmišljanja je bio isti kao i u [prethodnom slučaju sa RiTeh učionicom](2011-10-02-instalacija-fedore-na-racunala-u-ucionici-i3-riteh.md), trebalo nam je nešto popularno i moderno, a Ubuntu s Unityjem nitko baš ne voli previše.

Sva računala u 412 imaju disk kapaciteta 80 GiB, koji je bio cijeli predviđen za particiju na kojoj su instalirani Windowsi XP. Particiju od Windowsa smanjili smo na ~40GiB, a nakon toga smo instalirali Fedoru na preostali prostor. Obzirom na poznate Fedorine [probleme sa](https://bugzilla.redhat.com/show_bug.cgi?id=590369) [smanjivanjem](2011-05-27-drugi-installfest-vrlo-uspjesan.md) [NTFS particija](https://bugzilla.redhat.com/show_bug.cgi?id=733808), koristili smo [Parted Magic](https://distrowatch.com/table.php?distribution=partedmagic).

Problema nakon instalacije nije bilo, jedino što nadogradnji ima oko ~500MiB pa sam proces instalacije svih potraje oko pola sata. Na jednom smo računalu slučajno napravili reboot za vrijeme nadogradnje, ali je naredba `yum-complete-transaction` riješila stvar.

Potom smo instalirali [gnuplot](http://www.gnuplot.info/), [Emacs](https://www.gnu.org/software/emacs/) i [GFortran](https://gcc.gnu.org/wiki/GFortran). Domagoju se baš svidjela Fortran sintaksa.

Sve u svemu, Fedora uredno radi i smatramo ovu akciju velikim uspjehom.
