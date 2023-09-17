# Lab2 – Skapa en simpel butik

Din uppgift är att färdigställa en konsollaplikation som skall agera som en enkel affär.
När programmet körs så ska man få se någon form av **meny** där man ska kunna välja att **registrera ny kund** eller **logga in**. Därefter ska ytterligare en **meny** visas där man ska kunna välja att **handla**, **se kundvagn** eller **gå till kassan**.

Man ska endast kunna handla, logga ut eller gå till kassan om man är inloggad.

Om man inte är inloggad ska man endast kunna registrera ny kund eller logga in.

Om man väljer att handla ska man få upp **minst 3 olika** **produkter** att köpa (t.ex. Korv, Dricka och Äpple). Man ska se **pris** för varje **produkt** och kunna lägga till en eller flera varor i sin **kundvagn**.

Kundvagnen ska visa alla produkter man lagt i den, styckpriset, antalet och totalpriset samt totala kostnaden för hela kundvagnen.
Kundvagnen skall sparas i kund och finnas tillgänglig när man loggar in. (OBS, för godkänt behöver det inte sparas mellan körningar)

Exempel:
```
Kundvagn:
Äpple 2st 10kr/st = 20kr
Korv 1st 20kr/st = 20kr
Dricka 3st 15kr/st = 45kr
Totalt: 85kr
```

När man ska Registrera en ny kund ska man ange Namn och lösenord. Dessa ska sparas och namnet ska inte gå att ändra.

Väljer man Logga In så ska man skriva in namn och lösenord. Om användaren inte finns registrerad ska programmet skriva ut att kunden inte finns och fråga ifall man vill registrera ny kund. Om lösenordet inte stämmer så ska programmet skriva ut att lösenordet är fel och låta användaren försöka igen. Lösenordet ska bara kollas om användaren finns registrerad och metoden CheckPassword i Customer ska användas för att kontrollera lösenordet.

I klassen Kund skall det finnas en ToString() som skriver ut Namn, lösenord och kundvagnen på ett snyggt sätt.

## Redovisning

Uppgiften ska lösas individuellt. </br>
[Följ denna länk!](https://classroom.github.com/a/Raa2kh6o) Detta tar dig till en plattform som heter GitHub Classroom.</br>
När du accepterat uppgiften kommer du att få ett privat repository på GitHub som du kan arbeta i. </br>
Detta repository innehåller en mall för den applikation du ska skapa.</br>
Du får utöka mallen med fler klasser och metoder om du vill.</br>
Du får lägga till parametrar i metoder men inte ta bort några.</br>
Du får inte ändra access modifiers eller lägga till/ta bort static på några properties eller metoder.</br>

## Betygskriterier

### För godkänt

* Samtliga metoder i startkoden ska vara implementerade och användas där det är lämpligt.
* Koden ska fungera enligt ovan beskrivning.
* Man ska kunna få ut korrekt totalpris och antal i kundvagnen.
* ToString() ska vara implementerad.
* Programmet skall fungera utan krasch.
* Det skall gå att skapa ny kund, lägga till föremål i kundvagnen, titta i sin kundvagn och sedan fortsätta handla.
* Log in ska fungera för minst 3 fördefinierade kunder.
  * Kund1: Namn="Knatte", Password="123"
  * Kund2: Namn="Fnatte", Password="321"
  * Kund3: Namn="Tjatte", Password="213"
* Det skall gå att logga ut och in men inget krav på att skapade kunder skall finnas kvar emellan körningar.

### För väl godkänt krävs även

* Koden ska vara väl strukturerad och lätt att förstå
* Lösningen ska inte innehålla massa onödig kod.
* Det ska vara skalbart och enkelt att utöka.
* Man ska även implementera extrauppgiften enligt nedan.

## OBS! Extra uppgift som krävs för VG

Som Extra uppgift ska man på något sätt implementera 3 nivåer av kund (Gold, Silver och Bronze), dessa ska ha olika mycket rabatt.

* Gold: 15% rabatt på hela köpet
* Silver: 10% rabatt på hela köpet
* Bronze: 5% rabatt på hela köpet

Nivåerna skall implementeras med hjälp av arv av basklassen Kund.

Programmet ska också spara alla registrerade kunder så att de går att använda emellan körningar. (OBS! Kundvagnar behöver ej sparas) Tips: textfil.

Man ska också kunna välja att se priser i minst 3 olika valutor (två ytterligare förutom SEK).

## Inlämning sker före deadline