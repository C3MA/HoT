# Hackerspace of Things
C3MA Raum Automatisierung


#Installation Dokumentation NodeRed
Raspberry mit Raspberian drauf, hostname "nodered"
Installation via script von https://nodered.org/docs/getting-started/raspberrypi
Es existiert keine langzeit db by design, es soll nicht möglich sein Daten nachträglich zu analysieren, dh. es werden die standart Graphen verwendet, 
welche pro graph in der persistens nur daten halten, die auch angezeigt werden. Eg. beim stromverbrauch werden nur die letzten 1-2 Stunden gespeichert, ältere Daten werden absichtlich verworfen


MQTT server ist 10.23.42.10

#Regeln vom alten openhab:
Wenn LightBox Wand über 42Grad, wand abschalten um schäden zu verhindern
Wenn Sonnenauf bzw. Untergang dann $Darkness_Contact
Wenn $beamerinput auf an, dann screen auf down, lampe 1 aus, kühlschrank aus
Wenn $beamerinput auf aus, dann lampe1 wieder an, 45sec warten, screen hoch und beamer aus
-> Wenn Repman an oder fertig, TLblinkGreen aus, oder blinken?

Wenn Türschloss von offen auf geschlossen, lichter aus, pushmessage -> "Der C3MA Raum wurde abgeschlossen!"
Wenn Türschloss von geschlossen auf offen, dann fenster plug an, wall plug an und wenn nach sonnenuntergang licht hauptraum an, pushmessage -> "Der C3MA Raum wurde geöffnet!"

Wenn mehr als 20 wlan clients, kühlschranklicht an
Wenn weniger als 10 wlan clients, kühlschranklicht aus

#Alle MQTT adressen via MQTTExplorer reverse engineered, da einfacher als das openhab binding nachzubauen

