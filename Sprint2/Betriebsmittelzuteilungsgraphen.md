# Betriebsmittelzuteilungsgraphen

sind Graphen, die visualisieren, welche Threads welche Ressourcen belegen bzw. angefordert haben. Dabei können Verklemmungen(Deadlocks) im Falle einer zyklischen Konstellation leicht erkannt werden.

## Bestandteile

![fail](Bilder/B-Beispiel.png)

| Thread | Ressource | Belegung | Anforderung |
| ------ | --------- | -------- | ----------- |
| ![](Bilder/B-Thread.png) <br> Runde Ecken/Kreis| ![](Bilder/B-Ressource.png) <br> Rechteck| ![](Bilder/B-Belegung.png) | ![](Bilder/B-Anforderung.png) <br> Auch als gestrichelter Pfeil möglich|
