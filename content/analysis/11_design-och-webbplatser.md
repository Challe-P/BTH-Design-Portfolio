---
Title: Project load analysis
Description: A page analysing the load of the project site.
Template: analysis
---


Laddningstid och användbarhet - Egen sida
=======================

Denna uppgiften gick ut på att man skulle välja ett av de tre tidigare testerna och köra det på sin egen projektsida. Jag valde att testa min sidas ladddningstid och användbarhet, och se vad som skulle kunna göras för att förbättra sidan med hänsyn till de aspekterna. 


Urval
-----------------------

Eftersom uppgiften är att analysera sin egen projektsida så begränsas urvalet något. Jag valde dock att testa alla undersidor för att få lite mer att analysera.


Metod
-----------------------

Som mätverktyg använde jag [PageSpeed Insights](https://pagespeed.web.dev/), eftersom det rekommenderas. Datan sparade jag sedermera ner i ett Google Kalkylark, som jag sedan presenterade här på sidan. Jag använde också nätverskfliken i utvecklarverktygen i Google Chrome för att mäta laddningstid, antal resurser och storleken på de hämtade resurserna.

Resultat
-----------------------

### Data:  
<iframe class="data-iframe" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vRisqZTFjX55xLiCflJq8U8u3eLG25nS933XEe7eu5tM8UH1wZT0_Dh1jtOnvIWNQFMle9FxSbEceuV/pubhtml?gid=0&amp;single=true&amp;widget=true&amp;headers=false"></iframe>
  

<a href="https://www.student.bth.se/~vima23/dbwebb-kurser/design/me/kmom10/" target=_blank><img src="../image/project-screen.png" alt="Min projekt-sida" class="analysis-img"></a>

#### https://www.student.bth.se/~vima23/dbwebb-kurser/design/me/kmom10/

Som man kan utläsa av testerna är min projektsida ganska snabb. Alla sidor klockar in under sekunden och det sammanlagda snittet är på 660ms. Prestandan för desktop är också generellt hög med ett betyg kring 95 för samtliga sidor. Det som sticker ut i mätningen är prestandan för mobiler. Snittbetyget där är 88, som förvisso inte är dåligt, men det kan förbättras. 

Vill man se hela PageSpeed Insights analys kan man läsa mer [här](https://pagespeed.web.dev/analysis/https-www-student-bth-se-~vima23-dbwebb-kurser-design-me-kmom10/why8pz6kaz?form_factor=desktop).  

Analys
-----------------------

Min sida får generellt höga betyg. Antalet resurser är få och deras totala storlek är litet, vilket delvis förklarar sidans snabba laddningstid och prestanda. Problemet är mobilversionens prestanda.Enligt PageSpeed Insights så blockerar CSSen renderingen, eftersom hela sidans CSS läses in samtidigt. Lösningen för att göra sidan snabbare är då att placera den del av sidans som syns försts CSS i en egen fil och ladda in den först och låta resten ladda in senare, något som säkert är en rimlig idé, men som i detta skede skulle ta för lång tid att implementera. Andra saker som dyker upp i analyserna är att förminska hero-bilden, vilket är helt rimligt. Jag implementerade detta genom att sätta en max-bredd samt klippa bort de delar av bilden som ändå inte syns. Tyvärr blev det ingen förbättring på prestandabetyget, men sidan sparar ändå in på en eventuell mobilanvändares surt förvärvade datamängd. 

#### Rangordning: 

1. https://www.student.bth.se/~vima23/dbwebb-kurser/design/me/kmom10/  
2. https://www.student.bth.se/~vima23/dbwebb-kurser/design/me/kmom10/gallery 
3. https://www.student.bth.se/~vima23/dbwebb-kurser/design/me/kmom10/about 
4. https://www.student.bth.se/~vima23/dbwebb-kurser/design/me/kmom10/highlights 

Sidorna ligger väldigt nära varandra, och det är inte så konstigt eftersom de är på samma sida, men hemsidan och galleriet fick lite högre prestandabetyg så de fick hamna överst på prispallen. Min gräns på tio sekunder för en sida att ladda in som jag nämnt i tidigare analys har jag inga problem att komma under. Sidan är snabb och snärtig, och eventuella användare hoppas jag uppskattar hastigheten.

Referenser
-----------------------

[PageSpeed Insights](https://pagespeed.web.dev/)

Övrigt
-----------------------

Den som har författat den här rapporten är jag, Vilhelm Malmberg Eskilsson.
