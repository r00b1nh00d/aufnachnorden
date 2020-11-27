# Auf geht's nach Norden
## ~avatar avatar @unplugged
In der nachricht vom Weihnachtsmann schribe er, dass er deine Hilfe am Nordpol brauch. Aber wie sollst du dort hin kommen?

## ~ @unplugged 
Du kannst den Calliope zu einem Kompas programmieren. Er wird dir helfen der Weg richtung Norden zu finden.


## Schritt 1
Erstelle eine Variable namens ``||variable:Richtung||``. In der ``||basic:dauerhaft||`` - Schleife soll die ``||inputs:Kompasausrichtung||`` zuerst auf die Variable ``||variable:Richtung||`` gespeichert werden. Anschließend soll in einer ``||logic: wenn - dann||`` -  Bedingung überrüft werden in welche Richtung der Calliope zeigt. <br>
Bei einem Wert < 45 Soll N für Norden angezeigt werden. <br>
Bei einem Wert < 135 Soll O für Osten angezeigt werden. <br>
Bei einem Wert < 225 Soll S für Süden angezeigt werden. <br>
Bei einem Wert < 315 Soll W für Westen angezeigt werden. <br>
Ansonsten soll wieder Norden gezeigt werden.
```blocks
let Richtung = 0
basic.forever(function () {
    Richtung = input.compassHeading()
    if (Richtung < 45) {
        basic.showString("N")
    } else if (Richtung < 135) {
        basic.showString("O")
    } else if (Richtung < 225) {
        basic.showString("S")
    } else if (Richtung < 315) {
        basic.showString("W")
    } else {
        basic.showString("N")
    }
})
```
