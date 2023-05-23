# Web Typography, 2022/2023
### Beschrijving vak
Als je doof bent, of als je om een andere reden geen geluid kunt horen, dan mis je veel informatie als je een film kijkt. Knisperende voetstappen, langzaam aanzwellende muziek, nerveus getik op een deur, je hoort het natuurlijk allemaal niet. Nu bestaat er zoiets als *closed caption*, wat een type ondertiteling is waarbij ook dingen als omgevingsgeluiden en de muziek beschreven worden. Hierdoor krijgt een kijker die informatie wel binnen.

Alleen wordt die auditieve informatie nogal neutraal beschreven. Het geluid van huilend persoon zou bijvoorbeeld beschreven kunnen worden als *snikgeluid op de achtergrond*. En iemand die lacht zou geschreven kunnen worden als *iemand lacht.* Heel neutraal, bijna zakelijk, en bovendien allebei in precies hetzelfde neutrale lettertype. Terwijl het toch echt over twee heel verschillende emoties gaat. 

Dat kan visueel sterker. 

En dat gaan jullie doen.

## Voortgang
### Eerste ideeën
Ik heb opgelet naar hoe ik me voel tijdens het bekijken van het fragment. Dit wilde ik graag repliceren in het ontwerp.

Eerste ideeën:

- Het geluid van de 'sirene' zou rood en blauw zijn zoals op een politie auto 
- De andere geluiden in het begin zijn best hard dus misschien iets met rode kleuren doen?
- Op het einde is er een piepgeluid die steeds harder en irritanter wordt - deze merk je pas later op. De film is ook donker dus hoe luider het piepgeluid wordt wil ik een witte achtergrond gebruiken die steeds feller wordt om het geluid uit te beelden. Dit lijkt me vrij irritant om te zien in een bioscoop bijvoorbeeld.
- Naast de witte achtergrond wil ik misschien iets doen met het beeld? Dat het trilt of kleiner wordt misschien zodat je je een beetje gespannen voelt


### Voortgang

#### Wit Piepgeluid
De ideeën hierboven heb ik toegevoegd en had tot daaraan geen screenshots en zo gemaakt, omdat ik het was vergeten. Maar voor een lange tijd heb ik geworsteld met hoe ik het witte steeds groter kon krijgen op het einde met een knipperend effect. 

Ik heb met een `::before` een cirkel toegevoegd en daarmee het witte geïmiteerd. 
Maar op de een of andere manier pakte hij de styling van een cirkel van de scanner geluiden. En ging van rechtsonder naar het midden animeren.

<img src=".images/weirdcircle.gif" width="800px" alt="raar cirkel gebeuren">



Na die struggle heb ik gekeken of ik het witte dat steeds groter werd intenser kon maken. Ik wilde dat hij langzaam steeds groter werd en op het einde lichtelijk een flickering effect zou krijgen. Hieronder zie je een aantal experimenten ermee.

<img src="./images/whitercode1.png" width="500px" alt="code voor het witte stuk met keyframes">
<img src="./images/whitercode2.png" width="500px" alt="code voor het witte stuk met keyframes 2">

Met de code hierboven wilde ik het knipperende vormgeven maar uiteindelijk lukte het dus niet en heb het weggehaald.

Wel lukte het witte nu wel - met het groter maken.
In de afbeeldingen was ik nog bezig met het veranderen van de tekstkleur op de juiste momenten.

<img src="./images/sswhite.png" width="500px" alt="hoe het eruit zag">
<img src="./images/sswhite1.png" width="500px" alt="hoe het eruit zag met zwarte tekst">
<img src="./images/sswhite2.png" width="500px" alt="grotere witte cirkel">

Uiteindelijk heb ik het zo opgelost:

<img src="./images/whiterlast.png" width="500px" alt="stuk code van oplossing wit">


#### Chattering
In een deel van het fragment hoor je mensen praten op de achtergrond. Ik wilde hiermee ook iets doen. 
Als eerst dacht ik eraan om het met code te doen maar ik wist niet hoe dus heb het toen met Adobe After Effects gedaan toen ik hoorde dat dit mocht.

Ik heb toen in AE het woord 'chatter' een aantal keer ingetypt en dit verschillende styling gegeven (groot, klein, uitgerekt, platgedrukt, condensed etc.) en sommige toen laten bewegen en andere verdwijnen en verschijnen. Uitendelijk zag het er zo uit:

<img src="./images/chatterss.png" width="500px" alt="chatter v1">
<img src="./images/chatterv1.gif" width="800px" alt="chatter versie 1">

Het zag er uiteindelijk iets te komisch/cartoon-achtig uit en had ook deze feedback gekregen van een vriend dus heb dit toen veranderd naar audio lijnen. Dit heb ik ook in Adobe After Effects gemaakt. Ik heb [deze tutorial](https://youtu.be/Xd-CMLPO7Q4) gevolgd.

<img src="./images/soundwavesss.png" width="800px" alt="chatter v2">
<img src="./images/soundwavesinfragment.png" width="800px" alt="chatter v2 in fragment">


#### Background Music
Ik wilde ook iets doen met de 'background music' die in het begin afspeelt. Nu heb ik heel subtiel een boxshadow toegevoegd aan de body die soort van ademt. Die wilde ik eigenlijk wat intenser hebben.
Ik heb geprobeerd om ook een box-shadow op het fragment te plaatsen, maar deze was er tot aan het eind en ik wist niet zo goed hoe ik hem er weer eraf moest halen, dus heb ik het er maar gelaten. Ook omdat ik het toch niet zo mooi vond en het niet het effect gaf die ik wilde.

<img src="./images/boxshadow.png" width="500px" alt="box-shadow code">

Ik heb de shadow op de body toch behouden omdat het toch een beetje het effect gaf die ik wilde laten zien. 
De schaduwen in de hoek van het scherm zouden het effect moeten geven dat er iets boven hem opdoemt en dat er elk moment iets ergs kan gebeuren. Zijn interne conflict/gevaar volgt hem.


#### Nauwer/Kleiner scherm
Om de opbouw van de spanning bij de baseline test te vergroten heb ik ervoor gekozen om het fragment steeds kleiner te maken. Het is best subtiel. Wanneer het weer terug naar het originele formaat springt, merk je hoeveel het scherm was gekrompen. Je voelt dat je weer soort van normaal kunt ademen nadat het stukje is afgelopen.

`.sound9 iframe { animation: framesmaller 43s linear forwards; }`

`
@keyframes framesmaller {
	0% {
		width: 80vw;
		height: 53.33333333vw;
		margin-top: -0.35vw;
	}

	99% {
		width: 60vw;
		height: 53.33333333vw;
		margin-top: -0.35vw;
	}

	100% {
		width: 80vw;
		height: 53.33333333vw;
		margin-top: -0.35vw;
	}
}
`




## Oplevering
Het was voor mij best moeilijk om het 'extreem' vorm te geven, omdat het zo'n langzame, mysterieuze en dramatische film was wilde ik dit ook zo behouden. 