# Betriebsmittelzuteilungsgraphen

sind Graphen, die visualisieren, welche Threads welche Ressourcen belegen bzw. angefordert haben. Dabei können Verklemmungen(Deadlocks) im Falle einer zyklischen Konstellation leicht erkannt werden.

## Bestandteile


| Thread | Ressource | Belegung | Anforderung |
| ------ | --------- | -------- | ----------- |
| ![](Bilder/B-Thread.png) <br> Runde Ecken/Kreis| ![](Bilder/B-Ressource.png) <br> Rechteck| ![](Bilder/B-Belegung.png) | ![](Bilder/B-Anforderung.png) <br> Auch als gestrichelter Pfeil möglich|

![fail](Bilder/B-Beispiel.png)
Je nach Ausführung der Prozesse kann dabei eine zyklische Wartesituation entstehen, die auf einen Deadlock visualisiert.

| Ausführung mit Deadlock | Ausführung mit Deadlock |
| ----------------------- | ----------------------- |



