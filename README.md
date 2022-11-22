
https://arato.inf.unideb.hu/panovics.janos/beugrok_Java.pdf


Feladat: Szőlőbirtok kezelés.
Egy szőlőbirtok több parcellából áll. Egy parcellát a következő adatok
jellemeznek:
Helyrajzi szám, szőlőfajta, tőkeszám
A szőlőfajta egy enum, ami ezeket tartalmazza:
Kékfrankos, Furmint, Leányka
Minden parcellához lehet felvenni éves termést.
Az éves termés 3 adatot tratalmaz:
  év(ez lehet int, nem kell LocalTime), összetrmés, tőkére vetitett átlagos
termés (ez számított érték)
Részfeladatok:
1.: parcella felvétele
2.: parcellához termési adat felvétele, a parcellát helyrajzi szám alapján
választjuk ki
3.: parcella adatainak módosítása helyrajzi szám alapján, a helyrajzi szám
nem módposítható, minden más igen
4.: termés adat módosítása helyrajzi szám és évszám alapján, csak az össz
etrmés módosítható, az átlagot újra számolja
5.: a fenti pontok összefogása egy menürendszerben
