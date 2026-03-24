# Übersicht zu Gemeinsamen Ressourcen

Die gemeinsame Nutzung von Ressourcen (Resource Sharing) ist eine der Kernaufgaben eines modernen Betriebssystems. Ohne ein intelligentes Management würden Prozesse kollidieren, Daten korrumpieren oder das gesamte System zum Stillstand bringen.Die gemeinsame Nutzung von Ressourcen (Resource Sharing) ist eine der Kernaufgaben eines modernen Betriebssystems. Ohne ein intelligentes Management würden Prozesse kollidieren, Daten korrumpieren oder das gesamte System zum Stillstand bringen.

## 5.3 Nutzung gemeinsamer Ressourcen

**Das Erzeuger-Verbraucher-Problem:**

- Ein Erzeuger produziert Daten oder Objekte und legt sie in einem Zwischenspeicher ab.
- Ein Verbraucher entnimmt diese Objekte aus dem Speicher.
- Problematik: Wenn der Speicher voll ist, kann der Erzeuger nichts ablegen; ist er leer, kann der Verbraucher nichts entnehmen. Ohne Absprache verschwenden die Threads Zeit durch aktives Warten (Busy Waiting), indem sie ständig prüfen, ob der Speicher bereit ist.

**Lösung durch passives Warten:**

- Anstatt ständig zu prüfen, wird ein Thread in einen Wartezustand versetzt (Warten()), wenn die Bedingung (z. B. Speicher voll) nicht erfüllt ist.
- Sobald sich der Zustand ändert (z. B. Verbraucher hat Platz geschaffen), wird der wartende Thread informiert (Benachrichtigen()).
- Dies wird oft durch Monitore oder Semaphore realisiert.

**Das Leser-Schreiber-Problem:**

- Hier greifen zwei Arten von Threads auf Daten (z. B. eine Datenbank) zu.
- Regeln: Beliebig viele Leser dürfen gleichzeitig zugreifen, da sie Daten nicht verändern. Ein Schreiber benötigt jedoch exklusiven Zugriff; während er schreibt, darf niemand sonst lesen oder schreiben, um Inkonsistenzen zu vermeiden.
- Es müssen Strategien entwickelt werden, damit z. B. Schreiber nicht durch einen stetigen Strom an Lesern „verhungern“.

## 5.4 Deadlocks

**Das Problem der Speisenden Philosophen:**

- Fünf Philosophen sitzen an einem Tisch; jeder benötigt zwei Gabeln zum Essen, hat aber nur eine Gabel links und eine rechts von sich.
- Wenn jeder gleichzeitig die linke Gabel aufnimmt, wartet jeder ewig darauf, dass die rechte Gabel frei wird. Es entsteht ein zyklisches Warten.

Die **vier Coffman-Bedingungen** für Deadlocks: Damit eine Verklemmung überhaupt entstehen kann, müssen vier Bedingungen gleichzeitig erfüllt sein.

**Strategien zur Vermeidung**: Um Deadlocks zu verhindern, muss mindestens eine der Coffman-Bedingungen gezielt außer Kraft gesetzt werden.
