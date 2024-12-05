---
Title: Kursmoment 5 - analys av laddningstid
Description: Rapport för kursmoment 5
Template: reportpage
---

Kursmoment 5, laddningstid
===============

Uppgiften var att välja ut 3 webbsidor och analysera deras laddningstid.

Urval
-----------
Jag har valt att utgå från samma sidor som jag analyserade i kursmoment 4, men eftersom det bara ska vara 3 nu så tog jag bort västtrafik. De sidorna som återstår då är:
* [UL](https://ul.se)
* [SL](https://sl.se)
* [Värmlandstrafik](https://varmlandstrafik.se)

Metod
---------
För att göra analysen har jag använt mig av:
- pagespeed insights
- devtools, nätverk

Resultat
----------

<iframe class="load-table" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vSrlg-KaPW187zoANuhM6kM3Yn_MndsUQKzcXoRVu4BKjlfLG6RrvQBBo9iwYo4hA_ELdgjjTpTx-rV/pubhtml?widget=true&amp;headers=false"></iframe>

![UL](%base_url%/image/UL1.png?w=40%)
#### UL

Mobil prestanda (rött)
- Minska tiden det tar att tolka och kompilera JS, ta bort javascript som inte används.
- minska påverkan från tredjepartskod
- Textkomprimering
- minska CSS som inte används
- optimera hur bilder laddas


![SL](%base_url%/image/SL1.png?w=40%)
#### SL

Mobil prestanda (rött)
- minska körningstiden för javascript, reducera javascript som inte används
- optimera bilder, modernare filformat
- reducera css som inte används


![Värmlandstrafik](%base_url%/image/Varmlandstrafik1.png?w=40%)
#### Värmlandstrafik

Mobil prestanda (rött)
- minska körningstid för javascript, minska det som inte används
- aktivera textkomprimering
- bilder i modernare format, rätt storlek
- minifiera css
- LCP, element som största uppritningen av innehåll gjordes för

Analys
-----------
Det verkar vara prestanda på mobilsidan som var svårast om man kollar till alla sidorna. Det var det enda som var rött enligt page speed, gult blev ibland även sökmotoroptimering (SEO) men betyligt högre poäng än prestanda för mobilen. Det som återfanns som tips/saker att förbättra när det kommer till prestanda i mobilen:
- att optimera bilder, "rätt" storlek, modernare bildformat (t.ex. webp eller avif)
- kod som inte används, framför allt javascript som det ofta fanns många punkter om. Men även CSS. 
- LCP (largest contentful paint).

Generellt så verkar det, enligt min analys, som att det är svårt att anpassa ordentligt efter mobilen på alla fronter. Kanske lägger vi fortfarande mest resurser på att utevckla webbsidor för dator, trots att mobilanvändandet har ökat så markant senaste åren. När det kom till SEO så handlade det i princip alltid om länkar, antingen att länkarna inte var sökbara eller inte hade beskrivande text. För en olärd så låter det ju som små saker att fixa, men det kanske innebär mer arbete än vad man tror. 

Tittar man på datan från devtools så kan man se att SL i snitt hade kortast laddningstid (661ms) men kollar man snabbast till enskilt sida så vann värmlandstrafiks sida för kundservice (472ms). 

Jag sammanställde alla poäng från page speed, och fick då följande siffror.

SL = 2001

UL = 1989

VT = 1950

Siffrorna skiljer sig inte särskilt mycket åt, men SL fick högst. Hemsidorna tycks prestera hyfsat lika enligt mina analyser men ska vi ändå utse en vinnare så blir det SL som hade både högst poäng från page speed och bästa snitt när det kom till laddningstid. Man kan också se att alla 3 sidor som är mätta på sl håller en mindre storlek för hemsidan, vilket såklart hjälper. Kanske är det så att webbsidan för kollektivtrafik i vårt lands största stad också har mest resurser att bygga den bäst presterande webbsidan. 

#### Gränsvärde för en "snabb" webbsida
Jag har valt att sätta min gräns vid 1 sekund. Idag när jag gör mätningarna (mätningarna i tabellen gjordes igår) så hamnar laddningstiden för hemsidorna mellan 800ms och 1,5 sekund. Jag tycker att det känns som att när tiden börjar närma sig det spannet så hinner man tänka på att sidan laddas. Är det snabbare så är det nästan som att sidan bara "poppar" upp. Värmlandstrafik tycks vara mest morgonpigg idag när jag har testat på morgonen, som höll sig under 1 sekund precis på ca 900 ms. SL och UL hamnade båda idag runt 1,3-1,5. Jag skulle dock fortfarande säga att ingen av hemsidorna upplevs som långsam, bara inte lika snabb. 

Övrigt
-----------
Rapport och analys gjord av Hanna Arvidsson, haav23. 
