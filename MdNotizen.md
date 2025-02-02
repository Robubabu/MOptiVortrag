---
title: "MOpti-Vortrag"
author: "Robert Appel"
documentclass: scrartcl
classoption:
   - DIV = 15
header-includes:
   - \usepackage{braket}
   - \usepackage{siunitx}
lang: de
output:
    pdf_document
---
# Wikipedia: Optical switch
Ein optischer Schalter ist ein Gerät, dass selektiv optische Signale an/aus oder von einem Kanal zu einm anderem schaltet. Der erstgenannte wird als ein optischer (Zeit-Domäne) Schalter oder ein optischer Modulator, während der letztgenannte als ein optischer Raum-Schalter oder einen optischer Router bezeichnet wird. 

## Applications 
Die Technologie des optical switching wird von dem Bedarf an Felxibilität in optischen Netzwerken angetrieben. Führende Anwendugen sind optische Abschirmung, Testsysteme, fern-rekonfigurierbare add-drop Multiplexer und Sensorik.

> *Multiplexverfahren (lat. multiplex vielfach, vielfältig) sind Methoden zur Signal- und Nachrichtenübertragung, bei denen mehrere Signale zusammengefasst (gebündelt) und simultan über ein Medium (Leitung, Kabel oder Funkstrecke) übertragen werden. Oftmals werden Multiplexverfahren auch kombiniert, um eine noch höhere Nutzung zu erreichen. Die Bündelung erfolgt, nachdem die Nutzdaten auf ein Trägersignal moduliert wurden. Entsprechend werden sie beim Empfänger nach der Entbündelung (dem Demultiplexen) demoduliert.*
 
> *Ein Add-Drop-Multiplexer ist ein Gerät der Multiplextechnik, das einem Multiplexsignal sowohl ein oder mehrere Teilsignale hinzufügen (add) und auch aus dem Multiplexsignal Teilsignale entnehmen (drop) kann. Das empfangene Multiplexsignal wird bis auf diese Add/Drop-Änderungen unverändert weitergesendet.*

Aktuelle Anwendungen sind zB:

+ passiver Schutz-Schalten für wiederherstellung des Service nach ein Störung, zB einem  Bruch in einer Faser 
+ Remote Fiber Test Systems (RFTS) spührt und lokalisiert eine Störung innerhalb des Glasfaserkabels.

Aufstrebende Technik ist optical cross-connection. Also eine Kopplung zwischen mehreren optischen Imputs und Outputs.

---

#Optical switches - Materials and design
##Introduction to optical switches
Eine Glasfaser hat eine Bandbreite von $\SI{25000}{\GHz}$ und ein Kabel das 1000 dieser Fasern enthält kann bis zu sechs billionen Videotelefonate gleichzeitig übertragen, also ein Telefonat für jeden Menschen auf der Erde.
Mit den Techniken wie zB HDTV und 3D-Kino zu Hause, braucht es den Netzausbau und dieser ist nur mit Glasfaser zu bewerkstelligen unter verwendung von Halbleiterlasern. 
Deshalb müssen optische Bauteile für ein optisches Netzwerk gebaut werden. 
Allgemein ist ein Schalter dafür zuständig eine Umelitung eines Signals aufgrund eins Steuersignals durchzuführen. 
Das Signal kann dabei Multiplex-Verkehr oder auch eine große Anzahl von bit Kanälen sein. 
Die Anwendung von optischen Schaltern ist nicht nur limitiert auf Kommunikationsnetzwerke sondern könnten auch in Zukunft in großen multi-Prozessor Computern verwendet werden, deren Datenrate größer als 100Gbit/s.
Für Quantencomputing müssen noch Schalter entwickelt werden, die nicht die Phaseninformation stören.  

Ein optischer Schalter schaltet/leitet selektiv ein optisches Signal einer optischen Faser oder eines optischen Schaltkreis zu einem anderem.
Verschiedene Methoden durch verschiedene physikalische Mechanismen. 


**Elektro-optischer Schalter:**
Verminderung des Brechungsindexes durch anlegen einer Spannung an einem Halbleiter ermöglicht es zu Schalten. 
Wird eine Oberfläche des Materials Ladugsträger angebracht, kommt es dazu, dass der Brechungsindex einer Seite des MAterials reduziert wird, dass führt dazu das die Seiten des Materials unterschiedliche Brechungsindizies besitzen, was wiederum zu totaler inneren Reflexion führt. 
Das führt schließlich dazu, dass ein einfallender Strahl ehr reflektiert wird als an der OF transmittiert wird. 
Das kann verwendet werden um den Strahl zu schalten. 
Änderung des Brechungsindexes eines Strahlengangs zu einem anderen führt zur Interferenz, diese kann konstruktiv bzw destruktiv sein, wenn beide Strahlengänge sich treffen. 
Elektro-optische Schalter machen sich genau das zur Nutze in einem interferometrischen Apparat.

**Thermo-optischer Schalter:**
Der Brechungsindex kann mit Temperatur beeinflusst werden. 
Brechungsindizes von Materialien nehmen ab mit ansteigender Temperatur. 
In einem interferometrischen Apparat kann so ein SChalter ermöglicht werden. 

**Magneto-Optischer Schalter:**
Die Polarisation des Lichtes kann geändert werden, wenn es durch ein Medium durchgeht das mit einem Magnetfeild wechselwirkt. 
Die Rotation der Polarisationsebene ist bekannt als Faraday-Effekt, ist proportional zur Intensitiät des angelegten Magnetfeldes in Richtung des Lichtstrahls. Mit einem Polarisator am Ende des Mediums, kann der Strahl dann abgeschnitten werden. 


**MEMS Schalter:**
Wird ein Strahl an einem micro-Spiegel reflektiert, kann der reflektierte Strahl auf eine Anzahl an optischen Fasern präzise über die Auslenkung des Spiegels gelengt werden. 
Diese Spiegel können zu sog. micro-electro-mechanical (MEMS) systems eingebaut werden. 
Das wird oft bewerkstelligt in dem eine Si-OF in kleine arrays von flachen Balken oder Membranen geäzt wird. 
Die Bewegung dieser Spiegel bildet dann die Basis der auf MEMS-basierenden optischen Schalter.


**semiconductor optical amplifier (SOA) Schalter:**
Propagiert Licht durch ein Aktives Laser Medium, kann sich dessen Wellenlänge, Polarisation, Phase und Amplitude ändern, dabei kann dann durch ein Element, dass sensitiv auf die Eigenschaft reagiert die durch die Anregung verändert wurde, eine (gating function) Ein-/Ausblende Funktion erzeugt/erhalten werden. 
Bsp (grating polarization beam splitter) Pol Beam Splitter während ein Mach-Zehnder Interfero nach Wellenlänge, Polarisation und Phase selektieren kann. 
Das Eibinden eines Halbleiter optischen Verstärkers (SOA) formt die Basis des SOA SSchalters


**Schalten mit nichtlinearen Effekten:**
Mit dem nichtlinearen Kerr Effekt kann der Brechungsindex eines Materials durch anlegen eines elektrischen Feldes verändert werden.
Im Falle das das Licht selbst das E-Feld dastellt, handelt es sich um den optischen Kerr Effekt. 
Dieser ändert den Brechungsindex proportional zur lokalen Strahlungsintensität/-dichte des Lichtes. 
Dieser Brechungsindex ist verantwörtlich für die Effekte des Selbst-Fokusierens und Selbst-Phasen Modulation. 
Der Strahl der durch ein Medium propagiert, erfährt einen Phasenverschub aufgrund des sich ändernen Brechungsindizies, der durch die Intensität des Strahls hervorgerufen wird. 
Wird hierbei noch ein Ein-/Ausblendendes Element (gating) Element verwendet, kann eine Schaltung verwirklicht werden. 


**Flüssigkristall Schalter:**
In Flüssigkristallen ändert die Orientirung der Stab-ähnlichen Moleküle die Polarisierung eines linear pol Strahls, der durch das Medium propagiert. 
Wird die Orientierung der Moleküle kontinuierlich von Anfang bis Ende einer Lage bis $\SI{90}{\degree}$ variiert, durch anlegen einer Spannung, kann die Polarisationsebene des Lichtes um $\SI{90}{\degree}$ gedreht werden, im Vgl zum Input. 
Mit einem Polarisatior kann am Ende das Flüssigkristall, kann dann ein Schalter verwirklicht werden. 
Spannung an kommt durch, Spannung aus nicht.


**Schalter basieren auf photonischen Kristallen:**
photonische Kristalle sind periodische optische Nanokristalle, typisch hexagonal angeordnete arrays auf Löchern in einem flachen Hohlleiter/Wellenleiter (waveguide), so hergestellt, dass sie den selben Effekt auf Photonen wie die Periodizität von Halbleiterkristallen auf Elektronen hat. 
Bei richtiger Wahl des Loch Durchmessers und Periode, können spezifische Wellenlängen nicht durch das Material propagieren. 
Auf diese WEise kann durch entfernen einer solchen Reihe, kann das Licht durch diese Reihe hindurch propagieren, wo keine Löcher sind. 
Durch Änderung des Brechungsindexes des Halbleiter durch den das Licht propagiert, zB durch einen Kontrollpuls, kann ein Phasenverschub auftreten. Durch die Phasenänderung kann dann die Basis des Schalters bilden. 


**Faser-Schalter:** 
Physikalisches hin und her bewegen von zwei Phasern die jeweils von einem Piezoelement aufgebracht sind und so bewegt werden können. 
Bei richtiger Ausrichtung findet Transmission statt und es kann zwischen den Fasern geschaltetet werden. 


**Quanten optisscher Schalter:**
Bei dem Quantum confined stark effect beschreibt die Änderung eine quantisierten Energie in einem Quantentopf wenn ein el Feld über den Quantentopf gelegt wird. 
Daraus resultiert eine reduktion der Übergangsenergie zwischen dem geringsten quantisierten Energieniveau von LOch und Elektron. 
Die optische Absorption ist des Quantentopfes ist erhöht für eine bestimmte Wellenlänge bei Anschluss eine Spannung.

## Electro-optical switches
###Theory and principles of electro-optical switches

![Durschnitt eines Wellenleiters für einen el  opt Sw](./pics/ElOpSwDurchschnittWellenleiter.png){ height=40% }

### Device structures of electro-optical switches

![Schematische Darstellung eines 1x1 el optischen Sw auf SIO](./pics/SchematischerElOpSw.png){ height=40% }

1x1 optischer Schalter = 1x1 optischer Modulator. (1x1 = einer rein , einer raus) 
Wird mit III-V Materialen hergestellt, Bsp Si(Ge), $LiNbO_3$ oder Polymeren.
Wird ie zB im Bild als SOI hergestellt also Silizium auf einem Isolator (SOI). 
Besteht aus einer einzel Moden Lamelle die als einzel Moden-Wellenleite dient, diese besteht aus einem n-typ (n-dotiert) Silizium auf einer $Si0_2$ Lage. 
Eine p-n-Zusammenfügung wird unter der OF der Lamelle erstellt, um dort Ladungsträger in den Wellenleiter einzubringen. 
Wird der p-n-Übergang in Vorwärtsrichtung betrieben, wenn optische Signale in die Lamelle entkuppelt werden, kann eine große Zahl von Ladungsträgern in den Wellenleiter eingebracht werden, dass führt dazu das der Brechungsindexes sich verringern wird. 
Das kann dazu führen, dass der leitende Modus in den Strahlungsmodus des Substrates und der Hülle übergeht. 

> *Für Wellenleiter heißt das ein Strahlendermodus der nicht nur auf den Kern zB einer Faser begrenzt ist. Dieser Modus hat Felder, die überall außerhalb des Leiters oszillieren.*

Das führt dazu das viel Energie des leitenden Modus verloren geht und in der Lamelle absorbiert wird. 
Das führt dazu, dass die Lamelle den Strahl abschneidet. 
$n^+$ zeigen Kollektoren an.
Die Modulationstiefe (relative Modulations Amplitude / max. Änderung in Absorption) von $\SI{96}{\percent}$ bei $\SI{45}{\milli\ampere}$ (was auch der Betriebsstrom ist). 
Der Verlust beim einstrahlen liegt bei $\SI{3.65}{\decibel}$ bei einer Wellenlänge von $\SI{1.3}{\micro\meter}$.
Schlatzeit liegt bei $\SI{160}{\nano\second}$.


+ funkt so, dass durch anlegen eines Feldes ein ein Strahlungsmodus erreicht werden kann. Der kommt durch die reflexion innerhalb des LEiters durch die Änderung des Brechungsindexes. 
+ Dieser Strahlungsmodus hat Einfluss auf die Propagationskonstante des Materials $\gamma = \alpha + i \beta$. Dadurch wird $\beta$ verändert. Das ist der Parameter für die Phase, weshalb man hier auch von Phasenmodulation sprechen könnte. 

## Liquid crystal optical switches
### Liquid crystal theory and principles
Einige organische Stoffe besitzen eine gewisse molekulare Ordnung abhängig von der Temperatur (sog. thermooptische Flüssigkristalle [LC]), also ein Mittelding zwischen kristallinen Stoffen und amorphen Flüssigkeiten.
Manche Eigenschaften der Flüssigkristalle sind anisotrop wie zB die dielektrische Konstante und der Brechungsindex, wie auch bei manchen Festkörpern, sie sind aber gleichzeitig flüssig wie normale Flüssigkeiten. 
Das hat zur Folge, dass die optischen Eigenschaften sich leicht durch anlegen eines el Feldes kotrollieren lassen. 
Grundlegen basieren LC-Bauteile aus einer dünnen Schicht eines LC-Materials zwischen zwei Glassubstraten.
Die Dicke der LC Lage wird durch kleine kallibrierte Platzhalter gleich gehalten. 
Die Platzhalter sind kleine Plastikmicrosphären oder Glasfasern. 
Es werden transparente Elektroden in das Substrat eingebracht, um Spannung auf die LC Mol zu geben, die die Transmission durch die Zelle kontrollieren. 
Schließlich werden auf die Zelle Polarisatoren auf beide Seiten des Substrates angebracht, und andere photonische Aplikationen. 

![Schematischer Aufbau eines LC Bauteils](./pics/SchematischerAufbauLCModulator.png){ height=30% }

#### Liquid crystalline phases
Phasen zwischen Feststoff und Flüssigkeit sind in LC Materialen zu funden, diese werden LC PHasen oder Mesophasen genannt. 
Die Mesophasen tretten auf wenn die Moleküle stark anisotrop sind, üblicherweise bei Stabförmigen oder Scheibenförmigen Molekülen. 
Meistens werden im photonischen Bereich stabförmige Moleküle verwendet. 
Die meisten Materialen haben MEsophasen als Funtion der Temperatur. 
Bei hoher Temperatur sind die Moleküle ungeordnet. Bei Kühlung richten sie sich in einer Bestimmten Richtung aus, sind aber nicht in einer räumlichen Ordnung (= nematische Phase). Wird die Temperatur weiter reduziert bildet sich auch teilweise eine räumliche Ordnung, die eine Lagenstruktur aufweist, mit der langen Axe der Moleküle entlang der Lage (= smektisch [in der Ebene] -A Phase). 
Wird die Temperatur weiter reduziert, bildet sich eine Schieflage der Moleküle aus, im Bezug auf die Senkrechte der Lage ( smetisch-C Phase).
Bei niedrigen Temperaturen bildet sich dann sowohl eine Orientierung als auch eine räumliche Anordnung aus (kristallinier Feststoff). 
Dabei zeigen nicht alle LC Materialien alle Phasen. 

**Hier Fehlt nocht ein Absatz, faöös das wichtig werden sollte** 

#### Basic liquid crystal structures for optical switching

**Twisted nematic (TN) cells**   
Nemtaische LCs mit positiver dielektrischer Anisotropie, für die die dielektrische Konstante größer in der langen Axe des Moleküles ist als in der kruzen Axse ist, werden in TN Materialien verwendet. 
Planare Anordung, (zB LC Molekül Axse parallel zum Glassubstrat) und senkrechtes Schleifen entlang der beiden Anordnungsrichtungen werden verwendet. 
Desalb führen die LC Moleküle eine $\SI{90}{\degree}$ Drehung entlang der LC Zelle. 
Dadurch wird linearpol Licht so modifiziert, dass es mit $\SI{90}{\degree}$ Polarisierungsverschub zum eintreffenden Licht herraustritt. Das geschieht wenn die Maugin Bedinugn erfüllt ist:
$$ d \cdot \Delta n >> \frac{\lambda}{2} $$ 
dabei bezeichnet $d$ die Dicke der Zelle, $\Delta n$ die LC Doppelbrechung/opt. Anisotropie und $\lambda$ die Wellenlänge.   
Die Moleküle orientieren sich neu, wenn die Spannung größer ist als die Schwellspannung $V^{th}$ ist. 
Wird eine Schaltspannung $V^{sw}$ erreicht ( ON-Zustand ), richten sich die LC Moleküle parallel zum Feld aus und die Rotation der Polarisation verschwindet.   
Polarisatoren werden so angebracht, dass sie parallel zur Schleifrichtung (Richtung in der die Mol liegen) sind. 
Die typischen Spannung für Schwellspannung liegen bei 1-2V und bei der Schaltspannung bei 3-5V.

![**Arbeitsschema einer LC Zelle mit a) gekreuzten Polarisatoren b)parallelen Polarisatoren.**   In beiden Fällen tritt unpolarisiertes Licht ein und trifft auf einen Polarisator, dass Licht wird linear polarisiert. Die grauen Bohnen zeigen die Orientierung der Moleküle in der Zelle. a) und b) zeigen jeweils zwei Fälle einmal mit und ohne angelegte Spannung. Der UNterschied zwischen a) und b) sind die Polarisatoren am Ende der Zelle.](./pics/LCPolarisationArbeitsschema.png){ height=50% }

### Liquid crystal switches and applications
#### Switches based on polarization management
Dieser Schalter beruht auf dem Prinzip, dass die Polarisationsebene des einfallenden Lichtes  gedreht wird bei anlegen eines elektrischen Feldes. 
Die Änderung der Polarisation mit einer TN Zelle in Kombination mit einem Doppelbrechenden Calcitkristall, der räumlich Polarisation selektieren kann, oder einem Polarisations Strahlteiler (PBS) ist räumliches optisches Schalten möglich. 
Um die Polarisation zu verstärken und Verluste zu minimieren, wird eine Vielfach Polarisations methode verwendet, indem jede Polarisation parallel verabreitet wird. Das Signal wird in die TE und TM Komponente aufgeteilt, die wiederum am Ausgang rekombiniert werden. 
Das Prinzip ist in \autoref{PolMeth} dargestellt.

![LC Switch Polarisationsverarbeitungs Methodic Schema\label{PolMeth}](./pics/LCSwitchMethodeSchema.png){ height=40% }

> *Die transversalelektromagnetische Welle oder TEM-Welle (engl. Transverse Electromagnetic Mode) ist ein Sonderfall einer elektromagnetischen Welle, bei der in Ausbreitungsrichtung sowohl das elektrische als auch das magnetische Feld verschwindet. Stattdessen befinden sich die magnetischen und elektrischen Felder ausschließlich in Ebenen senkrecht (transversal) zur Ausbreitungsrichtung. Dieser Typ elektromagnetischer Wellen bildet sich als geführte Welle z. B. zwischen Außen- und Innenleiter eines verlustlosen Koaxialkabels aus. Auch die ebene Welle ist ein Beispiel für TEM-Wellen.*

> + *transversal-elektrische Wellen (TE-Wellen); hier verschwindet nur die elektrische Komponente in Ausbreitungsrichtung, während die magnetische Komponente Werte ungleich 0 annehmen kann.*
> + *transversal-magnetische Wellen (TM-Wellen); hier verschwindet nur die magnetische Komponente in Ausbreitungsrichtung, während die elektrische Komponente Werte ungleich 0 annehmen kann.*

Einfachste Bsp dazu ist der zuvor beschriebene 1x2 LC Schalter in \autoref{LCPolSw}. 
Dieser funktioniert wie folgt, der Polarisator P manipuliert die Polarisation zum bevorzugten Output. 
PS bezeichnet hier den LC,liegt keine Spannung an wird das linear polarisierte LIcht aus P um $\SI{90}{\degree}$ in der Polarisation gedreht. Das Licht tritt durch den PBS und trift so auf Port 2. 
Wird eine Spannung größer als $V^{sw}$ angelegt, richten sich die LC Molekülen parallel aus zum E-Feld und es tritt beim PS keine Rotation der Polarisation auf. 
Weshalb das Licht im ON-Modus des Schalters vom PBS zum Port 3 reflektiert wird.   
Die Transmission kann also durch die Spannung an der LC Zelle gesteuert werden, kleinere Spannungen führen zu einer geringeren Rotaion der Polarisationsebene. Folglich können diese Schalter auch als variable optische Dämpfungsglieder (variable optical attenuators = VOA) verwendet werden. 
Durch anlegen einer Spannung $V^{th} < V < V^{sw}$ kann der VOA so eingestellt werden, dass er auf beie Output ein Signal mit einstellbarem Verhältnis zu einander gibt. 
Das ist abhängig von der angelegten Spannung und damit von der Polarisationsebene.  

![LC Polarisations Schalter \label{LCPolSw}](./pics/LCPolRotSwitch.png){ height=50% }

**Performance of polarization management based liquid crystal switches**

Alle Schalter basieren Grundsetzlich auf dem oben dargestellten System, dabei können auch andere optische Instrumente verwendet werden Prismen, Spiegel etc.
Eine schnellere Schaltzeit wird dadurch erhalten, das ferroelektrische LC verwendet werden. 

> *Ferroelektrizität (oder auch Polarisationskatastrophe) beschreibt das Phänomen, dass Stoffe mit einem elektrischen Dipolmoment durch das Anlegen eines äußeren elektrischen Feldes die Richtung der spontanen Polarisation ändern.*

Mit FLCs können Reaktionszeiten von $\SI{35}{\micro\second}$ und mit NLCs nur $\SI{20}{\milli\second}$. 
NLC reagieren langsamer als FLC können auf eine größere Bandbreite im Bezug auf Wellenlängen. 
Tabellen mit Publikationen und Bauart des Schalters sind in den Abb. \ref{LCtab1} und \ref{LCtab2} zu finden. 

![LC Schalter Tab 1 \label{LCtab1}](./pics/TabLCPub.png){ height=60% }

![LC Schalter Tab 2 \label{LCtab2}](./pics/LCPubTab2.png){ height=60% }

## Thermo-optical switches
### Device structures of thermo-optical switches
#### Adiabatic mode coupler
In der \autoref{thopsw} sieht man einen digital optischen Schalter (DOS), dieser ist eine attraktive Variante um räumlich in Kommunikationsnetzwerken mit mehreren Wellenlängen zu schalten. 
Die meist verwendete Variante davon ist der linear Y-Verbinung, diese besteht aus einem Kegelförmigen Wellenleiter, der sich adiabatisch an die eingeführte fundermentale Mode in die bimodale DOS Inputregion anpasst, gefolgt von zwei Einzel-Moden symmetriesche Ausgänge.  
Das Funktionsprinzip des 1x2 DOS basiert auf der Variation des effektiven Modal Indizes bei heizen des Wellenleiters, welcher wiederum den Weg den das LIcht durch die Struktur nimmt ändern kann. 

> *Modal Index bezeichnet die Phasenverschub pro Längeneinheit die das Licht durch den Wellenleiter propagiert*

Die Wärmezufuhr gelingt über Elektroden über oder nahe des optischen Wellenleiters. 
Durch den Joule Effekt wird dann Hitze ins Material gebracht und der Brechungsindex im Wellenleiter verändert sich.   
Haben beide Arme also die gleiche Temperatur, dann ist der DOS geometrisch symmetrisch und wirkt als -3dB (Hälfte) Energie Teiler. 
Energie wird also auf beide Arme gleichmäßig verteilt. 
Bei erhitzen eines Arms wird die Y-Verbindung asymmetrisch; Das Licht wird also zum Arm mit dem höheren Brechungsindize geleitet, da der Input sich adiabatisch anpasst. 
 
![Schematischer Aufbau eines thermo optischen Schalters \label{thopsw}](./pics/ThermoOptSwSchematischerAufbau.png){ height=40% }

## Switching based on optical nonlinear effects
### Structure of nonlinear-effect-based optical switches
#### Nonlinear optical loop mirror
Nicht-lineare optische Schleifen Spiegel (Nonlinear optical loop mirrors [NOLMs]) arbeiten nach dem Prinzip, dass zei LIchtstrahlen die gegenläufig propagieren, unterschiedlich starke nichtlineare Phasenverschiebungen im nichtlinearen Medium erfahren. 
Der Schematische Aufbau eines NOLMs ist in der \autoref{NOLM} dargestellt. 
Er besteht aus einem optischen Koppler und einer Faser Schleife für eine Nichtlinarität. 
Ein Signal wird in den Eingang der Faser gegeben   $E^1$, der Koppler hat eine ungleiche Aufspaltungsrate $\alpha$, so dass die Energie der zwei entgegengerichteten Strahlen $E^2 \& E^3$. 
Der stärkere Strahl erzeugt mehr Selbst-Phasen-Modulation (SPM) als der schwächere, so dass eine Phasendifferenz zwischen den gegenläufigen Strahlenauftritt nach dem sie aus der Faser-Schleife austreten. 
Abhängig von der Stärke des Eingangssignals, ändert sich die nichtlineare Phasenmodulation des stärkeren Strahls sowie der Phasenverschub zwischen den gegenläufigen Strahlen. 
Die zwei gegenläufigen Strahlen treffen sich wieder am Koppler und interferieren, konvertieren ihre  Phasendifferenz zu einer entsprechenden Amplitude an dem Ausgang des Schleifen Spiegels. 
Das Signal das konstruktiv interferiert geht aus dem Ausgang raus $E^{O2}$, der destruktiv interferierte Teil geht wieder auf den Eingang zurück $E^{O2}$.   
**Verwendungsmöglichkeiten:**

+ Autokorrelationssignal Extraktion
+ Rauschunterdrückung 

![Grundlegender Aufbau eines nicht Linearen Schleifen Spiegel (NOLM) \label{NOLM}](./pics/NOLM-Schema.png){ height=40% }

## Magneto-optical switches
### All-optical switches

![Schematischer Aufbau eines el opt. Schalters \label{EOSch}](./pics/ElOptSwSchema.png){ height=20% }

### Magneto-optical switches
Magneto optische Schalter basieren auf dem Faraday Effekt, dieser dreht die Polarisationsebene wenn Licht durch ein magneto optisches Material in der selben Richtung propagiert in der ein B-Feld angelegt ist. 

**Problem:** 

Es wurde nicht soviel Forschung dahingehend betrieben, da es an ausreichend magneto optischen Materialen hoher Qualität magelt. 
Jüngste Fortschritte wurden mit Eisengranaten in den Bismuth ersetzt wurde oder Orthoferrite gemacht, da diese hohe magneto optische Eigenschaften zeigen. 
Diese haben einen geringen Verlust beim einkoppeln von Licht, sowie eine große Bandbreite und eine hohen Grad an Rotation für wenig angelegtes Feld. 

Schalt Methodik lässt sich aber an \autoref{EOSch} erklären. Hier muss nur das EO Material durch ein MO Material ersetzt werden und statt einem E-Feld ein B-Feld angelegt werden. 

---

# Digital MEMS for Optical Switching
## MEMS-BASED OPTICAL SWITCHES

![2D & 3D MEMS Schematischer Aufbau \label{23DMEMS}](./pics/23DMEMSSchema.png){ height=40% }

MEMS wurden sehr schnell attraktiv, da sie die Möglichkeit bieten bei kleinen Verlusten viele Anschlüsse bei wenig kosten pro Anschluss zu schalten. 
Grundlegend ist ein MEMS-Apparat ist ein mechanisch integrierter Schaltkreis bei dem die Antriebskräfte die benötigt werden um Teile zu bewegen elektrostaisch, elektromagnetisch sowie thermisch sein können. 
Deshalb werden Materialien verwendet die sowohl gute mechanische als auch elektrische Eigenschaften haben, zB Si, SiOx und SiNx. 
MEMS basierend auf Silizium können mit vielen Methoden verwirklicht werden zB Volumen microätzen (ätzen der Strukturen in einen Einkristall), Oberflächen microätzen bei dem epitaktische Lagen von Polysizium, Siliziumnitrid und Siliziumoxid ist aufgetragen, strukturiert und selektiv entfernt werden.   
Es gitb zwei Arten von MEMS 2D (digital) und 3D (analog). 
Bei 2D MEMS sind die Schalter digital, da die Spiegelpositionen hier bistabil sind (on/off), siehe \autoref{23DMEMS) a). 
In der Abbildung sind die Spiegel in der Diagonalen angeordnet um eine Querschaltung/Kreuzschaltung zu ermöglichen. 
Wird ein SPiegel aktiviert, bewegt er sich in den Strahl und lengt so den Strahl um $\SI{45}{\degree}$ ab. 
Das ermöglicht auch das ein Strahl durch die Speigelmatrix propagieren kann ohne einen Spiegel zu treffen. 
Das eröffnet die Möglichkeit optische Kanäle hinzufügen und zu entfernen.   
Bei den 3D MEMS ist die Verbindung zwischen Ausgang und Eingang durch, das kippen der Spiegel gegeben (router/selector Architektur). 
Diese Technologie ist sehr vielversprechend für hohe Anschlusszahlen und Kreuzschaltungen mit über 1000 Ein-und Ausgängen bei Verlusten unter 3dB. 

## 2D MEMS TECHNOLOGY :A MATURE TECHNOLOGY TODAY
### MEMS Design Aspects 
![2D MEMS a) Spiegel Aktuatoren Schema b) 16x16 MEMS mit 256 Aktuatoren \label{2DMEMS}](./pics/MEMSSpiegelSwitching.png){ height=40% }

Beste Möglichkeit, Aktuatoren zu erstellen, die die zuvor genannten Kriterien (für 2D) erfüllen, sind in der \autoref{2DMEMS} a) dargstellt. 
Im OFF-Zustand ist ein Winkel zwischen Substrat OF und Aktuator. 
Wenn eine Spannung angelgt wird zwischen dem Aktuator und der OF bewegt sich der Aktuator nach unten aufgrund der elektrostatischen Anziehungskraft. Der Spiegel wird so geätzt, dass er $\SI{90}{\degree}$ zur OF steht. 
Die elektrostatische Antriebsvariante ist besonders von Vorteil, da es sehr geringe Energie Disspation erlaubt, in einer Größenordnung von einigen Microwatt (für 16x16). 

## APPLICATIONS OF 2D MEMS OPTICAL SWITCHES

![a) Multiplexer Schema b) Multiplexer mit 2D MEMS \label{2DMEMSMultip}](./pics/Multiplexer+MEMSMuliplexer.png){ height=40% }

**Rekonfigurierbarer Wellenlängen add-drop Multiplexer:**  
Ein rekonfigurierbarer Wellenlängen add-drop Multiplexer siehe \autoref{2DMEMSMultip} a) ist ein wichtiges Bauelemnt für optische Netzwerkknoten. Es besteht aus einem Wellenlängen demultiplexer, der die Wellenlänge von einer Faser auf mehrere Fasern aufteilt. Die Schalter im inneren erlauben es Signale zu entfernen (droppen) oder gleichzeitig neue Signale hinzu zu fügen. Die Signale werden wieder in einem Wellenlängen Multiplexer zusammengeführt und auf eine Faser gegeben.   

**Rekonfigurierbarer Wellenlängen add-drop Multiplexer mit 2D MEMS:**  
Ein optischer 2x2 Schalter kann durch eine MEMS-Apparatur ausgetauscht werden. Die MEMS Chips haben zwei Reihen aus Spiegeln, die gleichzeitig schalten. 
Wenn ein Paar von Spiegeln aktiviert wird, wird das einkommende Signal auf den Drop-Port geleitet und der jeweilige Add-Port  gibt sein Signal auf den Ausganggegeben. 
Wird kein Spiegel aktiviert geht das Signal direkt auf den Ausgang. 









