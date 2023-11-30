---
Title: Load
Description: A page analysing load and utility.
Template: analysis
---

Laddningstid och användbarhet
=======================

Denna uppgiften gick ut på att man skulle välja tre hemsidor och testa dem för att mäta hur snabbt de laddas och om de innehåller några saker som kan förbättras med tanke på ladddningstid och användbarhet. 


Urval
-----------------------

Precis som med urvalet inför färg-analysen utgår jag från sidor jag kan använda under kursens alla moment, så jag håller kvar de tre sidor jag analyserade då. Jag tänker att de också har väldigt olika laddningstid, med tanke på den stora skillnaden i antal element, bilder, videor m.m. så det blir en spännande och relevant jämförelse. 

Här är länkar till sidorna:  
https://www.taylorswift.com/  
https://phoebefuckingbridgers.com/  
https://soccermommyband.com/home/


Metod
-----------------------

Som mätverktyg använde jag [PageSpeed Insights](https://pagespeed.web.dev/), eftersom det rekommenderas. Datan sparade jag sedermera ner i ett Google Kalkylark, som jag sedan presenterade här på sidan.

Resultat
-----------------------

### Data:  
<iframe class="data-iframe" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vTQx6XNi27wsNcmrMgw5kYXrprCtXCDYYZzOKyl1dRDIBVXXnEe8vaB8hHLS0-0ZX3YbD3EH5kdR2gb/pubhtml?gid=0&amp;single=true&amp;widget=true&amp;headers=false"></iframe>

### Taylor Swift: 
 

<a href="%assets_url%/img/taylor.png"><img src="%assets_url%/img/taylor.png" alt="https://www.taylorswift.com/" class="analysis-img"></a>

## https://www.taylorswift.com/
Som ni kan se så är Taylor Swifts hemsida inte särskilt snabb. Den klockar in på 20,61 sekunder och är med det dubbelt så långsam som den nästa långsammaste sidan, trots att den egentligen är mindre. Man kan också se på prestandabetyget för mobil att den inte är välfungerande. Enligt PageSpeed Insights så är ett stort problem att sidan laddar in för stora bilder, med en möjlig besparing på 2114,4KiB. Med modernare bildformat kan 1760,8KiB sparas. Att ta bort JavaScript som inte används skulle också göra sidan snabbare. Sidan har också en autostartande youtube-video som gör att mycket data laddas in.  
Läs mer [här](https://pagespeed.web.dev/analysis/https-www-taylorswift-com/ehdqxfrr1m?form_factor=desktop).  

## https://storeuk.taylorswift.com/
Precis som på huvudsidan är det stora bilder som tynger ner denna sidan, det finns dessutom JavaScript som inte används som begränsar prestandan.

## https://tstheerastour.taylorswift.com/
Bilder fortsätter vara det stora problemet med Taylor Swifts sidor. På denna sidan är ett stort problem att bilderna inte läses in i förväg, eftersom det största elementet beror på bilden.


### Phoebe Bridgers: 


<a href="%assets_url%/img/phoebe.png"><img src="%assets_url%/img/phoebe.png" alt="https://www.phoebefuckingbridgers.com/" class="analysis-img"></a>


## https://phoebefuckingbridgers.com/
Phoebe Bridgers hemsida är den snabbaste av de tre jag testat. Inte särskilt förvånande, då det är väldigt få objekt på sidan, och bara en liten bild i mitten. Det är dock förvånande att den trots det inte har högre poäng på prestandatesterna. Enligt PageSpeed Insights beror det på att sidan har JavaScript som inte används och en widget, som används för att anmäla sig till nyhetsbrevet, blockerar renderingen och borde skjutas upp till senare.  
Läs den fullständiga analysen [här](https://pagespeed.web.dev/analysis/https-phoebefuckingbridgers-com/pjq1d6q011?form_factor=desktop)

## https://phoebefuckingbridgers.com/shop
Precis som huvudsidan är det en nyhetsbrevswidget som ställer till det här, vad gäller desktopsprestanda. För mobil är det onödig JavaScript som drar ner sidans hastighet, vilket drar ner hastigheten med 1,42 sekunder. Nyhetsbrevswidgeten är inte ens synlig på den här sidan, så det är absolut en rimlig lösning att ta bort den för undersidorna.


## https://phoebefuckingbridgers.com/contact
Samma sak som för /shop, JavaScript som exekveras, men inte används, främst för nyhetsbrevswidgeten som inte används på denna undersidan. 


### Soccer Mommy: 


<a href="%assets_url%/img/soccermommy.png"><img src="%assets_url%/img/soccermommy.png" alt="https://soccermommyband.com/home/" class="analysis-img"></a>

## https://soccermommyband.com/home/
Soccer Mommys hemsida fick medelmåttiga betyg på PageSpeed Insights och hade en laddningstid på 10,72 sekunder i snitt. Det största prestandatappet för denna sidan är JavaScript som inte används, som kommer från WordPress-pluginmoduler. Den största delen av den onödiga koden som körs är från YouTube. Detta påverkar prestandan oerhört mycket, med 44,58 sekunder på mobil. Det andra som kan göras är att använda bilder i rätt storlek och i modernare format.  
Läs mer [här](https://pagespeed.web.dev/analysis/https-soccermommyband-com-home/kq2lx3ms6i?form_factor=desktop)

## https://soccermommyband.com/
Den här sidans stora problem är att en stor GIF står för mycket av innehållet. Prestandan skulle kunna förbättras med en konvertering till ett modernt videoformat.

## https://soccermommyband.com/map/
Samma sak som startsidan "https://soccermommyband.com/", GIF-animationer som skulle kunna göras effektivare med modernare videoformat. Ett annat problem här är att bilderna är för stora.

Analys
-----------------------

Det var väldigt varierande tid de tre sidorna laddades in med. Det är anmärkningsvärt att en av världens största artister inte har en mer välfungerande hemsida. Det verkar som att dåligt implementerad JavaScript och bilder som inte är optimerade för rätt storlek är de vanligaste orsakerna till prestandaproblem.

#### Rangordning: 

1. https://phoebefuckingbridgers.com/  
2. https://soccermommyband.com/home/
3. https://www.taylorswift.com/

Phoebe Bridgers hemsida står som klar vinnare, om än lite oförtjänt eftersom den är i princip tom.

För mig är en laddningstid på under tio sekunder absolut acceptabelt. När en sida börjar gå över där så blir det en sämre upplevelse. När jag testar att surfa vanligt, utan mätverktyg upplever jag inte Taylor Swifts sida som särskilt långsam, vilket jag antar är för att det som laddas in är bilder som kommer när man scrollar ner. Soccer Mommys sida upplevs däremot som mer krävande för datorn, och den känns till och med lite oresponsiv till en början. Phoebe Bridgers laddar snabbt och det tar inte heller så lång tid att ta i det sparsamma innehållet.

Referenser
-----------------------

[PageSpeed Insights](https://pagespeed.web.dev/)

Övrigt
-----------------------

Den som har författat den här rapporten är jag, Vilhelm Malmberg Eskilsson.
