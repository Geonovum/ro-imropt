# OCL Model constraints {#6CD32058}

De in dit hoofdstuk opgenomen constraints horen bij het conceptuele niveau van het UML-klassediagram. Voor toepassing op het implementatie niveau van GML (XML) moeten ze vertaald worden naar Schematron.

De constraints worden toegepast op objectklassen in het UML diagram van IMROPT2012. De constraints zijn hierdoor onderdeel van IMROPT2012. De overervingsregels uit de objectoriëntatie zijn van toepassing op constraints.

De constraints zijn uitgewerkt bij de objectklasse waarop ze van toepassing zijn. Elke constraintregel wordt eerst in woorden beschreven en daarna in OCL (versie 2.0).<br/>
<table style='width: 100%;'><caption>Tabel OCL constraints voor tekstobjecten</caption>
<colgroup><col id='col1' style='width: 6.014868213561613%;'
<col id='col2' style='width: 93.98513178643839%;'
</colgroup>
<thead valign='top'><tr><th align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: #000000;' colspan='2'><b>TekstObject</b><br/>
</th>
</tr>
</thead>
<tbody valign='top'><tr><td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>T1<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'><b>Alleen bij objecttype ‘document’ en ‘besluitdocument’ is er een verwijzing (verplicht) naar TekstMetadata.</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'><code>Context: IMROPT2012::TekstObject<br/>
Inv VerwijzingNaarMetadata:<br/>
if not (self.type = ObjecttypePlan:: document or<br/>
self.type = ObjecttypeVisie:: document or<br/>
self.type = ObjecttypeBesluit:: besluitdocument) then<br/>
 <br/>
self.tekstMetadata-&gt;isEmpty()<br/>
 <br/>
else<br/>
 <br/>
self.tekstMetadata-&gt;notEmpty()<br/>
</code>

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>T2<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'><b>Relatie tussen toegestane objecttypen (attribuut ‘type’) en plantype (‘typePlan’).</b><br/>
<b>Plannen:</b> bestemmingsplan, beheersverordening, inpassingsplan, rijksbestemmingsplan, wijzigingsplan en uitwerkingsplan<br/>
<b>Visies:</b> structuurvisie<br/>
<b>Besluiten:</b> provinciale verordening, amvb, regeling, aanwijzingsbesluit, beheersverordening, exploitatieplan, gerechtelijke uitspraak, omgevingsvergunning, reactieve aanwijzing, voorbereidingsbesluit<br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'><code>Context: IMROPT2012::TekstObject<br/>
Inv ObjecttypePerPlantype:<br/>
def: PlanLijst : set = Set{'bestemmingsplan','beheersverordening','inpassingsplan','rijksbestemmingsplan','wijzigingsplan','uitwerkingsplan'}<br/>
def: VisieLijst : set = Set{'structuurvisie'}<br/>
def: BesluitLijst : set = Set{'provinciale verordening','amvb','regeling,aanwijzingsbesluit', 'beheersverordening','exploitatieplan','gerechtelijke uitspraak','omgevingsvergunning','reactieve aanwijzing','voorbereidingsbesluit'}<br/>
 <br/>
and<br/>
Planlijst.includes(self.tekstMetadata.TekstMetadata.typePlan) implies<br/>
 <br/>
self.type.Objecttype.lijst1-&gt;notEmpty()<br/>
 <br/>
and<br/>
VisieLijst.includes(self.tekstMetadata.TekstMetadata.typePlan) implies<br/>
 <br/>
self.type.Objecttype.lijst2-&gt;notEmpty()<br/>
 <br/>
and<br/>
Besluitlijst.includes(self.tekstMetadata.TekstMetadata.typePlan) implies<br/>
 <br/>
self.type.Objecttype.lijst3-&gt;notEmpty()<br/>
</code>

</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'></td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'>T3<br/>
</td>
<td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'><b>Van de attributen label, nummer, naam moet er minstens 1 voorkomen.</b><br/>
</td>
</tr>
<tr><td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'></td>
<td align='left' style='border-top: 0.5pt solid #000000; border-left: 0.5pt solid #000000; border-bottom: 0.5pt solid #000000; border-right: 0.5pt solid #000000; background-color: none;'><code>Context: IMROPT2012::TitelInfo<br/>
Inv Minstens1Attribuut:<br/>
(self.label-&gt;size() + self.nummer-&gt;size() + self.naam-&gt;size()) &gt;= 1<br/>
</code>

</td>
</tr>
</tbody>
</table>

