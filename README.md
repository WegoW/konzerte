# Konzerte, ganz nach meinem Musikgeschmack

Statische Übersicht mit 106 Konzerten aus den öffentlich-rechtlichen Mediatheken,
quer durch Funk, Soul, Jazz und die eine oder andere Legende.

Ein Klick lädt die Datei, benannt als `Interpret - Titel (Jahr).mp4`. Mehrere
Zeilen lassen sich anhaken und nacheinander herunterladen, im Chrome oder Edge
landet alles direkt in einem vorher gewählten Ordner.

## Aufbau

| Datei | Zweck |
|---|---|
| `index.html` | die komplette Seite, Daten inline, keine externen Abhängigkeiten |
| `items.json` | dieselben Daten als JSON |

Es gibt keinen Server. Der Download läuft im Browser, der die Datei per `fetch`
holt und über die File System Access API auf die Platte streamt. Wo die fehlt
(Safari, Firefox), geht es über einen Blob.

## Woher die Daten kommen

MediathekView, also die Such-API über `https://mediathekviewweb.de/api/query`.
Gefiltert auf ganze Sendungen ab 25 Minuten, Rauschfilter gegen Talkshows und
Namensvettern, Dubletten aus ARD, 3sat, BR und SRF zusammengefasst.

## Ehrlicher Hinweis

Die Links sind Direkt-URLs der Sender. Die Mediatheken räumen regelmäßig ab,
ein Link kann also irgendwann ins Leere laufen. Dann hilft der Link „ansehen“,
der auf die originale Mediathek-Seite führt. Die Liste ist eine Momentaufnahme.

Alle Inhalte gehören den jeweiligen Sendern. Das hier ist eine private
Merkliste, kein Archiv und kein Angebot.
