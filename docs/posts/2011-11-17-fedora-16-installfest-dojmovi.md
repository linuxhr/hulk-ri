---
title: "Fedora 16 InstallFest: dojmovi"
date: 2011-11-17
categories: 
  - sveuciliste
tags: 
  - installfest
  - linux
  - predavanje
  - rijeka
authors: 
  - vedranm
---

Treći u nizu, i žešći od prethodna dva. Mjesto za susret onih koji žele Linux i onih koji znaju kako ga instalirati, mjesto za učenje, razmjenu iskustava i naravno zabavu.

Susret je otvorio Marko s uvodom u Fedoru i Linux uopće; pitanja su se uglavnom vrtila oko GNOME 3 desktopa i [Gnome Tweak Toola](https://wiki.gnome.org/action/show/Apps/GnomeTweakTool) koji je pritom demonstrirao. Moćan alat; omogućuje da vratite "Power Off" u izbornik, minimize gumb u title bar prozora, traku s minimiziranim prozorima i još mnogo toga.

Zanemarimo li trollove koji su zlobno ili dobrohotno tvrdili da Fedora nikom ne radi, imali smo nekoliko očekivanih problema i par neočekivanih. Idemo redom.

<!-- more -->

Očekivali smo Broadcom kartice; kao i obično, kod BCM4312 LP-PHY modela potrebno je nabaviti non-free firmware nakon čega kartica uredno radi. Problem je jedino taj što Fedora ima b43-fwcutter 014, a non-free firmware sa [LinuxWireless.org](https://wireless.wiki.kernel.org/) zahtijeva 015; to smo riješili ručnim instaliranjem novije verzije.

BCM4313 kartice (_"Domagoj, David, što li je to?"_ (...) _"Aaa, da, da, imali smo to prošli put."_) zahtijevaju non-free `broadcom-wl` dostupan preko RPMFusiona. Nadajmo se da će uskoro [brcm80211](https://wireless.wiki.kernel.org/en/users/drivers/brcm80211) biti dio mainline kernela te da to neće biti potrebno.

Bežične mrežne koje nisu bile Broadcom (jedna Realtek i jedna _"nisam gledao koja jer je radila"_ (c) Domagoj) uredno su radile iz prve bez dodatnog firmwarea.

Probleme s KMS-om na jednom Intel + AMD hybrid graphics laptopu nismo uspjeli riješiti; David je optimistično pokušao osposobiti Intel, ali bez rezultata obzirom da je BIOS u najbolju ruku tragičan. Sličnih problema imali smo na jednom Intel-only laptopu; izgleda da će trebati još neko vrijeme da se `intel` driver sredi za novije grafičke kartice u više laptopa, obzirom da na sličnoj konfiguraciji David nije imao problema. To smo na kraju riješili isključivanjem KMS-a i korištenjem `vesa` drivera što dakako nije optimalno rješenje, ali je prihvatljivo.

Fedora zahtijeva barem 768MB RAM-a za instalaciju; to nam je onemogućilo instalaciju na jednom laptopu koji ima 640MB (i što je zanimljivije, baršunastu podlogu za ruke; nismo uspjeli shvatiti je li tvornički ili korisnički rad).

Iduća zanimljiva kategorija problema je četiri primarne particije; neki laptopi u zadanim postavkama imaju takvu particionu shemu: Windows 7 system volume i C particija, D particija za korisnikove podatke i proizvođačeva koja služi za reinstalaciju sustava. Time smo bili jako iznenađeni, ali riješit ćemo tako da korisnik omogući brisanje jedne od njih, koju ćemo potom stvoriti kao logičku.

Ukupno smo imali desetak laptopa, i osim ovih problema većina instalacija prošla uspješno i novi korisnici Fedore se čine vrlo zadovoljni.
