1.Készítse el a Térkép osztályt a kartográfia csomagban! A térképekről tárolni szeretnénk a
címüket, azaz hogy mit ábrázolnak (sztring), a valós méretekhez viszonyított méretarányukhoz tartozó
arányszámot (egész) és egy névjegyzéket (sztringek listája). Az osztály adattagjai legyenek védett
láthatóságúak! Készítsen az osztályhoz egy konstruktort, amelynek segítségével mindhárom
adattagjának kezdőérték adható! A konstruktor dobjon IllegalArgumentException kivételt
„Hibás méretarány!” üzenettel, ha a paraméterként megkapott arányszám nem pozitív! Definiálja felül
az equals() metódust: két térkép akkor legyen egyenlő, ha a címük és a méretarányuk (tartalmilag)
megegyezik (a típusuktól függetlenül)! Definiálja felül a toString() metódust úgy, hogy az a térkép
adatait az alábbi formában adja vissza (egy sorban, idézőjelek nélkül):
„<cím>, 1:<arányszám>[ (<név>[, <név>]...)]” (pl. „Debrecen, 1:20000 (Piac u., Nagytemplom,
DE Főépület)”)! (Segítség: lásd a String.join() metódust.)



2. Egészítse ki a Térkép osztályt egy nagybetűsít() nevű publikus logikai metódussal, amelynek
segítségével nagybetűssé alakíthatók a névjegyzékben szereplő nevek kezdőbetűi! Felteheti, hogy
minden név tartalmaz legalább egy karaktert. A metódus adjon vissza igazat, ha volt kisbetűvel kezdődő
név a névjegyzékben (azaz a metódus módosította a térképet), különben pedig hamisat! (Segítség: lásd a
List interfész get() és set(), a String osztály charAt() és substring(), valamint a
Character osztály isLowerCase() és toUpperCase() metódusait.)



3. A térképek természetes rendezettsége a címük szerint lexikografikusan növekvő sorrendben legyen
értelmezve! Ha két térképnek azonos a címe, akkor közülük a részletesebb (nagyobb méretarányú)
kerüljön előrébb a rendezettségi sorrendben (az 1:1000 méretarányú térkép részletesebb, mint az
1:10000 méretarányú)! Ha a méretarányok is megegyeznek, akkor a nagyobb névjegyzékkel rendelkező
térkép kerüljön előrébb (azaz amelyikben több név szerepel)!



4. Származtasson a Térkép osztályból egy TematikusTérkép osztályt szintén a kartográfia
csomagban! A tematikus térképekről tárolni szeretnénk még azok témáját is (sztringként). Az új adattag
csak a kartográfia csomagban látszódjon! Készítsen az osztályhoz egy olyan konstruktort,
amelynek segítségével mindegyik adattagjának kezdőérték adható! Definiálja felül a toString()
metódust úgy, hogy az a Térkép sztring reprezentációját adja vissza, kiegészítve azt a végén egy
vesszővel, egy szóközzel és a térkép témájával (pl. „Magyarország, 1:1100000, domborzat”)! Definiálja
felül a nagybetűsít() metódust is úgy, hogy a térkép névjegyzékében szereplő nevek kezdőbetűin
kívül a térkép témájának kezdőbetűjét is alakítsa nagybetűssé! A metódus visszatérési értéke továbbra is
akkor legyen igaz, ha módosította a térképet, azaz vagy a névjegyzékben szereplő nevek valamelyike,
vagy a téma kisbetűvel kezdődött!



5. Adott az alábbi interfész a térképKiadó csomagban:
public interface TérképTár
{
// hozzáadja a paraméterként megkapott tömbben szereplő térképeket a
// térképtárhoz
public void hozzáad(Térkép[] térképek);
// visszaadja a térképtárban található olyan térképek listáját a természetes
// rendezettségük sorrendjében, amelyek névjegyzékében legalább a második
// paraméterként megkapott darabszámú név szerepel; ha az első paraméter igaz,
// akkor csak a tematikus térképeket, ha hamis, akkor mindegyiket
public java.util.List<Térkép> térképek(boolean csakTematikus, int nevekSzáma);
// visszaadja a paraméterként megkapott címmel rendelkező térképek névjegyzékeinek
// az unióját lexikografikusan növekvő sorrendben; ügyeljen arra, hogy egy elem
// csak egyszer fordulhat elő a teljes névjegyzékben!
public java.util.Collection<String> teljesNévjegyzék(String cím);
}



Készítse el az Atlasz osztályt a kartográfia csomagban, amely a megjegyzéseknek megfelelően
implementálja a TérképTár interfészt! Az osztály nem tartalmazhat nyilvános adattagokat! Figyeljen
arra, hogy egy atlasz több azonos című és méretarányú térképpel is rendelkezhet! Legyen lehetőség az
atlasz címének tárolására! Készítsen az osztályhoz egy konstruktort, amelynek segítségével megadhatjuk
az atlasz címét, valamint feltölthetjük azt egy térképeket tartalmazó (tetszőleges) kollekció elemeivel!
Definiálja felül a toString() metódust úgy, hogy az az első sorban az atlasz címét, majd egy üres
sort követően soronként az egyes térképeket adja vissza! (Segítség: lásd a TreeSet osztályt, valamint a
Collections.addAll() és a Collections.sort() metódusokat.)
