
## Prozesse vs Threads

###### (Für weiteres einfach die anderen Dateien lesen)


Prozesse sind unabhängige Programme mit ihrem eigenen Speicher, Threads sind kleine Teile eines Prozesses. Sie werden verwendet um mehrere Aufgaben schnell und effektiv zu bearbeiten und dabei die Leistung nicht beeinträchtigen. 

#### Unterschiede: 
- **Erstellen/Beenden:** Prozesse brauchen länger, Threads sind scheller.  
- **Context Switching:** Threads schneller als Prozesse.  
- **Kommunikation:** Prozesse kommunizieren weniger effektiv.  
- **Blocking:** Ein blockierter Prozess beeinflusst nicht andere Prozesse, ein blockierter Thread kann alle anderen Threads blockieren.
