+++
template = "hu_index.html"
title = "Kérdések"
+++

# Gyakori kérdések és válaszok

## Hogyan zajlik a gépészeti projektek megvalósítása?

Ha nincs rendelkezésre álló CAD terv az első lépés az elemzés és egy ajánlat
adása.

* fénykép küldése. Lehetőleg 2-3 kép, ami a terméket körbe mutassa meg – az
  ajánlat annál pontosabb minél több az adat
* befoglaló méret mm-ben, vagy a képeken mérőszalag, vonalzó használata
* opcionálisan: terméktömeg grammban, szín és anyagminőség (Pl. ABS, PLA, PP stb.)
* ajánlat adása részemről


Ha az ajánlatot elfogadja, akkor:

* mintatermék küldése (lehet enyhén sérült, lokálisan törött, a lényeg, hogy
  kivehető legyen a geometria). Lehet tükörkép is, ha csak az áll rendelkezésre
* 3D szkennelés, vagy egyszerűbb eseteben kézi mérés
* 3D CAD adat készül a termékről, ez alapján fog történni a programírás
* szeletelő program (slicer) használatával program írása
* 3D nyomtatás
* amennyiben szükséges utómunka FDM – szálas 3D nyomtatás esetén támaszok
  eltávolítása, csiszolás, furat kalibrálás…
* SLA (folyadékos, gyantás nyomtatás) esetén támaszok eltávolítása, csiszolás,
  furat kalibrálás, izopropil alkoholos mosás, szárítás, UV-kezelés…

Amennyiben rendelkezésre áll a CAD terv

* CAD adat küldése. Lehetőleg step, iges vagy jó minőségű stl fájl küldése
  e-mail csatolmányként, óriásfájlként
* opcionálisan: szín és anyagminőség (Pl. ABS, PLA, PP stb.)
* ajánlat adása részemről
* ha az ajánlatot elfogadja, akkor:
* a fogadott CAD adat alapján fog történni a programírás. A CAD adat módosítása
  az ön egyeztetésével történik – ha szükséges, egyébként az eredeti modell
  kerül kinyomtatásra.
* szeletelő program (slicer) használatával program írása
* 3D nyomtatás
* amennyiben szükséges utómunka FDM – szálas 3D nyomtatás esetén (támaszok
  eltávolítása, csiszolás, furat kalibrálás…)
* SLA (folyadékos, gyantás nyomtatás) esetén (támaszok eltávolítása, csiszolás,
  furat kalibrálás, izopropil alkoholos mosás, szárítás, UV-kezelés…)

## Videókon láttam, hogy a 3D nyomtatás gyors technológia, gyakorlatilag percek, vagy 1-2 óra alatt elkészül a kész termék.

Az esetek túlnyomó részében nem igaz. Vannak rövid idejű nyomtatások és a
technológia fejlődésével a gyártási idők 5 év alatt 1/5-1/10-ére csökkentek.
Alapvetően a térformázó szerszámokban történő nyomásos öntéshez képest ez egy
eléggé időigényes gyártási technológia. A  nagy sebességű felvételek ú.n.
timelapse videók, amelyek a munkafolyamatot teszik látványossá, mutatják
gyorsítva a termék felépülését.

## 3D nyomtatással csak dísztárgyak készülhetnek, funkcionális (a terhelést elviselő) alkatrészek nem?

Természetesen nem igaz. Az öntéskor az anyagrészek kohéziós kötéssel
kapcsolódnak egymáshoz, ez valóban nagyobb terhelhetőséget tesz lehetővé, még a
3D nyomtatásnál rétegek mentén adhéziós kötés alakul ki. Azonban növelhető a
terhelhetőség az öntött alkatrész szintjére a geometria átdolgozásával és a
megfelelő anyagválasztásával (lásd nyomtatóbarát terméktervezés).

## Ha 3d nyomtatáskor a terméket tömören – 100%-os kitöltéssel – nyomtatjuk, akkor érjük el a legnagyobb szilárdságot.

Nem így van, mert a szilárdság elsősorban a falak számának növelésével érhető
el, pl. 2 helyett 4-5 fal már tetemes szilárdságnövelést jelent. Másodsorban a
kitöltés adja a merevséget, 70%-os kitöltés majdnem teljesen azt a fizikai
jellemzőt adja, mint a 100% és ebben az esetben az anyagtakarékosság nem
elhanyagolható.

## Ha van egy mintadarabom, csak be kell 3d szkenneltetni, és „automatikusan” indul a 3d nyomatás!

Ez sajnos így nem igaz, illetve csak nagyon elenyésző esetben és főleg
dísztárgyak esetén. Mindenképpen kell CAD modellt építeni, vagy javítani a
szkennelt stl fájlt.

## A rosszabb minőségű durva hálózású stl fájl nem okoz gondot, mert a nyomtató úgy is „kijavítja”.

Sajnos nem így van, a durva hálózás okozta geometria torzulás, pl. sokszög alakú
kör keresztmetszet „megjelenik” a nyomaton, ezért fontos a jó minőségű mesh
fájl.

## Egy szkennelt állományból a szoftver automatikusan „készít” CAD modellt, így a visszamodellezés automatikus.

Ez csak nagyon ritkán járható út. A szkennelés lyukmentes legyen, illetve a
geometria is megfelelő formájú kell hogy legyen, pl. csalihal figura vagy egyéb
szabadformájú felületekkel határolt testek esetén működhet. Ez az ú.n. auto
meshing parancssorozat, de itt is inkább az irányított hálózású auto mesh
generálás a célszerűbb, ami már „félautomatikus” módszer. Tehát legtöbbször
szükséges CAD modellt építeni a szkennelt hálóból

## Miért viszonylag magas a visszamodellezés költsége?

Mert viszonylag kevesen csinálják ezt a munkafolyamatot és nagy rutin, valamint
– ahogy a neve is utal rá – fordított CAD modellezési szemléletet is igényel.
Továbbá mérlegelnie kell a tervezőnek, mely részek kopottak, amelyeket a
megfelelő mérettel kell a CAD modellen felépíteni.

## A 3D szkenner 3D CAD adatot készít.

Nem, az eredmény térben elhelyezkedő pontsokaság, amelyet a szoftver
„háromszögel” le, amelynek eredményeképpen sztereolitográfia, azaz
háromszögekkel reprezentált adat (stl fájl) készül.

## A 3D szkenner lézerrel készíti az stl adatot.

Nem, a lézer a méréshez kell, a pontok térbeli elhelyezkedésének
meghatározásához. A felületet letapogatása optikai eszközzel készül.

## Miért kell a 3D szkennelt felület fehér porral vagy festékkel lefújni?

Ezt anti-reflexív spray-nek is nevezik, amely a fényes felületről történő
fényvisszaverés, a „becsillogás” megakadályozása miatt történik. Hasonlóan a
hagyományos fényképezéshez.
