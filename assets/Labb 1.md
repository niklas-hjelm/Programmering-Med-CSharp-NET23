# Labb 1 – Hitta tal i sträng med tecken 
Skapa en konsollapplikation som tar en textsträng (**string**) som argument till Main eller uppmanar användaren mata in en sträng i konsollen. </br>
Textsträngen ska sedan sökas igenom efter alla delsträngar som är tal som börjar </br>
och slutar på samma siffra, utan att start/slutsiffran, eller något annat tecken än </br>
siffror förekommer där emellan. </br>
ex. 3463 är ett korrekt sådant tal, men 34363 är det inte eftersom det finns </br>
ytterligare en 3:a i talet, förutom start och slutsiffran. Strängar med bokstäver i </br>
t.ex 95a9 är inte heller ett korrekt tal. </br>
 
## Skriv ut och markera varje korrekt delsträng 
För varje sådan delsträng som matchar kriteriet ovan ska programmet skriva ut en </br>
rad med **hela strängen**, men **där delsträngen är markerad** i en annan färg. </br>
Exempel output för input ”29535123p48723487597645723645”: </br>

**2953512**3p48723487597645723645 </br>
29**535**123p48723487597645723645 </br>
295**35123**p48723487597645723645 </br>
29535123p**487234**87597645723645 </br>
29535123p4**872348**7597645723645 </br>
29535123p48**723487**597645723645 </br>
29535123p487**2348759764572**3645 </br>
29535123p4872**3487597645723**645 </br>
29535123p48723**48759764**5723645 </br>
29535123p4872348**7597**645723645 </br>
29535123p48723487**597645**723645 </br>
29535123p4872348759**76457**23645</br>
29535123p48723487597**6457236**45 </br>
29535123p487234875976**4572364**5 </br>
29535123p4872348759764**5723645** </br>
</br>
Ni kan välja vilka färger ni skriver ut med så länge man ser skillnad på dem. Ni </br>
byter färg genom att ändra värde på Console.ForegroundColor. </br>

## Addera ihop alla tal och skriv ut totalen
Programmet ska också addera ihop alla tal den hittat enligt ovan och skriva ut det </br>
sist i programmet. Gör gärna en tom rad emellan för att skilja från output ovan. </br>
Exempel output för input ”29535123p48723487597645723645”: </br>
Total = 5836428677242 </br>

## Redovisning
Uppgiften ska lösas individuellt. </br>
Lämna in uppgiften på ithsdistans med en kommentar med github-länken. </br>

## Betygskriterier 
### För godkänt:
* Räcker att lösa en av uppgifterna, d.v.s. antingen skriva ut alla delsträngar som i exemplet ovan, eller räkna ut och skriva ut totalen.
* Om man matar in strängen i exemplet ska man få samma output som ovan.
* Det ska även fungera generellt, oavsett vilken sträng man matar in.
### För väl godkänt krävs även:
* Båda uppgifterna ska vara lösta, d.v.s. programmet ska först skriva ut alla delsträngar som i exemplet ovan och därefter räkna ut och skriva ut total.
* Koden ska vara väl strukturerad och lätt att förstå.
# Inlämning sker före deadline.