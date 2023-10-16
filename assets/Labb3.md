# Labb3
Du har fått i uppgift att färdigställa en WPF-applikation som representerar en butik.

I applikationen ska alla listor och knappar ha passande funktionalitet. Exempel:

* ```Admin```-knappen ska registrera en ny användare av typen ``Admin``.
* ``Login``-knappen ska logga in användaren som det den är registrerad som (Admin/Customer)

När programmet startar ska produktlistan och användarlistan läsas in, om filen inte finns ska det skapas filer för detta i AppData/Local.

När programmet avslutas ska Produktlistan och Användarlistan sparas i respektive fil.

Alla metoder som är tillagda ska användas till det de är där för.

Klasserna `User`, `Admin`, `Customer`, `Product`, `UserManager` och `ProductManager` får utökas men inte ändras(**!**). Det är alltså okej att lägga till kod men inte ändra befintlig kod.

## Redovisning

### Hämta repot och jobba här: https://classroom.github.com/a/6M0M2WTp

Uppgiften ska lösas individuellt.

Du ska boka in minst 2 handledningstillfällen under arbetet, ett senast en vecka efter uppgiftens start och en senast 3 dagar före deadline. OBS! Det första tillfället måste alltså bokas men inte genomföras inom en vecka efter uppgiftens start alltså.
Vid detta samtal ska du visa hur långt du kommit och ställa minst tre frågor om något du fastnat på eller vill ha hjälp med. Samtalet ska ta max 15 minuter.
Om man inte gör detta klarar man inte uppgiften

## Betygskriterier

### För godkänt

* Man skall lämna in en planering med tillhörande klassdiagram för arbetet **Deadline för planering och klassdiagram: 29/10-2023**
* Koden ska fungera enligt ovan beskrivning.
* Programmet skall fungera utan krasch.
* Filer för både kunder och produkter ska sparas som JSON.
* Både att spara och läsa fil skall ske asynkront.
* Alla klasser skall ha lämpliga konstruktorer.

### För väl godkänt krävs även

* Koden ska vara väl strukturerad och lätt att förstå
* Lösningen ska inte innehålla massa onödig kod.
* Det ska vara skalbart och enkelt att utöka.
* Man ska även implementera extrauppgiften enligt nedan.

### OBS! Extra uppgift som krävs för VG!

Som extra uppgift vill kunden gärna ha följande extra funktionalitet:

* Produkter ska kunna ha bilder kopplade till sig.
* Man ska kunna filtrera lagret och affären efter produkttyp.

## Tips och hjälp

Environment.GetFolderPath(Environment.SpecialFolder.LocalApplicationData) returnerar sökvägen till användarens ‘/appdata/local’ mapp För hantering av filer och mappar, kolla upp följande klasser:
Path, Directory, StreamWriter, StreamReader
Tänk på att göra både user input och lagrad data till lower case innan du jämför dem om du vill att ditt program ska vara case insensitive.

ListView kan användas för att visa produktlistor och kundkorg och Open-/Save-Dialog kan användas för att öppna/spara filer.

Kolla upp Asynkron programmering här för mer info kring hur du skapar ett asynkront anrop.

WPF: https://wpf-tutorial.com/

JSON och read/write file: https://github.com/niklas-hjelm/ReadWriteFileDemo/tree/Json
