# Hackerspace of Things
C3MA Raum Automatisierung


#Installation Dokumentation NodeRed
Raspberry mit Raspberian drauf, hostname "nodered"
Installation via script von https://nodered.org/docs/getting-started/raspberrypi

Es existiert keine langzeit db by design, es soll nicht möglich sein Daten nachträglich zu analysieren, dh. es werden die standart Graphen verwendet, 
welche pro graph in der persistens nur daten halten, die auch angezeigt werden. Eg. beim stromverbrauch werden nur die letzten 1-2 Stunden gespeichert, ältere Daten werden absichtlich verworfen

MQTT server ist 10.23.42.10
IpAdresse auf 10.23.42.11 stellen, evtl etc/hosts datei im routerpi dazu anschauen

nginx installieren via apt
im var/www auf der default index einen redirect auf nodered:1880 hinzufügen

uhr muss funktionieren und gesynct sein sonst graphen kaputt und tag nacht erkennung

settings.json anpassen der flows.json auf location von usb stick

git config --global user.email "pi@nodered"
git config --global user.name "Nodered"

# Recovery
Vom github backup die flows_nodered.json über import dialog reinladen, fehlende nodes via palette nachinstallieren



