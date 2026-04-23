# Betriebsmittelzuteilungsgraphen

sind Graphen, die visualisieren, welche Threads welche Ressourcen belegen bzw. angefordert haben. Dabei können Verklemmungen(Deadlocks) im Falle einer zyklischen Konstellation leicht erkannt werden.

## Bestandteile

![](https://www.google.com/imgres?q=geek%20for%20geeks%20deadlocks&imgurl=https%3A%2F%2Fmedia.geeksforgeeks.org%2Fwp-content%2Fuploads%2F20241003170604%2FScreenshot-2024-10-03-170601.png&imgrefurl=https%3A%2F%2Fwww.geeksforgeeks.org%2Foperating-systems%2Fintroduction-of-deadlock-in-operating-system%2F&docid=-M0x9HJrEDuqaM&tbnid=EuhRzXhYyADyfM&vet=12ahUKEwi6oL2z24OUAxU5wQIHHV0wODIQnPAOegQIGxAB..i&w=322&h=327&hcb=2&ved=2ahUKEwi6oL2z24OUAxU5wQIHHV0wODIQnPAOegQIGxAB)

| Thread | Ressource | Belegung | Anforderung |
| ------ | --------- | -------- | ----------- |
| 
