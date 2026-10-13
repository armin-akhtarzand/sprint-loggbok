# Loggbok - Armin Akhtarzand

## OBS: Sprint 1-3 är skrivna i efterhand och därför kan reflektioner samt beskriviningar vara begränsade.
## Kommer tillägga (Scrum Master) på de veckor som jag agerar som det.
## Skriver inte några namn i på mina arbetskollegor då de bättre att de själva berättar om deras arbete :D Skriver alltså "kollega" 

---

## Sprint 1(Scrum Master)

### Vad jag arbetade med :

- Jag ansvarade för FE-04, FE-05 FE-08, FE-09, denna vecka samarbetade vi med att undersökning för FE-14. Jag var Scrum Master denna vecka.

- Min del gick sammanfattande ut på att en användare ska kunna logga in via Frontend, hade inga större svårigheter med detta då uppgiften var väldigt "straight forward". Jag själv ansvarade för Auth-service vid mikrotjänst-projektet så jag visste att min reponse DTO redan returnerade all information som var nödvändig. La alltså bara till CORS-konfigurationen i backend, resterande jobb var mestadel i frontend.

- Vi blev allihoppa färdiga med samtliga punkter.

### Eventuella problem och hur jag löste dem:

- Hade inga större svårigheter under denna sprint. Var lite ovan med rollen som Scrum Master tills att jag insåg att rollen inte är dirket krävande.

### Samarbete och agilt arbete

- Svårt att säga exakt hur vi diskuterade under sprint planeringen då de nu har gått ett par veckor, dock kan jag inte minnas att vi hade svårt att dela upp arbetet.

- Vi jobbar otroligt bra som Team. Alla är aktiva när det behövs, även fast man själv kanske inte jobbar/skriver kod så är man aktiv för att kunna Merga eller svara frågor vid behov! Grymt!

- Vi kände inte att vi behövde köra digitala möten varje dag (alltså samtal) då vi konstant håller kontakten via meddelanden.

- Under Repot kom vi fram till att vi borde börja jobba i nya områden varje vecka. Alltså ifall man jobbade med produktsidan vecka 1 så ska man helst inte jobba med samma vecka 2. Så att man får lite variaton samt får testa nya saker.
  Självklart så gott vi kan, ibland får man jobba med samma område 2 gånger och det är okej.

---

## Sprint 2

### Vad jag arbetade med:

- Jag ansvarade för FE-15 och FE-16. Mitt ansvar låg denna vecka hos kundvagnen istället för användar funktioner.

- Gillade verkligen den sprinten, vi valde att gå i en annan riktning än vad vi lärt oss under föreläsningarna. Istället för att kundvagnen skulle placeras direkt i produktsidan så valde vi att köra på en separat sida för kundvagnen.
  Kundvagnen state kunde alltså inte ligga i ProductPage eftersom kundvagnen och produktsidan behövde använda samma data. Jag skapade en custom Hook istället (useCart) som samlar kundvagnen state & funktioner för att lägga till produkter, ändra antal och tömma kundvagnen. App använder därefter hooken och skickar vidare data och funktionerna till sidorna via props.

- I hooken la jag till funktionerna bl.a addToCart, decreaseQuantity, increasQuantity.
  Jag fick lära mig hur man använder sig av custom hooks och detta underlättade även för oss i nästa sprint då vi behövde göra en ProductDetailPage. Vi återanvände alltså logiken där med.

- Skapade CartItemCard samt även CartPage, la till logiken i cartpage som räknade ut summan av varje enskilda produkt samt även totala summan för samtliga produkter i kundvagnen. Ifall kundvagnen är tom så presenteras det tydligt i sidan.

- Vi blev färdiga med samtliga punkter denna vecka. Ingenting låg kvar. Vi började dock inte med prototypen för betalningssystemet denna vecka.

- Med tanke på att jag blev klar på onsdag/torsdag så valde jag att försöka "piffa upp" webbshoppen lite. Skrev lite grundläggande CSS för att få sidan att få lite mer liv. Det var inte något avancerat, de mesta använde jag från taskboarden från Lab2. Vi kommer senare dyka djupare i hur vi vill att webbshoppen ska se ut.

### Eventuella problem och hur jag löste dem.

- Egentligen inga större problem, dock så hade jag först planerat på att placera alla funktioner samt state direkt i App. Jag insåg dock snabbt att det blev för mycket kod samlat i App. Jag gjorde lite research på bästa sätt att flytta ut funktionerna och states från App och hittade custom hook, flyttade över allt dit. App blev mer lättläst och kundvagnslogiken samlades på ett ställe.

### Samarbete och agilt arbete

- Här hade vi det lätt att dela upp arbetet. Vi alla fick 2st tasks var att ansvara över. 1 av oss fick specifikt fokusera på att presentera betalningssystemet för resterande för att underlätta undersökningsprocessen.
Vi kom helt enkelt fram till att det var enklare ifall 1 person tog det ansvaret än att vi alla skulle undersöka samma saker. På torsdagen presenterade vår kollega en pdf med en förslag på betalningssystemet samt vilka steg vi skulle ta för att påbörja prototypen.

- Under Repot kom vi fram till att vi inte kunna hitta förbättringar då vi ansåg att vi verkligen gjorde ett riktigt bra jobb allihoppa, i slutändan kom vi fram till att vi ska "forsätta som vi gör".

---

## Sprint 3(Scrum Master)


### Vad jag arbetade med:

- Jag ansvarade denna vecka för FE-26, FE-28 och FE-29. Denna vecka låg mitt ansvar mestadels på produktsidan men ansvarade även över att felaktig url ska visa en 404-sida.

- Började med att fixa 404-sidan med tanke på att jag behövde vänta tills min kollega skulle lägga till category + imgurl i backend. Gick väldigt snabbt för oss båda, när jag var klar med 404-sidan så var hon klar med backend.
Innan jag fixade sökfunktionen i produktsidan ville jag se så att jag kunde få klart kategori filtret. Detta helt enkelt för att se till så att redan från början ska sökfunktionen gå hand i hand med kategori filtret alltså att ifall man filtrera på en specifik produkt så kan sökfunktionen endast hitta produkter från relevant kategori.

- Vi alla jobbade otroligt intesivt under tisdagen denna vecka, vi var klara med alla punkter redan tisdag/onsdag. Vi tog ett möte och bestämde oss för att påbörja prototypen för betalningssystemet. Eftersom att vi redan hade en plan på hur vi ska gå vidare så var det enkelt att påbörja processen.

- Vi delade upp arbetet i 3 olika områden, frontend, backend och en testade flödet. Jag ansvarade för frontend. Jag kopplade kundvagnens knapp till backend så att användaren sen skickas till stripes betalningssida.
Skapade därefter en "Success" sida och en "Canceled" sida för avbrutna ordrar. I samband med success såg (och backend ger oss statusen PAID) så töms kundvagnen, vid cancel ska varorna vara kvar.

- Vi valde att inte merga något för ens vi var helt säkra att det funkade.


### Eventuella problem och hur jag löste dem.
- Denna vecka stötte jag på problem, inte vid mina ordinarie tasks utan när jag byggde min del utav prototypen.

1. Fel sida vid betalning - Lösning: Backend pekade porten mot 3000, för mig ligger Grafana i port 3000 så det var ett litet roligt problem (blev skickad till Grafana vid betalning). Min kollega bytte snabbt det till port 5173 (rätt port).

2. Betalningsbesked kom inte fram -  Den här satt jag och klurade på längre än jag vill erkänna. Jag märkte att min sandlåda fick information om betalningen (kunde se alla transaktioner i min dashboard) men backend fick inte den informationen och frontend fastnade i "Inväntar betalning" sidan. Lösning: Hade råkat skapa 2st sandlådor i Stripe, så hade använt API nyckeln från ena sandlådan med webhook-nyckeln från den andra. Jag bytte helt enkelt ut webhoop-nyckeln så att den matchade API-nyckelns sandlåda. LÖST!

### Samarbete och agilt arbete
- Man märkte att vår samarbete hade gjort framsteg, vi alla gick på auto-pilot (på ett bra sätt). Vi pratade lite mer i samtal denna vecka (med tanke på att Håkan hade rekommenderat de :P) men helt ärligt kände vi att de inte behövdes jättemycket. Självklart var det ingen nackdel, men det gav ingen specifik fördel heller. Vi var vana med att skriva, kände oss bekväma med det och det fungerar väl med tanke på att vi alla svarar snabbt.
Vi reflekterade lite på att vi förstår innebörden av att ha ett samtal varje dag för att man ska ha den dagliga kontakten, men eftersom att vi redan har det (via meddelanden) och lite mer därtill så kändes det överflödigt..fanns inte mycket att säga än BRA JOBBAT!
- Kan slutligen säga att vi var otroligt nöjda med oss själva, alla fick en klapp på axeln!


---
## Sprint 4


### Vad jag arbetade med:
- NOTE: Denna veckas planeringsmöte var lite jobbigare, det var första gången vi behövde dela upp punkterna i product-backlogen. Samtalet tog 37 minuter (längre än de brukar) vi var osäkra på ifall vi skulle hinna med allt denna vecka för just denna backlog, men vi lovade varandra att det inte är någon press! Vi har inte delat ut ALLA punkter direkt utan valde att köra 2st punkter var till att börja med.
- Jag ska just nu implemnentera GatewayProxyServer (skapade alla forward metoder samt send), nu ska jag implementera produktflödet.




### Eventuella problem och hur jag löste dem.


### Samarbete och agilt arbete

