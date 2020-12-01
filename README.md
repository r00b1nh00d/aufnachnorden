# Auf geht's nach Norden
## ~avatar avatar @unplugged
In der Nachricht vom Weihnachtsmann schrieb er, dass er deine Hilfe am Nordpol bräuchte. Aber wie sollst du dorthin kommen?

## ~ @unplugged 
Du kannst den Calliope zu einem Kompass programmieren, er wird dir helfen, den Weg Richtung Norden zu finden.


## Schritt 1
Erstelle eine Variable namens ``||variables:Richtung||``. In der ``||basic:dauerhaft||`` - Schleife soll die ``||input:Kompassausrichtung||`` zuerst auf die Variable ``||variables:Richtung||`` gespeichert werden. Anschließend soll in einer ``||logic: wenn - dann||`` -  Bedingung überprüft werden, in welche Richtung der Calliope zeigt. <br>
Bei einem Wert < 45 soll N für Norden angezeigt werden. <br>
Bei einem Wert < 135 soll O für Osten angezeigt werden. <br>
Bei einem Wert < 225 soll S für Süden angezeigt werden. <br>
Bei einem Wert < 315 soll W für Westen angezeigt werden. <br>
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
