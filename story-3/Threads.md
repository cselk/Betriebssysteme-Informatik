## Threads
#### *Was sind Threads?*
Ein Thread ist eine einzelne Sequenz in einem Prozess, es wird auch lightweight process genannt da es kleiner und schneller ist als ein Prozess. 


#### *Wieso brauchen wir sie?*
- Bessere Performance: Mehrere Tasks können gleichzeitig ausgeführt werden (parallel oder interleaved)
- Gleichzeitigkeit (Concurrency): Operationen können gleichzeitig erfolgen (data processing, datein speichern und user action)
- Bessere CPU verwendung: Threads können auf verschiedene cores aufgeteilt werden
- Resource Sharing: Threads teilen innerhalb eines Prozesses Memory was die geschwindigkeit erhöht


#### *Components/Attributes*
- Stack Space: Speichert lokale Variablen, Funktionsaufrufe und Rückgabeadressen des Threads.
- Register Set: Speichert temporary data und zwischenergebnisse 
- Programm Counter 


#### *Arten von Threads*
Es wird grundsätzlich in zwei Arten von Threads unterteilt, User Level Threads (ULTs) und Kernel Level Threads (KLTs). 

**Thread libraries**: Thread libraries sind APIs die entweder im Userspace (-level) oder im Kernalspace implementiert sind. Sie kontrollieren den multithread prozess damit man das nicht selber manuel machen muss.

##### *ULTs*
Werden in dem User-Level durch eine Thread Library verwaltet und sind schneller als KLTs. Werden verwendet wenn präzise Kontrolle über multithreading gewünscht ist aber der overhead von KLTs nicht. Alle Threads sind im gleichen Prozess untergebracht. 

**+** Kann in Systemen verwendet werden die keine native multithreading anbieten. 

**-** Eine blockierende Operation kann den gesamten Prozess anhalten. Kann tendenziell nicht mehrere cores verwenden.  

##### *KLTs*
Werden direkt vom kernel (und kernel level thread libraries) gemanaged. Dadurch das der kernel das handelt, kann ein besseres Sceduling geschehen und es kann über mehrere Prozessoren verteilt werden. 

**-** Context switching ist langsamer im Vergleich zu ULTs. 



