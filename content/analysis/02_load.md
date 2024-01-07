---
Title: Load
Description: This is our load page.
Template: analysis
---

Laddningstid
=======================

I denna uppgift ska jag analyser och rapportera mina resultat gällande laddningstid för tre olika webbsidor. Jag kommer fokusera på bilder och hur stort antal bilder som används samt kvaliten på bilderna.

Urval
-----------------------

Jag har valt att analysera tre hemsidor som jag tidigare har analyserat färgetma och typografi. Anledningen till detta är att jag vill få djupare förståelse av hur dessa hemsidors webbprogrammerare har tänkt utifrån design i balans med laddningstid.

Hemsidorna är: Blocket, Coop och Prisjakt.


Metod
-----------------------


För att utföra analysen kommer jag att använda mig av några olika verktyg. Google lighhouse kommer jag att använda för att få en helhets bild över hur hemisdan byggts upp och vad som eventuelt kan behövas förbättras. Jag kommer även att använda mig av "network" funktionen i "devtools", detta verktyg hjälper mig att få data om hur lång tid det tar att ladda hemsidan genom olika internet hastigheter. Verktyget ger mig även en inblick i hur hemsidorna implementerar sina bilder.

Resultat
-----------------------

De tre sidornas resultat kan ses i slutet av denna text i form av ett google sheet.

<img src="%assets_url%/img/prisjakt1.png" alt="prisjakt" width="40%">


<a href="https://www.prisjakt.nu/">Länk till Prisjakt</a>



Resultatet som kan konstateras för prisjakt är att det finns några områden där hemsidan kan optimeras.

 Vid analysen med network "funktionen" i devtools kan jag konstatera att hemsidan använder sig av 255 requests med 8.1mb, där de två största resurserna är en javascript-fil (273kb) respektive en en jpeg-fil (217kb). Vi kan även se att hemsidans laddningstid varierar stort beroende på internet hastighet. Laddningstiderna finns i google sheets nedan.

I Google lighthouse jämför vi "desktop" och "mobile". Där kan vi se att "performance" score varierar kraftigt beroende på enhet. Desktop får ett score på 80 och mobile 33.
När det kommer till "best practices" och "SEO" syns ingen skilldnad mellan mobile och desktop.

<img src="%assets_url%/img/coop.png" alt="coop" width="40%">


<a href="https://www.coop.se/">Länk till Coop</a>

Resultaten från Copps hemsida är följande, laddningtiden är 3.3 sekunder med 7.2mb resources. Där de två största resurserna är en mp4-fil (446kb) samt en javascript-fil (246kb). Med hjälp av Google lighthouse kan vi konstatera att hemsidans performance följer det vi kom fram till på prisjaks hemsida. Vid test av desktop får hemsidan ett score på 91 och mobile får ett score på 39. Denna minsking i score konstaterar att även denna sida har en stor använding av javascript, vilket gör att sämre processorer får en högre laddningstid. När det kommer till "best practices finns det möjlighet för förbättring, sidan kanske körs på äldre verisioner av api:er.

<img src="%assets_url%/img/blocket.png" alt="blocket" width="40%">


<a href="https://www.blocket.se/">Länk till Blocket</a>

Blockets laddningstid är 4.6 sekunder med 8.3mb, de två största requestsen är javascript filer, (339kb) samt (248mb). Vid analys av laddningstid följer även denna hemsida mönstret att drastiskt öka laddningstid beroende på internethastighet. Fast 3g får laddningstid på 34.9 sekunder, slow 3g har laddningstid på 57 skeunder.

<div>
    <iframe title="google-sheet" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vT03dH04z5V9FJ8Rrjcz17bL_MgzZsxQLZkoe_xKKJjcV9C5o5xfejuD-5VR9Fw2ppKhFzIj_SStR8Y/pubhtml?widget=true&amp;headers=false" width="90%" height="530px"></iframe>
</div>




Analys
-----------------------

Till och börja med så kan vi kolla på "network" funktionen i devtools. Där kan vi se att prisjakt har en laddnings tid på 9,2 sekunder. Detta är en rätt hög laddningstid i jämförelse med Coop och Blocket. Vi kan även se att laddningstiden ökar markant under "fast 3g" samt "slow 3g" vilket gäller för samtliga hemsidor. Detta kan bero på använding av höguplösta bilder och krävande javascript filer. Hemsidorna har potential att optimera detta cimage och 

Med hjälp av "google-lighthouse" kan jag konstatera att samtilga hemsidors laddningstid tyngs ned kraftigt pågrund av javascript. Scripten är en väsentlig del av sidan som kan vara svår att optimisera men under analysen fann jag att samtliga hemsidor blev flaggade med "unused javascipt" och "duplicate modules". Med effektiv kod skulle hemsidorna säkert kunna förbättras och göra laddningstider snabbara både för desktop användare och mobil användare.

Enligt min analys får webbsidorna följande rangordning. Prisjakt på 3:e plats, Coop 2:e plats och Blocket på första plats. Anledningen är att prisjakt har valt design före optimisireing. Hemsidan har en annons som täcker bakgrunden vilket tar en stor del av hemsidns storlek. Coop fick andra plats då laddningstiden för slow och fast 3g markant försämrades, samt att google lights tester visade sämre score. Blocket får första plats då hemsidan är väl optimiserad mellan desktop och mobile. Mobil användare är en stor del av trafiken på nätet och jag anser därför att Blocket förtjänar första plats.

När det kommer till en absolut laddningstid anser jag att allt under 5 sekunder är en snabb laddningstid. Både Coop och Blocket klarar denna gräns och ger en responsivt intryck. Prisjakt har en laddningstid på 9.2 sekunder vilket beror på bakgrundsbilden. Bilden laddas in några sekunder efter övriga hemsidan laddats in vilket ger ett dåligt intryck. 


Referenser
-----------------------

Google lighthouse
Devtools Network funktion

Övrigt
-----------------------

Mattis Kvant