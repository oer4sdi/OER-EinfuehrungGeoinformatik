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
Die

### 2.2 Inhaltliche Vertiefung 
Geo

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
Die

### 2.2 Inhaltliche Vertiefung 
Geo

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
Die

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
Die

### 2.2 Inhaltliche Vertiefung 
Geo

## 3. Übungen und Leitfäden

**Zusammenfassung des Inhaltes**
Wir werden uns mit dem Umgang der wichtigsten Funktionen der Benutzeroberfläche von ArcGIS Pro beschäftigen. Im Zuge dessen lernt ihr die Kartenansichten und -layer anzupassen. Außerdem werden wir bereits eine eigene kleine Karte über die Schulstandorte in Bochum erstellen, ausgestalten und exportieren.

# Dein Feedback ist willkommen!

Wenn du Defizite in diesem OER-Modul festgestellt hast oder Ideen zur Verbesserung des OER-Materials hast, bist du herzlich eingeladen, Einträge in die Issue-Liste ([https://github.com/oer4sdi/OER-Fernerkundung]) vorzunehmen.
