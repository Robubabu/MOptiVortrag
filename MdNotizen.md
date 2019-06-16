---
title: "MOpti-Vortrag"
author: "Robert Appel"
documentclass: scrartcl
classoption:
   - DIV = 15
header-includes:
   - \usepackage{braket}
   - \usepackage{siunitx}
output:
    pdf_document
---
# Wikipedia: Optical switch
Ein optischer Schalter ist ein Gerät, dass selektiv optische Signale an/aus oder von einem Kanal zu einm anderem schaltet. Der erstgenannte wird als ein optischer (Zeit-Domäne) Schalter oder ein optischer Modulator, während der letztgenannte als ein optischer Raum-Schalter oder einen optischer Router bezeichnet wird. 

## Applications 
Die Technologie des optical switching wird von dem Bedarf an Felxibilität in optischen Netzwerken angetrieben. Führende Anwendugen sind optische Abschirmung, Testsysteme, fern-rekonfigurierbare add-drop Multiplexer und Sensorik.

*Multiplexverfahren (lat. multiplex vielfach, vielfältig) sind Methoden zur Signal- und Nachrichtenübertragung, bei denen mehrere Signale zusammengefasst (gebündelt) und simultan über ein Medium (Leitung, Kabel oder Funkstrecke) übertragen werden. Oftmals werden Multiplexverfahren auch kombiniert, um eine noch höhere Nutzung zu erreichen. Die Bündelung erfolgt, nachdem die Nutzdaten auf ein Trägersignal moduliert wurden. Entsprechend werden sie beim Empfänger nach der Entbündelung (dem Demultiplexen) demoduliert.*

*Ein Add-Drop-Multiplexer ist ein Gerät der Multiplextechnik, das einem Multiplexsignal sowohl ein oder mehrere Teilsignale hinzufügen (add) und auch aus dem Multiplexsignal Teilsignale entnehmen (drop) kann. Das empfangene Multiplexsignal wird bis auf diese Add/Drop-Änderungen unverändert weitergesendet.*

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

