# Einführung

_RedMatic_ fasst mehrere Softwarekomponenten zu einem CCU Addon zusammen, einem Softwarepaket, dass auf einer Homematic 
CCU3 oder RaspberryMatic als Zusatzsoftware komfortabel über das WebUI installiert werden kann.

Die Grundlage bildet [Node-RED](https://nodered.org/about/) mit den 
[CCU Nodes für Node-RED](https://github.com/HM-RedMatic/node-red-contrib-ccu). Hiermit ist es auf einfache, visuelle 
Weise möglich Regeln, Automationen, Scripte und Anbindungen von externen Services und Systemen für ein Homematic System 
zu realisieren - und das weitgehend auch ohne Programmierkenntnisse. Im 
[Wiki](https://github.com/HM-RedMatic/RedMatic/wiki) gibt es weitere Informationen zu Node-RED und einige 
Anwendungsbeispiele (sogenannte _Flows_).

Für die Visualisierung und Steuerung sind [RedMatic WebApp](https://github.com/HM-RedMatic/RedMatic-WebApp) und 
[Node-RED Dashboard](https://github.com/node-red/node-red-dashboard) enthalten. _RedMatic WebApp_ ist eine
Bedienoberfläche die ohne weitere Konfiguration sofort genutzt werden kann (vergleichbar mit _WebMatic_ oder _Yahui_).
_Node-RED Dashboard_ ist ein konfigurierbares User Interface, kann mehr Möglichkeiten als die _RedMatic WebApp_ bieten, 
ist aber mit Konfigurationsaufwand verbunden. 
Beispiel Screenshots: [RedMatic WebApp](https://github.com/HM-RedMatic/RedMatic/wiki/Webapp), 
[Node-RED Dashboard](https://github.com/HM-RedMatic/RedMatic/wiki/Dashboard-Screenshots).

Außerdem ist es mit der ebenfalls enthaltenen Erweiterung 
[RedMatic HomeKit](https://github.com/HM-RedMatic/RedMatic/wiki/Homekit) möglich Homematic Geräte und andere in Node-RED 
verfügbare Systeme über Siri und mit HomeKit-Apps anzusteuern.

Eine Anbindung der CCU an einen [MQTT](https://github.com/HM-RedMatic/RedMatic/wiki/Flow-MQTT) Broker mit komfortabel 
konfigurierbarer Topic- und Payload-Struktur wird durch einen speziellen Node vereinfacht.

Eine große und aktive Community rund um Node-RED hat zudem eine 
[Bibliothek von tausenden zusätzlichen Nodes](https://flows.nodered.org/?type=node&num_pages=1) geschaffen die auf 
einfache Weise [installiert werden können](https://github.com/HM-RedMatic/RedMatic/wiki/Node-Installation) und es 
ermöglichen spezielle Automatismen zu implementieren und diverse weitere Services und Systeme komfortabel anzubinden - 
wie z.B. das Xiaomi Aqara Smart Home System, Loxone, den Logitech Harmony Hub, verschiedene Smart TVs und AV-Receiver, 
Sonoff, Hue, Lightify, Tradfri, ArtNET/DMX, Modbus, Amazon Alexa, Google Home, diverse Datenbanken wie z.B. InfluxDB 
oder MySQL, Webservices zur Abfrage von beispielsweise Wetterdaten und vieles mehr.

_RedMatic_ kann damit - insbesondere für diejenigen die neben der CCU keinen weiteren Server betreiben möchten - eine 
Alternative zu einem "ausgewachsenen" Smart Home System wie z.B. ioBroker, Home Assistent, OpenHAB oder FHEM darstellen. 
Für die Automatisierung eines Homematic Systems kann _RedMatic_ auch als Alternative oder Ergänzung für "Rega" 
Programme/Scripte dienen. 


## Voraussetzungen

_RedMatic_ ist __nur für die CCU3 und RaspberryMatic geeignet__. Da RedMatic unter Umständen über 100MB Speicher 
benötigt ist es ratsam einen RaspberryPi mit 1GB RAM zu nutzen (ab Pi 2B). Auf der CCU1/2 kann _RedMatic_ nicht 
direkt verwendet werden.

Für die Nutzung der Weboberflächen ist ein moderner Browser notwendig, der Internet Explorer wird nicht unterstützt.

Das Kernstück von _RedMatic_ ist `node-red-contrib-ccu` was die CCU Nodes für Node-RED zur Verfügung stellt.
Sie lassen sich, wie auch andere Nodes, 
[zu einer bestehenden Node-RED Installation hinzufügen](RedMatic/01_installation.html#deinstallation),
die beispielsweise auf einem zweiten RaspberryPi läuft.


## Schnellstart

Unter [Releases](https://github.com/HM-RedMatic/RedMatic/releases/latest) steht die Datei `redmatic-<version>.tar.gz` 
zum Download zur Verfügung. Nach der Installation des Addons über das Homematic WebUI (Systemsteuerung -> 
Zusatzsoftware) und dem darauf folgenden Reboot der CCU ist Node-RED unter `http://<ccu-addresse>/addons/red` 
erreichbar. Bei der Installation ist Geduld erforderlich, es kann bis zu ~10 Minuten dauern. Einige Beispiel-Flows sowie
ein einfaches Dashboard sind bereits vorkonfiguriert, das Dashboard ist unter `http://<ccu-addresse>/addons/red/ui` 
erreichbar.



