## Scheduling Strategien 

### **Round Robin**
In der Round Robin Scheduling Strategie rotiert das System (OS) durch jeden anstehenden Prozess und gibt ihnen allen die gleiche Anzahl an Zeit, genannt *Quantum Time*, zur Verfügung. Dabei wird nicht auf Priorität geachtet. 

#### Beispiel 1: Prozesse mit gleichzeitigem Ankommen
| Process | Burst Time | Arrival Time |
|---------|------------|--------------|
| P1 | 4 ms | 0 ms |
| P2 | 5 ms | 0 ms |
| P3 | 3 ms | 0 ms |
