# OER - EinführungGeoinformatik
**Die Modul sind wie folgt aufgebaut**

1. Überblick
2. Thematischer Hintergrund
3. Übungen und Leitfäden
4. Quiz 
5. Zusammenfassung 

**Generelle Informationen**

Dieses Tutorial richtet sich hauptsächlich an Teilnehmer, die in kurzer Zeit ihr Wissen zum Thema Geographische Informationssysteme verbessern wollen. Du benötigst keine Vorkenntnisse für die Bearbeitung. 

Dieses Tutorial wurde am Institut für Geodäsie der Fachhochschule Bochum in enger Zusammenarbeit mit der Universität Münster und der Universität Bochum entwickelt. Hauptautoren Fabian Przybylak, Lena Pfeil und Jonas Haine unter der Leitung von Prof. Dr. Carsten Keßler.

Du darfst das OER (H5P-Inhalte) unter den Bedingungen der CC-BY-SA 4.0-Lizenz frei verwenden, verändern und vervielfältigen. Jeglicher Code, der mit dem OER zur Verfügung gestellt wird, kann unter den Bedingungen der MIT-Lizenz verwendet werden. Bitte lesen Sie die [vollständigen Lizenzbedingungen](/LICENSE.md). 

Das Projekt OER4SDI wurde von der Digitalen Hochschule NRW empfohlen und wird durch das Ministerium für Kultur und Wissenschaft NRW gefördert. 

# Module 1 - Geographische Informationssysteme
         	           	
## 1. Überblick

In diesem Modul lernst du, was Geographische Informationssysteme (GIS) sind und wofür du diese nutzen kannst. Darüber hinaus bekommst du einen ersten Eindruck von der Oberfläche eines GIS und lernst gängige Datentypen und Formate kennen. 

**Nachdem du die folgende OER abgeschlossen hast, wirst du wissen:**
* Was Geographische Informationssysteme sind und wofür man diese nutzen kann
* Welche verschiedenen GIS es gib
* Was räumliche Daten ausmacht und in welchen Typen und Formaten diese in einem GIS verarbeitet werden können
* Wie die Oberfläche von ArcGIS Pro aufgebaut ist
* Wie du ein einfaches erstes Projekt in ArcGIS Pro aufsetzen kannst

## 2. Thematischer Hintergrund

### 2.1 Kurze Einführung
Die räumliche Analyse bezieht sich auf die Untersuchung von Daten, die geografisch verortet sind. Ziel solcher Analysen ist es, räumliche Beziehungen und Muster zwischen verschiedenen geografischen Merkmalen zu verstehen, indem ihre geografischen Standorte in die Betrachtung mit einbezogen werden.

Geografische Informationssysteme (GIS) sind computergestützte Systeme, die aus mehreren Komponenten bestehen. Diese dienen der Erstellung, Verwaltung, Visualisierung und Analyse von Geodaten. Ein GIS ermöglicht es, verschiedene Informationen über geografische Standorte zu integrieren und in Karten darzustellen. Neben der reinen Visualisierung von Daten erlaubt es GIS, diese mithilfe von Tools zu verarbeiten und dadurch neue Datensätze und Informationsgehalte zu generieren.

Ein GIS sollte dann eingesetzt werden, wenn komplexe räumliche Zusammenhänge oder umfangreiche Datensätze in Kartenform analysiert werden sollen. Für einfache Informationsabfragen, die sich auch aus Tabellen ablesen lassen, ist der Einsatz eines GIS nicht zwingend erforderlich.

Ein praxisnahes Beispiel zeigt die Identifikation der zehn afrikanischen Länder mit den höchsten Konfliktindexwerten zwischen 1966 und 1978. Diese Aufgabe lässt sich mit einer Tabelle lösen, da lediglich die Anzahl der Konflikte je Land benötigt wird. Wird jedoch die Frage gestellt, ob diese Länder geografisch geclustert sind, reicht eine einfache Tabelle nicht mehr aus. Hier wird ein Geodatensatz benötigt, um geografische Standorte mit den Konfliktwerten zu verknüpfen. Für diese Analyse ist ein GIS erforderlich.

Bei der Auswahl eines GIS ist zu beachten, dass die Entscheidung oft vom jeweiligen Anwendungsfall abhängt. Persönliche Präferenzen können ebenfalls eine Rolle spielen. Die bekanntesten GIS, wie QGIS und ArcGIS, bieten unterschiedliche Vor- und Nachteile. ArcGIS ist eine weit verbreitete kommerzielle GIS-Software, die von ESRI entwickelt wurde. Sie bietet eine umfassende Palette von Funktionen für fortgeschrittene räumliche Analysen und kann tief in Unternehmensumgebungen integriert werden. ArcGIS wird in verschiedenen Lizenzstufen angeboten, die Kosten können sich je nach Umfang im Bereich von mehreren tausend bis über zehntausend Dollar bewegen.

QGIS hingegen ist eine leistungsfähige, quelloffene (kostenlose) GIS-Software, die von einer aktiven Community entwickelt wird. Sie bietet die meisten Funktionen, die auch in ArcGIS verfügbar sind, und kann durch Plugins individuell erweitert werden. QGIS ist besonders geeignet für Mac- und Linux-Umgebungen und wird aufgrund seiner Plattformunabhängigkeit sowie der aktiven Unterstützung durch die Community immer beliebter.

In einer Vergleichstabelle werden QGIS und ArcGIS gegenübergestellt. QGIS zeichnet sich durch seine Kostenfreiheit und die Erweiterbarkeit über Plugins aus, während ArcGIS durch seine umfassende Funktionalität und die einfache Integration in Unternehmensumgebungen punktet. Beide Systeme bieten eine benutzerfreundliche Oberfläche und haben starke Communities, die bei Fragen und Problemen unterstützen.

Zusammengefasst: QGIS bietet eine kostengünstige, flexible Lösung, während ArcGIS fortschrittlichere Funktionen und eine bessere Integration in Unternehmen bietet, allerdings zu höheren Kosten.



### 2.2 Inhaltliche Vertiefung 
Geodaten sind Informationen, die die geografische Lage, Größe, Form oder Eigenschaften von geografischen Objekten wie Städte, Straßen, Seen oder Berge beschreiben. Diese Daten werden in digitalen Karten und geografischen Informationssystemen (GIS) genutzt, um räumliche Beziehungen und Muster zu analysieren und zu visualisieren.

In einer GIS-Umgebung werden Geodaten häufig in zwei Hauptformen dargestellt: Vektor- und Rasterdaten. Vektordaten repräsentieren geografische Objekte als Punkte, Linien und Polygone, wobei sowohl Geometrien als auch Attributdaten gespeichert werden. Rasterdaten bestehen hingegen aus einer regelmäßigen Anordnung von Pixeln, bei denen jedes Pixel eine numerische Eigenschaft wie Höhe oder Temperatur speichert.

Die einfachste Form von Vektordaten ist der Punkt, der einen geografischen Standort durch ein Koordinatenpaar repräsentiert. In Karten werden Punkte häufig durch Symbole wie Kreise oder Quadrate dargestellt und können beispielsweise Städte, Messstationen oder Brunnen markieren. Linien bestehen aus verbundenen Punkten und repräsentieren lineare geografische Objekte wie Straßen, Flüsse oder Flugrouten. Sie werden in Karten durch Eigenschaften wie Farbe und Breite symbolisiert. Polygone hingegen sind geschlossene Flächen, die durch Linienzüge gebildet werden und sowohl eine innere als auch eine äußere Grenze haben. Sie repräsentieren geografische Flächen wie Gebäudegrundrisse, Seen oder Parks.

In GIS-Anwendungen werden Vektordaten in Layern organisiert. Ein Layer stellt eine strukturierte Gruppierung von Vektordaten dar, die ähnliche Eigenschaften oder Geometriearten teilen. Layer ermöglichen es, die Sichtbarkeit und Anzeige der Geodaten in der GIS-Software zu steuern.

Rasterdaten bestehen aus einer regelmäßigen Anordnung von Zellen oder Pixeln. Jedes Pixel speichert dabei eine numerische Eigenschaft, wie beispielsweise Höhe, Temperatur oder Landnutzung. Rasterdaten werden oft für Fernerkundungsdaten, digitale Höhenmodelle oder die Darstellung kontinuierlicher Daten, wie Niederschläge, verwendet.

Die Pixeltiefe, auch Bittiefe genannt, beschreibt, wie viele Bits zur Darstellung eines Pixels in einem Rasterbild verwendet werden. Eine höhere Pixeltiefe ermöglicht eine größere Farbvielfalt oder Genauigkeit der dargestellten Daten. Ein 1-Bit-Raster kann zum Beispiel nur zwei Werte speichern, nämlich 0 und 1.

Attribute sind nicht-räumliche Informationen, die mit räumlichen Merkmalen verbunden werden. Sie werden in Attributtabellen gespeichert und helfen dabei, geografische Daten genauer zu charakterisieren und in einen Kontext zu setzen. Diese Attribute können in verschiedene Datentypen unterteilt werden, wie beispielsweise Integer (ganze Zahlen), Float (Gleitkommazahlen), Double (doppeltgenaue Gleitkommazahlen) und Text (Zeichenketten). Die Wahl des Datentyps beeinflusst dabei sowohl die Genauigkeit und Dateigröße der dargestellten Informationen.

In der Welt der Geoinformatik und GIS spielen verschiedene Dateiformate eine wichtige Rolle bei der Speicherung, Verarbeitung und dem Austausch von räumlichen Daten. Jedes Dateiformat wurde entwickelt, um spezifische Anforderungen an die Darstellung, Analyse und Verwaltung von Geodaten zu erfüllen. Die Wahl des Formats hängt dabei von den Anforderungen der jeweiligen GIS-Anwendung ab. Zu den gängigsten Formaten gehören Vektor- und Rasterformate.

Ein Beispiel für ein Vektorformat ist das **Shapefile (.shp)**, das eine Sammlung von Features mit identischen Geometrietypen und strukturierten Attributen darstellt. Ein Shapefile besteht in der Regel aus mehreren Dateien mit verschiedenen Funktionen, wie der Speicherung von Attributinformationen, Koordinatensystemen oder räumlichen Indexdaten.

Ein weiteres verbreitetes Vektorformat ist das **GeoPackage (.gpkg)**, ein standardisiertes, plattformunabhängiges und kompaktes Format für die Speicherung von Geodaten in einer SQLite-Datenbank. Es bietet eine hohe Kompatibilität mit Programmen wie QGIS, kann aber in ArcGIS nur eingeschränkt genutzt werden.

Im Bereich der Rasterdaten ist das **GeoTIFF**-Format ein offenes und weit verbreitetes Format, das räumliche Georeferenzierungsinformationen und Metadaten zu den Bilddaten speichert. Ein weiteres wichtiges Rasterformat ist **Imagine (.img)**, das speziell für Fernerkundungsdaten entwickelt wurde und in der ERDAS-Software verwendet wird. Allerdings ist die Interoperabilität dieses Formats eingeschränkt.

**Geodatenbanken** wie die **File Geodatabase (.gdb)**, die von Esri entwickelt wurde, bieten die Möglichkeit, räumliche Daten und zugehörige Attribute in einer strukturierten Ordnerstruktur zu organisieren. Dieses Format unterstützt die Speicherung mehrerer Feature-Klassen und ermöglicht es, topologische Beziehungen zwischen den Features zu definieren.

Zusammenfassend lässt sich sagen, dass die Wahl des geeigneten Dateiformats von den Anforderungen der GIS-Anwendung abhängt. Vektorformate wie Shapefile und GeoPackage eignen sich für die Verwaltung und Analyse von diskreten geografischen Objekten, während Rasterformate wie GeoTIFF und Imagine für kontinuierliche Daten wie Satellitenbilder oder Höhenmodelle verwendet werden. Geodatenbanken bieten eine flexible und leistungsfähige Möglichkeit zur Organisation großer Datenmengen in GIS.

## 3. Übungen und Leitfäden

**Zusammenfassung des Inhaltes**
Wir werden uns mit dem Umgang der wichtigsten Funktionen der Benutzeroberfläche von ArcGIS Pro beschäftigen. Im Zuge dessen lernt ihr die Kartenansichten und -layer anzupassen. Außerdem werden wir bereits eine eigene kleine Karte über die Schulstandorte in Bochum erstellen, ausgestalten und exportieren.

# Modul 2 - KoordiantensystemeUndProjektionen
         	           	
## 1. Überblick

In diesem Modul lernst du, was Koordinatensysteme und Projektionen sind, wie diese funktionieren und warum diese Notwendig für die Sichtung, Bearbeitung und Analyse von räumlichen Daten sind. 

**Nachdem du die folgende OER abgeschlossen hast, wirst du wissen:**
* Was unter dem Begriff der Georeferenzierung zu verstehen ist
* Welche Schwierigkeiten beim Georeferenzieren auf der Erde überwunden werden müssen
* Wie verschiedene Ansätze von Koordinatensystemen Lösungen bieten können
* Was Projektionen sind und wie diese es schaffen dreidimensionale Infos in einem zweidimensionalen Raum zu bringen
* Welche verschiedenen Projektionsformen es gibt und in welchen konkreten Anwendungsfällen diese häufig genutzt werden 


## 2. Thematischer Hintergrund

### 2.1 Kurze Einführung
Koordinatensysteme sind von zentraler Bedeutung in der Geoinformatik, da sie es ermöglichen, räumliche Informationen eindeutig zu referenzieren und zu analysieren. Mit Hilfe von Koordinatensystemen können Positionen von Objekten auf der Erdoberfläche präzise beschrieben werden. Dabei spielen sowohl globale als auch regionale und lokale Koordinatensysteme eine Rolle.

Die Erdoberfläche entspricht nicht einer perfekten Kugel, sondern hat die Form eines Geoids, das durch die Unregelmäßigkeiten der Erdmasse und der Gravitationskräfte bestimmt wird. Um diesen Faktoren gerecht zu werden, werden verschiedene Koordinatensysteme entwickelt. Ein bekanntes geozentrisches Koordinatensystem ist das World Geodetic System 1984 (WGS84), das für viele globale Anwendungen genutzt wird und auf der Annahme basiert, dass die Erde eine Kugel oder ein Ellipsoid ist. Dieses System verwendet Breiten- und Längengrade, um die Positionen von Punkten auf der Erdoberfläche zu bestimmen.

Neben geozentrischen Koordinatensystemen gibt es auch projektive Koordinatensysteme, die verwendet werden, um die gekrümmte Erdoberfläche auf einer flachen Karte darzustellen. Ein Beispiel hierfür ist das Universal Transverse Mercator (UTM), das häufig für regionale und nationale Kartenanwendungen verwendet wird. Diese Systeme minimieren Verzerrungen in einem spezifischen definierten Gebiet.

Für bestimmte lokale Anwendungsfälle werden zudem lokale Koordinatensysteme genutzt, die auf einem spezifischen Gebiet oder Referenzpunkt basieren. Solche Systeme, wie das Deutsche Hauptdreiecksnetz (DHDN), sind besonders nützlich, wenn detaillierte Untersuchungen in einem kleinen, spezifischen Bereich durchgeführt werden. Die Wahl des Koordinatensystems hängt dabei stets von den Anforderungen der jeweiligen Anwendung ab.

### 2.2 Inhaltliche Vertiefung 
Projektionen sind Methoden, um die dreidimensionale Erdoberfläche auf einer zweidimensionalen Karte darzustellen. Da es geometrisch unmöglich ist, diese Überführung ohne Verzerrungen vorzunehmen, können sich Projektionen auf Winkel, Formen, Entfernungen und Flächen auswirken. Sie sind jedoch notwendig, um geografische Daten visuell interpretierbar und analysierbar zu machen.

Es gibt verschiedene Familien von Projektionen, darunter Zylinder-, Kegel- und Planar-/Azimuthalprojektionen. Jede dieser Projektionen hat unterschiedliche Eigenschaften und Anwendungsbereiche. Die Zylinderprojektion projiziert die Erdoberfläche auf einen Zylinder, der zu einer Ebene ausgerollt wird. Eine der bekanntesten zylindrischen Projektionen ist die Mercator-Projektion, die insbesondere in der Navigation verwendet wird, da sie gerade, parallele Breiten- und Längengrade zeigt. Sie erhält die Winkel, aber verzerrt Flächen, was dazu führt, dass beispielsweise Regionen in hohen Breitengraden größer erscheinen, als sie tatsächlich sind.

Die Kegelprojektion projiziert die Erdoberfläche auf einen Kegel. Sie ist besonders nützlich für die Darstellung von Regionen, bei denen die Verzerrungen entlang der Kegeltangente gering sind. Ein Beispiel dafür ist die Lambert-Kegelprojektion, die häufig in der Kartographie verwendet wird, um bestimmte Regionen flächentreu darzustellen.

Die Planar- oder Azimuthalprojektion projiziert die Erdoberfläche auf eine Ebene und wird häufig zur Darstellung von Polarregionen verwendet. Diese Projektion eignet sich gut für die Darstellung von Punkten oder Regionen, allerdings verzerrt sie Entfernungen und Winkel, je weiter man sich vom Zentrum der Projektion entfernt.

Bei der Auswahl der richtigen Projektion müssen verschiedene Faktoren berücksichtigt werden, wie der geografische Bereich, die Art der Daten und der Verwendungszweck der Karte. Winkeltreue Projektionen, wie die Mercator-Projektion, erhalten die Winkel und sind ideal für Navigationszwecke. Flächentreue Projektionen, wie die Albers-Projektion, stellen die Größenverhältnisse korrekt dar und eignen sich besonders für großflächige Analysen. Längentreue Projektionen, wie die Plate-Carree-Projektion, erhalten die Entfernungen und sind besonders nützlich für seismische oder Funkkartierungen.

Insgesamt ist die Wahl der Projektion entscheidend, um geografische Informationen je nach Anwendungsfall korrekt darzustellen und zu analysieren.

## 3. Übungen und Leitfäden

# Modul 3 - DigitalisierenSelektierenManipulieren
         	           	
## 1. Überblick

In diesem Modul lernst du, Daten in einem Geographischen Informationssystem (GIS) selbst zu digitalisieren, zu selektieren und zu manipulieren und diese Kenntnisse in der Praxis anzuwenden. 

**Nachdem du die folgende OER abgeschlossen hast, wirst du wissen:**
* Wie du Infomationen zu Vektordaten in Form von Punkt, Linien und Polygon Geometrien digitalisieren kannst
* Wie du über verschiedene Wege einzelne oder eine Gruppe von Features selektieren und anschließend exportieren kannst
* Wie du einfache SQL-Abfragen einsetzen kannst
* Wie einfache Datenmanipulationen über Standardwerkzeuge wie Buffer, Clip, oder Intersect funktionieren


## 2. Thematischer Hintergrund

### 2.1 Kurze Einführung
In der Geoinformatik und bei der Arbeit mit Geografischen Informationssystemen (GIS) spielen die Konzepte des Digitalisierens, Selektierens und Manipulierens eine zentrale Rolle. 

Das Digitalisieren bezieht sich auf den Prozess der Umwandlung analoger geografischer Informationen in digitale Formate. Dieser Prozess beinhaltet oft das Eingeben von geografischen Entitäten wie Straßen, Flüssen oder Gebäudegrenzen in ein GIS, indem man Punkte, Linien oder Polygone auf digitalen Karten erstellt. Das Ergebnis ist eine Geodatenbank, die es ermöglicht, räumliche Analysen und Abfragen durchzuführen.

Das Selektieren ist der Akt des Auswählens bestimmter geografischer Daten oder Objekte innerhalb einer GIS-Datenbank. Dies erfolgt mithilfe von Selektionswerkzeugen, die es den Benutzern ermöglichen, geografische Elemente basierend auf verschiedenen Kriterien wie Lage, Attributen oder räumlichen Beziehungen auszuwählen. Selektionen sind von entscheidender Bedeutung, um spezifische Informationen zu isolieren und sie für Analysen oder Präsentationen zu nutzen.

Das Manipulieren von geografischen Daten umfasst die Bearbeitung und Veränderung von räumlichen Informationen in einem GIS. Dazu gehört unter anderem das Verschieben, Rotieren, Skalieren oder Ändern der Geometrien und Attribute. Die Manipulation ist wichtig, um Geodaten an aktuelle Anforderungen anzupassen, Fehler zu korrigieren oder neue Informationen hinzuzufügen.

Insgesamt gehört das Digitalisieren, Selektieren und Manipulieren von Geodaten zu den grundlegenden Konzepten in der Geoinformatik und der Arbeit mit geographischen Informationssystemen. Sie ermöglichen die Umwandlung von analogen Karten und Daten in digitale Formate, die Auswahl relevanter Informationen für Analysen und die Anpassung von Geodaten an spezifische Anforderungen. Diese Prozesse sind unverzichtbar, um räumliche Informationen effektiv zu nutzen und fundierte Entscheidungen in verschiedenen Anwendungsgebieten wie Stadtplanung, Umweltschutz, Landmanagement und Katastrophenmanagement zu treffen.

### 2.2 Inhaltliche Vertiefung 
Das Digitalisieren beschreibt den Prozess, bei dem analoge geografische Informationen in digitale Formate umgewandelt werden. In einem Geographischen Informationssystem (GIS) wie ArcGIS Pro erfolgt dies durch das Zeichnen von Linien, Punkten und Polygonen, wobei analoge Karten oder Luftbilder in digitale Daten umgewandelt werden. Dieser Prozess ermöglicht es, geografische Informationen zu speichern, zu bearbeiten und räumliche Analysen durchzuführen. Zu den verwendeten Digitalisierungswerkzeugen gehören Editor-Werkzeuge für das Erstellen von Vektordaten, Snapping-Werkzeuge, die sicherstellen, dass neue Features genau an bereits existierenden Features ausgerichtet werden, sowie Topologie-Werkzeuge, die sicherstellen, dass räumliche Beziehungen, wie das Vermeiden von Überschneidungen, eingehalten werden.

Ein wesentlicher Aspekt beim Arbeiten in einem GIS ist das Selektieren. Dies ermöglicht es, spezifische geografische Daten oder Objekte innerhalb eines Datensatzes auszuwählen. Die Selektion kann manuell durch Klicken auf einzelne Features, durch das Zeichnen einer Auswahlfläche oder basierend auf Attributen oder räumlichen Beziehungen erfolgen. Zum Beispiel kann eine Abfrage erstellt werden, um alle Straßen eines bestimmten Namens oder alle Gebäude über einer bestimmten Höhe auszuwählen. Diese Abfragen werden häufig in einer SQL-ähnlichen Syntax formuliert und erlauben eine detaillierte Analyse und Weiterverwendung der ausgewählten Daten.

Manipulationen von geografischen Daten umfassen das Bearbeiten und Anpassen der Daten, um sie den Projektanforderungen anzupassen oder um Fehler zu korrigieren. Zu den Manipulationswerkzeugen gehören das Zuschneiden von Layern, das Erstellen von Pufferzonen um Features, das Kombinieren von Geometrien und Attributen mehrerer Layer sowie das Erzeugen neuer Features durch Überlappung bestehender Layer. Beispiele für Manipulationen sind das Verschieben von Features, das Drehen und Skalieren von Objekten oder das Bearbeiten von Scheitelpunkten, um die Form eines Features zu ändern.

Diese Werkzeuge und Methoden sind essenziell, um geografische Daten in einem GIS zu erfassen, zu bearbeiten und für spezifische Analysen und Anwendungen vorzubereiten. Sie ermöglichen eine präzise Kontrolle über die räumlichen Daten und ihre Darstellung, wodurch die Genauigkeit und Aussagekraft der Analysen erhöht wird.

## 3. Übungen und Leitfäden

**Zusammenfassung des Inhaltes**
Wir werden uns mit dem Umgang der wichtigsten Funktionen der Benutzeroberfläche von ArcGIS Pro beschäftigen. Im Zuge dessen lernt ihr die Kartenansichten und -layer anzupassen. Außerdem werden wir bereits eine eigene kleine Karte über die Schulstandorte in Bochum erstellen, ausgestalten und exportieren.

## 3. Übungen und Leitfäden

# Modul 4 - Kartenlayouts
         	           	
## 1. Überblick

In diesem Modul lernst du, wie du in einem Geographischen Informationssysteme (GIS) Kartenlayouts anlegst und in verschiedenen Formaten exportieren kannst. Darüber hinaus wird dir theoretisches Wissen bezüglich kartographischer Best Practices vermittelt.  

**Nachdem du die folgende OER abgeschlossen hast, wirst du wissen:**
* Wie du in einem GIS ein Kartenlayout anlegst und die gewünschten Elemente hinzufügst
* Welche Elemente in ein gutes Kartenlayout gehören
* Auf welche stylistischen gegebenheiten du beim symbolisieren deiner Layer achten solltest (Farbe, Farbraum, Helligkeit, Sättigung, Symbolwirkung)
* Wie du deine Layer klassifizieren kannst und worauf dabei zu achten ist
* Wie du deine fertigen Kartenlayouts in verschiedenen Formaten exportieren kannst  


## 2. Thematischer Hintergrund

### 2.1 Kurze Einführung
Karten sind ein wesentliches Werkzeug, um räumliche Informationen visuell darzustellen und zu analysieren. Sie helfen uns, komplexe geografische Daten in verständlicher Form zu präsentieren. Ein besonderes Augenmerk wird dabei auf das richtige Layout und die Gestaltung von Karten gelegt, um eine klare Interpretation der dargestellten Informationen zu gewährleisten.

Ein Beispiel sind Mental Maps, also kognitive Karten, die auf individuellen Erfahrungen und Erinnerungen basieren. Sie dienen der persönlichen Orientierung und der Planung von Routen in bekannten Umgebungen. Diese Karten sind subjektiv und stark von den Erfahrungen des jeweiligen Betrachters geprägt.

Topographische Karten hingegen bieten eine detaillierte Darstellung geografischer Merkmale wie Geländeformen, Höhenlinien, Flüsse, Straßen und Gebäude. Sie sind besonders nützlich für die Navigation und bei Outdoor-Aktivitäten. Im Vergleich dazu bieten topographische Übersichtskarten eine vereinfachte Darstellung der Landschaft und sind ideal, um einen schnellen Überblick über ein Gebiet zu bekommen.

Politische Karten heben politische Grenzen und Verwaltungseinheiten hervor. Sie veranschaulichen die geopolitischen Strukturen eines Gebiets und helfen dabei, die politische Aufteilung und die Beziehungen zwischen Ländern und Regionen zu verstehen.

Ein weiterer wichtiger Kartentyp sind Flurkarten oder Liegenschaftskarten, die Grundstücke und Landbesitz darstellen. Sie spielen eine wesentliche Rolle bei der Verwaltung von Ländereien, der Immobilienbewertung und der Einhaltung von Bauvorschriften.

Wirtschaftskarten bieten Einblicke in die Verteilung von Branchen, Rohstoffen und Infrastruktur in einem geografischen Gebiet. Sie sind von entscheidender Bedeutung für die Standortplanung, Wirtschaftspolitik und Marktanalysen.

Wander- und Freizeitkarten sind speziell für Outdoor-Enthusiasten konzipiert. Sie zeigen Wanderwege, Sehenswürdigkeiten und andere wichtige Punkte für Aktivitäten in der Natur und erleichtern die Planung solcher Ausflüge.

Ein Liniennetzplan zeigt die Routen öffentlicher Verkehrsmittel in einer Stadt oder Region und hilft Nutzern, ihre Fahrten mit Bus, Bahn oder U-Bahn zu planen.

Panoramakarten bieten eine umfassende visuelle Darstellung einer Region und vermitteln den Betrachtern eine weitreichende Perspektive auf geografische Merkmale und Sehenswürdigkeiten. Sie sind oft in touristischen Kontexten zu finden.

Schließlich gibt es interaktive Karten, die es den Nutzern ermöglichen, mit den dargestellten Informationen zu interagieren. Diese Karten bieten dynamische Funktionen, wie das Ein- und Auszoomen oder das Anzeigen von detaillierten Informationen durch Anklicken bestimmter Punkte.

Choroplethenkarten visualisieren die Verteilung bestimmter Daten in geografischen Regionen, indem sie die relative Dichte oder Werteintensität durch Farbnuancen darstellen. Sie sind besonders nützlich, um Muster und Unterschiede in Daten schnell zu erkennen.

### 2.2 Inhaltliche Vertiefung 1
In der Kartenerstellung sind Symbolisierung und Klassifizierung von Layern entscheidend, um Karten verständlich und ansprechend zu gestalten. Eine korrekte Symbolisierung und Klassifikation hebt wichtige Informationen hervor, was die Interpretation und Kommunikation von geografischen Daten erleichtert. Der Farbton, also die Farbnamen, wird genutzt, um verschiedene Datenkategorien zu visualisieren. Bestimmte Farbtöne können emotionale Assoziationen hervorrufen, wie Rot für negative und Grün für positive Werte. Farben sollten konsistent verwendet und Farbsehschwächen berücksichtigt werden. Die Helligkeit einer Farbe beeinflusst Kontrast und visuelle Hierarchie, wobei hellere Farben mehr Aufmerksamkeit erzeugen und dunklere in den Hintergrund treten. Gesättigte Farben haben ebenfalls eine starke visuelle Wirkung und sind nützlich, um wichtige Informationen hervorzuheben, während weniger gesättigte Farben dezentere Informationen anzeigen.

Ein Farbraum ist ein dreidimensionales Modell, das Farben systematisch organisiert und ermöglicht, verschiedene Farben basierend auf Helligkeit, Sättigung und Farbton zu vergleichen. Der Mensch nimmt Farben jedoch nicht symmetrisch wahr, weshalb alternative Farbräume wie CIELAB entwickelt wurden, um die menschliche Farbwahrnehmung zu berücksichtigen.

Symbole spielen in der Kartographie eine wichtige Rolle, um geografische Merkmale wie Standorte oder Ereignisse verständlich darzustellen. Die Wahl der Symbole sollte kulturelle Kontexte berücksichtigen und in der Kartendarstellung konsistent sein. Auch die Größe, Farbe und Platzierung der Symbole sind wichtig, um Hierarchien und emotionale Reaktionen zu steuern.

Es gibt verschiedene Farbschemata, die für die Darstellung von Daten genutzt werden. Qualitative Farbschemata visualisieren kategoriale Daten ohne spezifische Reihenfolge, wobei Farbtöne mit gleichen Helligkeits- und Sättigungswerten verwendet werden. Sequentielle Farbschemata hingegen stellen kontinuierliche Daten wie Temperatur oder Einkommen dar, indem sie von hellen zu dunklen Farbtönen übergehen. Divergente Farbschemata visualisieren geordnete Daten, die sich um einen zentralen Wert gruppieren, mit symmetrischen Anpassungen der Farbtöne um diesen Wert herum.

Klassifikationsintervalle sind wichtig, um numerische Daten in Klassen zu unterteilen. Methoden wie Quantile, Equal Intervals oder Jenks werden verwendet, um die Daten in sinnvolle Gruppen zu unterteilen und somit eine angemessene Visualisierung zu ermöglichen.

In der Kartographie sind grafische Variablen wie Farben, Formen, Größe, Helligkeit und Ausrichtung entscheidend, um geografische Merkmale und räumliche Beziehungen darzustellen. Schriftarten und -größen beeinflussen ebenfalls die Lesbarkeit und können genutzt werden, um Objekte nach Bedeutung zu unterscheiden. Die Platzierung von Beschriftungen folgt bestimmten Regeln, abhängig davon, ob es sich um flächenhafte, lineare oder punktuelle Objekte handelt, um eine klare und verständliche Darstellung der Informationen auf der Karte zu gewährleisten.

### 2.3 Inhaltliche Vertiefung 2

Das Kartenlayout umfasst die Anordnung verschiedener Elemente auf einer Karte, um geografische Informationen klar und effektiv zu kommunizieren. Zu den Hauptelementen gehören die Hauptkarte, die Legende, der Kartentitel, der Maßstab, das Koordinatengitter und weitere visuelle Informationen. Ein gutes Kartenlayout ist entscheidend für die Übersichtlichkeit und Verständlichkeit der Karte, damit der Betrachter die Informationen leicht erfassen kann.

Der Kartentitel ist eine prägnante Überschrift, die das Hauptthema der Karte beschreibt. Er gibt dem Betrachter eine erste Orientierung, ohne dass die Karte im Detail analysiert werden muss. Der Titel enthält oft Informationen zum geografischen Ort, zum Thema oder zur Zeitspanne und ist meist prominent über oder in der Nähe der oberen Ecke der Karte platziert.

Der Kartenrahmen bildet den sichtbaren Bereich der Karte ab und trennt diese von anderen Elementen wie der Legende oder dem Titel. Er sorgt dafür, dass die Karte visuell isoliert und geordnet erscheint. Besonders bei Karten mit einem Raster sind die Koordinateninformationen entlang der Randlinien des Kartenrahmens vermerkt.

Die Hauptkarte ist das zentrale Element des Kartenlayouts und zeigt die geografischen Informationen, die auf der Karte dargestellt werden. Eine gut gestaltete Hauptkarte sollte klar und leicht verständlich sein. Sie kann verschiedene Ebenen wie physische Merkmale, politische Grenzen oder thematische Daten enthalten, abhängig vom Zweck der Karte.

Zusätzlich zur Hauptkarte kann eine Übersichtskarte eingefügt werden, die einen umfassenderen Blick auf die umliegende Region bietet. Diese Zusatzkarte dient der räumlichen Orientierung und zeigt die Lage des Hauptkartenausschnitts im Kontext der weiteren Umgebung.

Die Kartenlegende dient als Schlüssel für das Verständnis der verwendeten Symbole und Icons auf der Karte. Sie listet abstrahierte Darstellungen geografischer Objekte auf, wie etwa Symbole für Häuser oder Straßen, um dem Betrachter zu erklären, was die verschiedenen Darstellungen auf der Karte bedeuten.

Der Maßstabsindikator gibt das Verhältnis zwischen den Entfernungen auf der Karte und den tatsächlichen Entfernungen in der realen Welt an. Er kann als Leiste, Balken oder numerische Angabe dargestellt werden und hilft dem Betrachter, die Größe der dargestellten geografischen Merkmale zu verstehen.

Der Nordpfeil oder die Kompassrose zeigt die Hauptrichtungen auf der Karte an, insbesondere die Ausrichtung nach Norden. Ist die Karte nicht nach Norden orientiert, wird der Nordpfeil entsprechend gedreht, um die tatsächliche Ausrichtung anzuzeigen.

Zusätzliche Anmerkungen auf einer Karte können verwendet werden, um wichtige Informationen hervorzuheben, historische Hintergründe zu erläutern oder den Betrachter auf interessante Details aufmerksam zu machen. Quellenangaben sind ebenfalls ein wichtiges Element einer Karte, da sie die Glaubwürdigkeit und Genauigkeit der dargestellten Informationen belegen.

Für eine gute Strukturierung einer Karte ist es wichtig, eine visuelle Hierarchie der Elemente zu etablieren. Die wichtigsten Informationen wie die Hauptkarte, der Titel und die Legende sollten prominent platziert werden, während weniger relevante Elemente weiter unten angeordnet sein sollten. Textliche Informationen sollten kurz und prägnant gehalten werden, und es ist ratsam, die Anzahl der verwendeten Farben auf ein überschaubares Maß zu begrenzen, um die Lesbarkeit der Karte zu gewährleisten.

## 3. Übungen und Leitfäden

**Zusammenfassung des Inhaltes**
Wir werden uns mit dem Umgang der wichtigsten Funktionen der Benutzeroberfläche von ArcGIS Pro beschäftigen. Im Zuge dessen lernt ihr die Kartenansichten und -layer anzupassen. Außerdem werden wir bereits eine eigene kleine Karte über die Schulstandorte in Bochum erstellen, ausgestalten und exportieren.

## 3. Übungen und Leitfäden

# Modul 5 - Vektordatenanalyse
         	           	
## 1. Überblick

In diesem Modul tauchst du in die Welt der Vektordatenanalyse ein und lernst, wie Geographische Informationssysteme (GIS) diese spezielle Form der Datenverarbeitung nutzen. Du erhältst einen umfassenden Überblick über Vektordaten, die Anwendung verschiedener Analysetechniken sowie die Herausforderungen und Methoden der Vektordatenanalyse.

**Nachdem du die folgende OER abgeschlossen hast, wirst du wissen:**
* dass Vektordaten eine Form der räumlichen Darstellung sind, die aus Punkten, Linien und Polygonen besteht und diskrete geographische Objekte wie Straßen oder Grundstücke repräsentiert.
* die Grundlagen der Vektordatenanalyse, einschließlich der verschiedenen Methoden wie thematische, topologische und geometrische Abfragen.
* wie Werkzeuge in GIS, wie Buffer, Clip und Spatial Join, eingesetzt werden, um räumliche Beziehungen zu analysieren und komplexe geographische Fragestellungen zu bearbeiten.
* dass der Dijkstra-Algorithmus eine Schlüsseltechnik in der Netzwerkanalyse ist, die verwendet wird, um die kürzesten Wege in einem Netzwerk zu bestimmen.
* die Herausforderungen der Vektordatenanalyse, wie die Generalisierung und die damit verbundenen Genauigkeitsprobleme, sowie die Bedeutung der korrekten Datenverarbeitung und -interpretation.


## 2. Thematischer Hintergrund

### 2.1 Kurze Einführung
Die Vektordatenanalyse befasst sich mit der Verarbeitung und Analyse von geografischen Informationen, die in Form von Punkten, Linien und Polygonen dargestellt werden. Diese Art der Analyse nutzt Geoinformationssysteme (GIS) und fortschrittliche Analysetechniken, um geografische Muster zu erkennen und fundierte Entscheidungen in Bereichen wie Stadtplanung, Umweltmanagement und Transportwesen zu treffen. Zu den gängigen Anwendungen gehören die Netzwerkanalyse, bei der optimale Routen und Transportflüsse ermittelt werden, und die Standortanalyse, die potenzielle Standorte bewertet.

Vektordaten selbst repräsentieren die Geometrie von geografischen Merkmalen, wobei diese Daten mithilfe von GPS-Geräten oder durch Digitalisierung analoger Karten erfasst werden. Die Daten können dann in verschiedenen Formaten wie Shapefiles oder GeoJSON gespeichert und verarbeitet werden. Die Analyse dieser Daten erfordert spezielle Methoden und Werkzeuge, darunter GIS-Software wie ArcGIS und QGIS sowie räumliche Datenbanken, die für die effiziente Speicherung und Abfrage geografischer Informationen entwickelt wurden.

Zu den häufigsten Analysewerkzeugen gehören Methoden wie das Puffern, das Überlagern von Layern oder die räumliche Interpolation. Geoverarbeitungswerkzeuge ermöglichen es, neue Layer zu erstellen, indem bestehende Themen miteinander kombiniert oder ausgeschnitten werden. Dies ist besonders nützlich für Abfragen, bei denen geometrische, thematische oder topologische Kriterien genutzt werden, um bestimmte Informationen aus den Daten zu extrahieren, wie etwa die Lokalisierung von Supermärkten oder die Berechnung von Flächen und Entfernungen.

Die Vektordatenanalyse stößt jedoch auch auf Herausforderungen, wie unvollständige oder ungenaue Daten, die regelmäßige Aktualisierungen erfordern, sowie komplexe Analysen, die fortgeschrittene Kenntnisse in GIS-Techniken voraussetzen. Die Integration von Daten aus verschiedenen Quellen kann ebenfalls problematisch sein, insbesondere wenn unterschiedliche Formate verwendet werden. Die Verarbeitung großer Datenmengen erfordert leistungsstarke Hardware und optimierte Algorithmen, um die Analyse effizient durchzuführen.

Letztlich bietet die Vektordatenanalyse durch den Einsatz spezialisierter Algorithmen wie dem Ray-Casting- oder dem Dijkstra-Algorithmus die Möglichkeit, räumliche Beziehungen zu untersuchen und komplexe geografische Probleme zu lösen.

### 2.2 Inhaltliche Vertiefung
Geo

## 3. Übungen und Leitfäden

**Zusammenfassung des Inhaltes**
Wir werden uns mit dem Umgang der wichtigsten Funktionen der Benutzeroberfläche von ArcGIS Pro beschäftigen. Im Zuge dessen lernt ihr die Kartenansichten und -layer anzupassen. Außerdem werden wir bereits eine eigene kleine Karte über die Schulstandorte in Bochum erstellen, ausgestalten und exportieren.

## 3. Übungen und Leitfäden

# Modul 6 - Rasterdatenanalyse
         	           	
## 1. Überblick

In diesem Modul tauchst du in die Welt der Rasterdatenanalyse ein und erfährst, wie Geographische Informationssysteme (GIS) diese spezielle Form der Datenverarbeitung nutzen. Du erhältst einen grundlegenden Überblick über Raster, den Aufbau von Rasterdaten sowie die Anwendung von Rasterdatenanalyse und Interpolation.

**Nachdem du die folgende OER abgeschlossen hast, wirst du wissen:**
* dass Rasterdaten eine Form der räumlichen Darstellung sind, die in regelmäßigen Gittern oder Rasterzellen organisiert sind
* die Grundlagen des Rasteraufbaus, einschließlich der Struktur von Rasterzellen, ihrer Größe und Auflösung
* wie Rasterdatenanalysen in GIS eingesetzt werden, um komplexe geographische Phänomene zu untersuchen
* dass die Interpolation eine Schlüsseltechnik in der Rasterdatenanalyse ist. Du erfährst, wie dieses Verfahren genutzt wird, um fehlende Werte zwischen den vorhandenen Datenpunkten zu schätzen


## 2. Thematischer Hintergrund

### 2.1 Kurze Einführung

Die Präsentation gibt einen Überblick über die Rasterdatenanalyse und deren Bedeutung in der Geoinformatik. Rasterdaten sind georeferenzierte Informationen, die in einem regelmäßigen Gitter (Raster) organisiert sind. Jede Zelle des Rasters enthält einen numerischen Wert, der eine spezifische Information repräsentiert. Mehrere Schichten, sogenannte Bänder, können in einer Datei kombiniert werden, wobei jedes Band nur ein Attribut darstellen kann. Rasterdaten werden in vielen Bereichen eingesetzt, insbesondere zur Untersuchung geografischer Phänomene.

Ein wesentlicher Bestandteil der Präsentation ist die Erklärung der **Rasterdatenanalyse**, die sich auf die Verarbeitung und Analyse von Daten im Rasterformat stützt. Sie umfasst verschiedene Anwendungen:

1. **Analyse von Landnutzung und Bodenbedeckung**: Ermittlung von Mustern in der Landnutzung und Vegetationsverteilung.
2. **Untersuchung von Temperatur, Luftdruck und Klimawandel**: Analyse von Mustern und Trends, die helfen, klimatische Veränderungen zu verstehen.
3. **Erstellung von Höhenmodellen und Geländeanalyse**: Untersuchung von Hangneigungen und die Durchführung von Sichtbarkeitsanalysen.
4. **Dichtenanalyse**: Verwendung von Rasterdaten zur Analyse von Bevölkerungsdichten oder der Verteilung von anderen Objekten.
5. **Umweltüberwachung**: Überwachung von Luft- und Wasserqualität sowie die Beobachtung von Naturereignissen wie Waldbränden oder Überschwemmungen.

Ein weiterer Schwerpunkt der Präsentation liegt auf **Digitalen Höhenmodellen (DHM)**, die als digitale Repräsentationen der Erdoberfläche genutzt werden. Diese Modelle sind in der Regel in regelmäßigen Abständen geordnet und speichern Geländepunkte, die die Struktur der Erdoberfläche repräsentieren. Zwei Unterkategorien werden dabei vorgestellt:

- **Digitales Geländemodell (DGM)**: Eine spezielle Art von DHM, das die reine Geländeoberfläche ohne Vegetation und Bauwerke darstellt. Es wird vor allem zur topografischen Analyse genutzt, um Merkmale wie Höhenzüge, Täler und Gipfel zu identifizieren.
- **Digitales Oberflächenmodell (DOM)**: Dieses Modell enthält zusätzlich zur Erdoberfläche auch künstliche und natürliche Objekte wie Gebäude und Vegetation. Es ermöglicht eine detailliertere Analyse der Oberflächenstrukturen.

Insgesamt betont die Präsentation die Bedeutung von **Rasterdaten** und **Höhenmodellen** in der Geoinformatik, insbesondere für Anwendungen in der Stadtplanung, Umweltüberwachung, Geowissenschaften und dem Katastrophenmanagement.

### 2.2 Inhaltliche Vertiefung 1
die Interpolation als ein mathematisches Verfahren erklärt, bei dem Werte zwischen bekannten Datenpunkten geschätzt werden, um kontinuierliche Funktionen oder Kurven zu erstellen. Diese Methode wird genutzt, um fehlende Daten zu ergänzen oder glattere Darstellungen von diskreten Datensätzen zu erhalten, indem neue Werte berechnet werden, die einen zugrunde liegenden Trend repräsentieren.

Ein Problem bei der Datenerfassung ist, dass es unmöglich ist, überall Messungen durchzuführen. Als Lösung werden Stichproben genommen, aber es bleibt die Frage offen, was mit den Orten passiert, an denen keine Messungen gemacht wurden. Hier greift das Prinzip der Interpolation, das auf Toblers erstem Gesetz der Geographie basiert: „Alles hängt mit allem zusammen, aber nahe Dinge sind stärker miteinander verbunden als entfernte Dinge.“

Die Geschichte der Interpolation reicht weit zurück und findet sich in antiken Kulturen wie bei den Babyloniern und Ägyptern, die Methoden entwickelten, um fehlende Daten zu schätzen. In Griechenland beschäftigten sich Mathematiker wie Euklid und Archimedes mit der geometrischen Interpolation. Später, im 17. Jahrhundert, legten Newton und Fermat wichtige Grundlagen für die Entwicklung moderner Interpolationsmethoden.

Das Grundprinzip der räumlichen Interpolation ist, ein Raster über ein Untersuchungsgebiet zu legen und für jede Rasterzelle den Wert anhand eines gewichteten Mittels der umliegenden Messungen zu schätzen. Ein Beispiel für dieses Verfahren wird anhand von Wetterstationen erklärt. Wenn zwei Wetterstationen unterschiedliche Temperaturen messen, kann die Temperatur eines Punktes zwischen diesen Stationen durch lineare Interpolation berechnet werden.

Es gibt verschiedene Interpolationsmethoden, darunter deterministische Methoden wie Nearest Neighbour und Inverse Distance Weighting (IDW) sowie statistische Methoden wie Spline und Kriging. Jede Methode verwendet einen Algorithmus, um die Werte zwischen bekannten Datenpunkten zu schätzen und eine kontinuierliche Darstellung des betrachteten Phänomens zu erzeugen.

Die Nearest Neighbour Methode geht davon aus, dass der Wert an einer Stelle ohne Messung dem Wert des nächstgelegenen Referenzpunkts entspricht, während IDW den Einfluss der benachbarten Stationen auf den Schätzwert je nach Distanz abnimmt. Splines werden verwendet, um geglättete Oberflächen zu erstellen, indem sie polynomiale Funktionen nutzen, während Kriging die statistische Verteilung von Messwerten über eine Fläche modelliert und lokale Variationen berücksichtigt.

### 2.2 Inhaltliche Vertiefung 2
Map Algebra, ein von Charles Dana Tomlin in den 1980er Jahren entwickeltes Konzept, ist ein leistungsstarkes Werkzeug zur Analyse und Verarbeitung von Rasterdaten. Es kombiniert grundlegende mathematische Operationen wie Addition, Subtraktion, Multiplikation und Division, um komplexe räumliche Berechnungen durchzuführen, die Einblicke in geografische Phänomene ermöglichen und Entscheidungsprozesse, wie in der Umweltplanung oder im Katastrophenmanagement, unterstützen.

Ein wesentlicher Aspekt von Map Algebra ist die Arbeit mit verschiedenen Operationstypen. Die lokale Operation arbeitet an einzelnen Rasterzellen, wobei die Ausgabewerte auf den Werten derselben Zelle in zwei oder mehr Eingaberastern basieren. Benachbarte Zellen beeinflussen das Ergebnis nicht. Eine andere wichtige Methode ist die fokale Operation, bei der nicht nur die Zellen, sondern auch deren Nachbarschaft berücksichtigt werden, um die Werte im Ausgaberaster zu berechnen. Diese Operation ist nützlich bei der Berechnung von Glättungen oder der Analyse räumlicher Muster, bringt jedoch potenzielle Kanteneffekte mit sich.

Zonale Operationen hingegen berechnen Werte basierend auf allen Zellen innerhalb einer vordefinierten Zone, wobei Zonen nicht zusammenhängend sein müssen. Diese Technik wird verwendet, um Variationen innerhalb bestimmter geografischer Regionen zu untersuchen. Schließlich gibt es die globale Operation, die alle Zellen des Eingaberasters einbezieht. Ein Beispiel dafür ist die Erstellung einer „Cost Surface“, die die Entfernung zur nächstgelegenen Quelle angibt und oft in Wegfindungsalgorithmen verwendet wird.

Ein weiteres bedeutendes Anwendungsfeld in der Kartographie ist das Digitale Höhenmodell (DHM). Es ermöglicht die Analyse der Änderung von Oberflächenrichtungen und Neigungen. Der „Slope“-Wert gibt die Hangneigung an, die über eine einfache mathematische Formel berechnet wird und nützliche Informationen für das Management von Hangrutschungsgefahren oder Entwässerungssystemen bietet. Je dichter die Höhenlinien einer Karte angeordnet sind, desto steiler ist das Gelände.

Die „Aspect“-Analyse misst die Ausrichtung des Hangs, also die Richtung, in der die größte Steigung auftritt. Diese wird im Uhrzeigersinn gemessen, beginnend bei 0° für Norden bis hin zu 360°. Anwendungen wie die Solarpotentialberechnung profitieren von dieser Methode, da sie die optimale Ausrichtung von Flächen bestimmen kann.

Schließlich bietet die Hillshade-Analyse eine detaillierte Berechnung des Schattenwurfs auf der Oberfläche. Diese wird auf der Grundlage des Azimuts (der Winkelrichtung der Lichtquelle) und der Höhe (dem Winkel der Lichtquelle über dem Horizont) berechnet. Diese Technik verleiht Karten eine realistische 3D-Optik und hilft dabei, Geländeformen besser zu erkennen und darzustellen.

Zusammenfassend lässt sich sagen, dass Map Algebra und die zugehörigen Operationen sowie das Digitale Höhenmodell grundlegende Werkzeuge für die Analyse und Visualisierung von geografischen Daten sind, die in verschiedenen Anwendungsbereichen wie der Umweltplanung, dem Katastrophenmanagement oder der topografischen Analyse von Geländen eingesetzt werden können.

## 3. Übungen und Leitfäden

**Zusammenfassung des Inhaltes**
Wir werden uns mit dem Umgang der wichtigsten Funktionen der Benutzeroberfläche von ArcGIS Pro beschäftigen. Im Zuge dessen lernt ihr die Kartenansichten und -layer anzupassen. Außerdem werden wir bereits eine eigene kleine Karte über die Schulstandorte in Bochum erstellen, ausgestalten und exportieren.

# Dein Feedback ist willkommen!

Wenn du Defizite in diesem OER-Modul festgestellt hast oder Ideen zur Verbesserung des OER-Materials hast, bist du herzlich eingeladen, Einträge in die Issue-Liste ([https://github.com/oer4sdi/OER-Fernerkundung]) vorzunehmen.
