# Het model {#6CD31B94}

In dit hoofdstuk wordt het model zelf uitgebreid beschreven en toegelicht.<br/>
## Algemeen {#6CD31B96}

Objectgerichte planteksten zijn opgebouwd uit objecten van twee klassen: TekstMetadata en TekstObject. TekstMetadata bevat een aantal algemene kenmerken die van toepassing zijn op de tekst en wordt beschreven in hoofdstuk <a href='#6CD320A3'>5</a>. De tekst zelf bestaat uit TekstObjecten (“de inhoud”).<br/>
Bij een klasse, te beschouwen als een groep van objecten met dezelfde eigenschappen, worden attributen gedefinieerd die de eigenschappen van een object van die klasse kunnen bevatten.

<i>Voorbeeld: een tekstobject heeft altijd een attribuut “titel”. De inhoud van dit attribuut is de titel van het tekstobject, bijvoorbeeld ”Wonen” .</i>

De klasse TekstObject is van toepassing op alle instrumenten en heeft één bijzonder onderdeel: de tekst zelf. Dit attribuut is de eigenlijke inhoud. Binnen dit attribuut bevindt zich de tekst zelf, “de cijfers en letters”, evt. noodzakelijke opmaak zoals tabellen, lijsten, nadruk etc. In <a href='#fig-imropt-model-in-totaliteit'>Figuur 1</a> is het IMROPT model als geheel in een UML diagram weergegeven.<br/>
<figure><img src='media/imropt_model.png' alt='Het IMROPT model wordt weergegeven met de objecten TekstMetadata, TeksObject, TitelInfo en Objecttype.' style='width: 100%;'></img>
<figcaption>IMROPT model in totaliteit</figcaption></figure>

## Klasse TekstObject {#1DB047CE}

De tekst is samengesteld uit één of meerdere TekstObjecten, een stuk tekst met een titel. Alle TekstObjecten kennen dezelfde set van mogelijke attributen. De waarde van een attribuut kan uiteraard verschillend zijn.<br/>
De verhouding tussen de verschillende TekstObjecten komt tot uitdrukking in de attributen niveau, volgnummer, ouderId en objecttype en in de volgorde in het document. Het is verplicht de TekstObjecten in de juiste volgorde in het XML document te plaatsen. Het TekstObject met volgnummer 1 wordt als eerste in het document geplaatst, het TekstObject met het hoogste volgnummer als laatste.<br/>
Label, nummer en titel bepalen samen wat de volledige titel, de kop boven de tekst wordt.

<i>Voorbeeld: Hoofdstuk 2 “Beschrijving bestaande situatie” in de toelichting krijgt als label de waarde “Hoofdstuk”, als nummer de waarde “2” en als naam de waarde “Beschrijving bestaande situatie”. De kop wordt dus “Hoofdstuk 2 Beschrijving bestaande situatie”.</i><br/>
<figure><img src='media/tekstobject.png' alt='Afbeelding in UML van het TekstObject.' style='width: 100%;'></img>
<figcaption>TekstObject</figcaption></figure>

In tabel Klasse TekstObject wordt de klasse TekstObject beschreven, waarbij per attribuut wordt aangegeven. Welke waarde gewenst is, welke dit moet zijn, of het gebruik van het attribuut verplicht is,<br/>
en of het attribuut meerdere keren mag voorkomen. Na de tabel wordt per attribuut een nadere toelichting gegeven over de toepassing ervan.<br/>
<table style='width: 100%;'><caption>Tabel Klasse TekstObject</caption>
<colgroup><col id='col1' style='width: 25%;'
<col id='col2' style='width: 9.997688395746648%;'
<col id='col3' style='width: 65.00231160425335%;'
</colgroup>
<thead valign='top'><tr><th align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: #000000;'>Klasse<br/>
</th>
<th align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: #000000;' colspan='2'>TekstObject<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Definitie<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;' colspan='2'>Zelfstandig leesbaar stuk tekst met een titel, dat begint met een hoofdletter en eindigt met een punt.<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>Herkomst definitie <br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;' colspan='2'>IMROPT<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;' colspan='3'>Attributen<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><i>Attribuutnaam</i><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>m*</b><br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'><b>Toelichting</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>identificatie<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>1<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>eigen identificatie (idn) van het TekstObject. De code moet uniek zijn binnen het plantekstenbestand. De identificatie begint met "NL.IMRO.PT." en wordt gevolgd door max. 32 alfanumerieke tekens.<br/>
De waarde moet voldoen aan de volgende reguliere expressie: NL\.IMRO\.PT\.[A-Za-z0-9_\-,\.]{1,32}<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>verwijzingNaarPlangebied<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>1<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>identificatie (idn) van het IMRO Plangebied waar dit TekstObject bij hoort.<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>volgnummer<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>1<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>een oplopend volgnummer 1, 2, 3, ... dat de volgorde van de tekstobjecten aangeeft.<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>niveau<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>1<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>een oplopende waarde 0, 1, 2, ... dat het hiërarchische niveau van het object aangeeft. Het object met niveau 0 heeft het hoogste niveau. De waarde mag niet hoger zijn dan 11.<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>ouderId<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>1<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>identificatie (idn) van het bovenliggend TekstObject.<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>type<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>1<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>type van het object volgens domein ObjecttypePlan, ObjecttypeVisie of ObjecttypeBesluit <br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>typeTekst<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>0..1<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>aanduiding van het type tekst waarnaar verwezen wordt. Domein: Teksttype.<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>titelInfo<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>1<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>TitelInfo: Een samengesteld attribuut:<br/>
<ul><li>label [0..1]: Soortnaam die getoond moet worden, vaak gelijk aan type. Dit is een vrij tekstveld.</li>
<li>nummer [0..1]: aanduiding van het object. Een opvolgende reeks (1,2,3 of A,B,C) wordt geadviseerd.</li>
<li>naam[0..1]: de zelf gekozen naam van het object.</li>
</ul>

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>interneVerwijzing<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>0..n<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>TekstObject identificatie (idn), koppelt TekstObjecten<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>externeVerwijzing<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>0..n<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>verwijzingen naar een ander bronbestand waar het ruimtelijk instrument is opgebouwd of een specifieke locatie daarbinnen.<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>tekstMetadata<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>0..1<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>verwijzing naar object TekstMetadata. Alleen van toepassing en verplicht indien het type object gelijk is aan ‘document’ of ‘besluitdocument’.<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>tekst<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>0..1<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>de tekst. Wat hier mag worden opgenomen staat beschreven in paragraaf <a href='#6CD31BFC'>2.3</a>.<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;' colspan='3'>* multipliciteit<br/>
1 = komt 1 keer voor<br/>
1..n = komt 1 of meer keer voor<br/>
0..1 = komt hooguit 1 keer voor<br/>
0..n = komt zo vaak voor als gewenst<br/>
</td>
</tr>
</tbody>
</table>

## Speciale tekstonderdelen {#6CD31BFC}

De inhoud van de tekstelementen is “mixed-content”. Dat betekent dat binnen deze klasse verschillende objecten door elkaar heen kunnen voorkomen. De basis word gevormd door een selectie uit XHTML. Deze wordt aangevuld met voor planteksten van belang geachte specifieke onderdelen.

<b>XHTML elementen</b><br/>
De volgende XHTML 1.0 elementen (conform <a href='https://www.w3.org/TR/xhtml1/' target='_blank'>W3C</a>) mogen worden gebruikt. Nadere definitie vindt plaats in het IMROPT2012 XML Schema (XSD) en dit modeldocument.

<table style='width: 304.8pt;'><caption>Tabel XHTML elementen</caption>
<colgroup><col id='col1' style='width: 50%;'
<col id='col2' style='width: 50%;'
</colgroup>
<thead valign='top'><tr><th align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: #000000;'>XHTML element<br/>
</th>
<th align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: #000000;'>betekenis<br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>&lt;!--...--&gt;<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>commentaar<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>&lt;strong&gt;<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>sterke nadruk<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>&lt;em&gt;<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>nadruk<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>&lt;sub&gt;<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>subscript<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>&lt;sup&gt;<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>superscript<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>&lt;ul&gt;<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>ongeordende lijst<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>&lt;ol&gt;<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>geordende lijst<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>&lt;li&gt;<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>item in een lijst<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>&lt;p&gt;<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>paragraaf<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>&lt;br&gt;<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>nieuwe regel<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>&lt;table&gt;<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>tabel<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>&lt;tr&gt;<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>rij in tabel<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>&lt;td&gt;<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>cel in tabel<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>&lt;th&gt;<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>kop in tabel<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>&lt;img&gt;<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #666666; border-left: 0.5pt solid #666666; border-bottom: 0.5pt solid #666666; border-right: 0.5pt solid #666666; background-color: none;'>afbeelding<br/>
</td>
</tr>
</tbody>
</table>

<b>Verwijzing naar afbeeldingen in de tekst</b><br/>
In de tekst attributen mag alleen worden verwezen naar afbeeldingen die deel uitmaken van het instrument en die dus ook in samenhang beschikbaar gesteld worden conform de <a href='https://docs.geostandaarden.nl/ro/stri' target='_blank'>STRI2012</a>. Deze afbeeldingen worden middels een &lt;img&gt; tag in de tekst verwerkt.<br/>
Bij het beschikbaar stellen van objectgerichte planteksten is het mogelijk om gebruik te maken van een separaat Cascading Style Sheet (CSS bestand), waarin de gewenste opmaak van de planteksten is vastgelegd. Dit is vastgelegd in de <a href='https://docs.geostandaarden.nl/ro/stri' target='_blank'>STRI2012</a>. De bepaling dat alleen mag worden verwezen naar afbeeldingen die deel uitmaken van het instrument is niet van toepassing op afbeeldingen waar vanuit het CSS bestand naar wordt verwezen.

<b>Toevoegingen voor opsommingen</b><br/>
Voor de ongeordende lijst &lt;ul&gt; kunnen de volgende “classes” worden gebruikt om specifieke opsommingtekens te gebruiken. Als geen class wordt gebruikt, zal de standaard waarde worden verondersteld conform de volgende tabel:<br/>
<table style='width: 100%;'><caption>Tabel gebruik van classes</caption>
<colgroup><col id='col1' style='width: 21.336610486891384%;'
<col id='col2' style='width: 78.66338951310861%;'
</colgroup>
<thead valign='top'><tr><th align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: #000000;'><b>Class</b><br/>
</th>
<th align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: #000000;'><b>Toelichting</b><br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>disc<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>Een gevulde cirkel. Dit is de standaard waarde van de &lt;ul&gt;<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>circle<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>Een open cirkel<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>square<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>Een vierkant<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>nomarker<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>Er wordt geen opsommingsteken getoond (list-style-type=none)<br/>
</td>
</tr>
</tbody>
</table>

Voor de geordende lijst &lt;ol&gt; kunnen de volgende “classes” worden gebruikt om specifieke opsommingtekens te gebruiken. Als geen class wordt gebruikt, zal de standaard waarde worden verondersteld conform de volgende tabel:<br/>
<table style='width: 100%;'><caption>Tabel gebruik van opsommingen</caption>
<colgroup><col id='col1' style='width: 22.951779026217228%;'
<col id='col2' style='width: 77.04822097378276%;'
</colgroup>
<thead valign='top'><tr><th align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: #000000;'><b>Class</b><br/>
</th>
<th align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: #000000;'><b>Toelichting</b><br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>decimal<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>Een numerieke waarde. Dit is de standaard waarde van de &lt;ol&gt;<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>decimal-leading-zero<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>Een numerieke waarde met voorloopnul (01, 02, 03, etc.)<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>lower-alpha<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>Een kleine letter (onderkast) (a, b, c, d, e, etc.)<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>upper-alpha<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>Een hoofdletter (kapitaal) (A, B, C, D, E, etc.) <br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>lower-roman<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>Een Romeinse numerieke waarde in kleine letter (i, ii, iii, iv, v, etc.)<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>upper-roman<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>Een Romeinse numerieke waarde in hoofdletter (I, II, III, IV, V, etc.)<br/>
</td>
</tr>
</tbody>
</table>

<table style='width: 100%;'><caption>Toegevoegde IMRO-PT elementen</caption>
<colgroup><col id='col1' style='width: 22.955938475771944%;'
<col id='col2' style='width: 77.04406152422806%;'
</colgroup>
<thead valign='top'><tr><th align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: #000000;'><b>XHTML element</b><br/>
</th>
<th align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: #000000;'><b>Betekenis</b><br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>voetnoot<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>voetnoot<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>verwijderd<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>Verwijderde tekst, alleen bedoeld voor het markeren van tekst waarvan vermeld wordt dat deze verwijderd wordt (in geval van herzieningen).<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>toegevoegd<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>Toegevoegde tekst, alleen bedoeld voor het markeren van tekst waarvan vermeld wordt dat deze een toevoeging vormt (in geval van herzieningen)<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>interneVerwijzing<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>TekstObject identificatie (idn), koppelt TekstObjecten<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>externeVerwijzing<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>verwijzingen naar een ander bronbestand waar het ruimtelijk instrument is opgebouwd of een specifieke locatie daarbinnen.<br/>
</td>
</tr>
</tbody>
</table>

<b>Verwijzingen</b><br/>
Een verwijzing verwijst altijd naar een bepaald object in de plantekst. Deze verwijzing moet geïnterpreteerd worden als een verwijzing naar de aangegeven plek in de volledige tekst. In ieder geval moet de onderliggende tekst gemakkelijk bereikbaar zijn.

<i>Voorbeeld: In een bestemmingsplan wordt verwezen worden naar het bestemmingsartikel “Wonen”. Hiermee wordt ook bedoeld de onderliggende leden bestemmingsomschrijving, bouwregels etc.</i>

Verwijzingen worden binnen IMRO geïmplementeerd als XLink href (conform <a href='https://www.w3.org/TR/xlink11/' target='_blank'>W3C</a>). Dit kan een verwijzing binnen het planteksten bronbestand zijn, maar ook een verwijzing naar een ander bronbestand waaruit het instrument is opgebouwd. Binnen de tekst kunnen dezelfde verwijzingstypes worden gebruikt als die mogelijk zijn als attribuut bij het TekstObject, interneVerwijzing en externeVerwijzing.

De opbouw van de href bij een interneVerwijzing is altijd het interne identificatienummer van een TekstObject voorafgegaan door het symbool #, de <i>fragment identifier</i>.

Toelichting: de <i>fragment identifier</i> geeft aan dat binnen een href het volgende fragment een locatie betreft binnen het huidige bestand. Als er geen voorafgaand bestand is gespecificeerd, betreft het dus een locatie binnen het huidige bronbestand. Als de href begint met een # wordt er dus verwezen naar een lokaal object. Dat klopt ook met de bedoeling van de links tussen Tekstobjecten. Als er verwezen wordt naar een extern object, dan begint de href niet met het # maar wordt de fragment identifier facultatief gebruikt om een nadere locatie binnen het externe document aan te duiden.

Hier onder volgen enkele voorbeelden.

<aside class='example'><i>Voorbeeld 1 - Interne verwijzing</i><br/>
Bij een interne verwijzing is de opbouw voor de href een intern identificatienummer van een TekstObject element voorafgegaan door een # teken.

<pre class="text"><span style='color: #0000FF;'>&lt;</span><span style='color: #800000;'>imropt2012:interneVerwijzing</span><span style='color: #FF0000;'> xl:type</span><span style='color: #0000FF;'>="</span><span style='color: #000000;'>simple</span><span style='color: #0000FF;'>"</span><span style='color: #FF0000;'> xl:href</span><span style='color: #0000FF;'>="</span><span style='color: #000000;'>#NL.IMRO.PT.s2</span><span style='color: #0000FF;'>"&gt;</span><span style='color: #000000;'>Hoofdstuk 1 Inleidende bepalingen</span><span style='color: #0000FF;'>&lt;/</span><span style='color: #800000;'>imropt2012:interneVerwijzing</span><span style='color: #0000FF;'>&gt;</span><br/>
</pre>

<i>Voorbeeld 2 - Verwijzing naar een extern bronbestand</i><br/>
De verwijzing naar een bijlage bronbestand wordt als volgt vormgegeven:

<pre class="text"><span style='color: #0000FF;'>&lt;</span><span style='color: #800000;'>imropt2012:externeVerwijzing</span><span style='color: #FF0000;'> xl:type</span><span style='color: #0000FF;'>="</span><span style='color: #000000;'>simple</span><span style='color: #0000FF;'>"</span><span style='color: #FF0000;'> xl:href</span><span style='color: #0000FF;'>="</span><span style='color: #000000;'>b_NL.IMRO.4321.12-0004_bijlage1.pdf</span><span style='color: #0000FF;'>"/&gt;</span><br/>
</pre>

De bestandsnaam in dit voorbeeld is uiteraard fictief. Er dient altijd te worden verwezen naar bronbestanden die onderdeel zijn van het desbetreffende instrument en die dus ook voorkomen in het Geleideformulier, zie <a href='https://docs.geostandaarden.nl/ro/stri' target='_blank'>STRI2012</a>.

<i>Voorbeeld 3 - Externe verwijzing</i><br/>
Met de fragment identifier # kan tevens een verwijzing worden gemaakt naar een bepaalde locatie binnen een extern object. Bij verwijzingen naar PDF bestanden kan op die manier worden verwezen naar een bepaalde pagina binnen het document, bijvoorbeeld:

<pre class="text"><span style='color: #0000FF;'>&lt;</span><span style='color: #800000;'>imropt2012:externeVerwijzing</span><span style='color: #FF0000;'> xl:type</span><span style='color: #0000FF;'>="</span><span style='color: #000000;'>simple</span><span style='color: #0000FF;'>"</span><span style='color: #FF0000;'> 
xl:href</span><span style='color: #0000FF;'>="</span><span style='color: #000000;'>b_NL.IMRO.4321.12-0004_bijlage1.pdf#page=6</span><span style='color: #0000FF;'>"/&gt;</span><br/>
</pre>

bij verwijzingen naar HTML of XHTML bestanden kan er worden verwezen naar specifieke elementen in dit bronbestand, bijvoorbeeld:

<pre class="text"><span style='color: #0000FF;'>&lt;</span><span style='color: #800000;'>imropt2012:externeVerwijzing</span><span style='color: #FF0000;'> xl:type</span><span style='color: #0000FF;'>="</span><span style='color: #000000;'>simple</span><span style='color: #0000FF;'>"</span><span style='color: #FF0000;'> xl:href</span><span style='color: #0000FF;'>="</span><span style='color: #000000;'>b_NL.IMRO.4321.12-0004_bijlage1.html#hoofdstuk6</span><span style='color: #0000FF;'>"/&gt;</span><br/>
</pre>

</aside>

<aside class='example'><b><i>Voorbeeld tekstfragment – niet normatief</i></b>

Meer technisch georiënteerde lezers zullen zich gemakkelijker een beeld kunnen vormen van de werking van het tekst attribuut door onderstaand voorbeeld te bekijken:

<i>Het belangrijkste </i><b><i>doel</i></b><i> van dit voorbeeld is duidelijkheid verschaffen. Een verwijzing naar </i>een bijlage<i> is bijvoorbeeld een apart onderdeel. Net zoals een lijst met</i><br/>
</aside>

<ol><li><i>punt 1</i></li>
<li><i>punt 2</i></li>
<li><i>punt 3</i></li>
</ol>

<aside class='example'>In bovenstaand voorbeeld wordt de inhoud van <span style='color: #0000FF;'><span style='background-color: white;'>&lt;</span></span><span style='color: #800000;'><span style='background-color: white;'>tekst</span></span><span style='color: #0000FF;'><span style='background-color: white;'>&gt;</span></span> gevormd door<br/>
</aside>

<ul><li>een aantal alfanumerieke tekens (de eigenlijke tekst);</li>
<li>een codering die aangeeft dat “doel” sterke nadruk (strong) moet krijgen;</li>
<li>een codering die van de frase “een bijlage” een verwijzing maakt;</li>
<li>een lijst met 3 items, aangegeven met alfanumerieke tekens.</li>
</ul>

<aside class='example'>In XML code zal dit er als volgt uitzien:

<pre class="text"><span style='color: #0000FF;'>&lt;</span><span style='color: #800000;'>tekst</span><span style='color: #0000FF;'>&gt;
    &lt;</span><span style='color: #800000;'>p</span><span style='color: #0000FF;'>&gt;</span>Het belangrijkste <span style='color: #0000FF;'>&lt;</span><span style='color: #800000;'>strong</span><span style='color: #0000FF;'>&gt;</span>doel<span style='color: #0000FF;'>&lt;/</span><span style='color: #800000;'>strong</span><span style='color: #0000FF;'>&gt;</span>van dit voorbeeld is duidelijkheid verschaffen. Een verwijzing naar <span style='color: #0000FF;'>&lt;</span><span style='color: #800000;'>imropt2012:externeVerwijzing</span><span style='color: #FF0000;'> xl:type</span><span style='color: #0000FF;'>="</span><span style='color: #000000;'>simple</span><span style='color: #0000FF;'>"</span><span style='color: #FF0000;'> xl:href</span><span style='color: #0000FF;'>="</span><span style='color: #000000;'>b_NL.IMRO.4321.12-0004_bijlage1.pdf</span> "<span style='color: #0000FF;'>&gt;</span>een bijlage<span style='color: #0000FF;'>&lt;/</span><span style='color: #800000;'>imropt2012:externeVerwijzing</span>&gt; is bijvoorbeeld een apart onderdeel. Net zoals een lijst met<span style='color: #0000FF;'>&lt;/</span><span style='color: #800000;'>p</span><span style='color: #0000FF;'>&gt;
    &lt;</span><span style='color: #800000;'>ol class</span><span style='color: #0000FF;'>="</span>lower-alpha<span style='color: #0000FF;'>"&gt;
        &lt;</span><span style='color: #800000;'>li</span>&gt;punt 1<span style='color: #0000FF;'>&lt;/</span><span style='color: #800000;'>li</span><span style='color: #0000FF;'>&gt;
        &lt;</span><span style='color: #800000;'>li</span>&gt;punt 2<span style='color: #0000FF;'>&lt;/</span><span style='color: #800000;'>li</span><span style='color: #0000FF;'>&gt;</span>
<span style='color: #0000FF;'>        &lt;</span><span style='color: #800000;'>li</span>&gt;punt 3<span style='color: #0000FF;'>&lt;/</span><span style='color: #800000;'>li</span><span style='color: #0000FF;'>&gt;</span>
<span style='color: #0000FF;'>    &lt;/</span><span style='color: #800000;'>ol</span><span style='color: #0000FF;'>&gt;
&lt;/</span><span style='color: #800000;'>tekst</span><span style='color: #0000FF;'>&gt;</span><br/>
</pre>

</aside>

