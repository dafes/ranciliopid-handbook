---
layout: default
title: Einbau
parent: Hardware
grand_parent: DE - Handbuch
has_children: false
nav_order: 3
---

#   {{ page.title }}

<details open markdown="block">
  <summary>
    Inhaltsverzeichnis
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

Grundsätzlich würde ich alle Kabel erstmal mit einer Kabellänge von ca. 60 cm abschneiden. Nach dem Einbau auf Seite 1 und dem Verlegen sollten diese beim Anschließen an Seite 2 gekürzt werden.

Vorbereitung:
* ESP bespielen (ggf. sicherstellen, dass das WLAN funktioniert)
* PCB zusammenlöten (Link zur Anleitung folgt)
* ggf. Blynk einrichten und verbinden
* ggf. Displayhalter drucken / bestellen

Zeitaufwand:
* PID Only ca. 3 h
* Vollaubau weitere 2-3 h

## Zerlegen

Als erstes muss die Maschine zerlegt werden. Hier findet ihr einen [Link zur Demontage](https://clevercoffee.de/rancilio-silvia-demontage/).

## PID only

### Thermostat gegen Temperatursensor tauschen

Kabel (0,14mm2) am Temperatursensor anlöten und mit Schrumpfschlauch versehen. **!!!Unbedingt Pinbelegung beachten!!!** Es empfiehlt sich folgende Belegung zu verwenden:

> Rot = +  
> Schwarz = -  
> Grüne = Signal

Freies Kabelende beschriften

Stecker mit rotem Kabel und Stecker mit grauem Kabel abziehen.

Schrauben 1 + 2 lösen.
Schraube 3 ein wenig lockern.
Das alte Thermostat beiseite legen und aufheben; bereich von der Wärmeleitpaste reinigen.

Bügel mit Schraube, Beilagscheiben und Muttern vorbereiten. Bügel wieder einbauen dabei Schraube 3 und 2 festziehen, 1 noch etwas locker lassen.

Die neue Schraube mit Hilfe der zwei Muttern so einstellen, dass die Schraube auf dem Temperatursensor aufliegt. Muttern festziehen.
Temperatursensor auf der Unterseite mit etwas Wärmeleitpaste versehen, unter der neuen Schraube platzieren und Schraube 1 anziehen. Der Bügel sollte sich dabei leicht verformen. So wird sichergestellt, dass der Sensor fest sitzt, aber nicht zu sehr gequetscht wird.  


### Stromversorgung

1,5mm2 Kabel blau mit Flachsteckhülse mit Abzweig versehen und in den abgezogenen Stecker mit Rotem Kabel stecken.
Ein weiteres 1,5mm2 Kabel blau mit Flachstecker versehen und ebenfalls einstecken. Alles mit einem Schrumpfschlauch versehen.
Kabel eins geht zum SSR der Heizung, Kabel zwei zum Netzteil. Welches Kabel dabei wofür verwendet wird ist egal.

1,5mm2 Kabel schwarz mit Flachsteckhülse mit Abzweig versehen. Den unteren Stecke am Schutzschalter abziehen, auf den Abzweig stecken und beides direkt wieder anstecken.

Kabel sinnvoll verlegen und einen Platz für das Netzteil festlegen. Kabel vor dem anschließen entsprechend kürzen.

Am Netzteil ein blaues Kabel und ein schwarzen Kabel anschließen / anlöten. Wird das Schaltnetzteil aus der Bestellliste verwendet, das schwarze Kabel an N anschließen und das blaue Kabel an L anschließen. Es empfiehlt sich hierfür die Ringösen zu verwenden. Zusätzlich muss hier noch ein Schutzleiter verlegt werden. Dieser lässt sich an der Erdung des Kessels oder des 3-Wege Ventils "klauen". Vor dem Einbau die Ausgangsspannung am Poti prüfen und ggf. auf ca. 5.2V verstellen.

Am Ausgang ein Rotes und ein schwarzes Kabel anbringen. Ich habe dafür 0,5 mm2 Kabel verwendet, die 0,14 mm2 sollten aber auch reichen. Die beiden Kabel richtung 3-Wege Ventil legen und beschriften.

### SSR Relais Heizung

Montagepunkt für das SSR festlegen. Es kann bei der Rancilio Silvia E z.B. über der "CPU" neben dem Wasserschlauch mit doppelseitigem Klebeband angebracht werden. Alternativ befindet sich eine Schraube an der Vorderseite der Maschine (hinter der Abdeckung), auf die das SSR mit einer Mutter festgeschraubt werden kann.

An Kabel 2 (blau) des Schrittes oben, eine Ringöse pressen (Kabel vor dem Anschließen entsprechend kürzen) und an einen beliebigen Pol des SSR-Ausgangs anschließen.
Ein weiteres Kabel 1,5 mm2 mit einer Ringöse versehen und am zweiten Pol des SSR-Ausgangs befestigen. Kabel zum Stecker mit dem grauen Kabel verlegen, welches ursprünglich am Thermostat war und entsprechend kürzen. Einen Flachstecker aufpressen und anschließend mit einem Schrumpfschlauch versehen.

Zwei Kabel (rot und schwarz) an der Eingangsseite des SSR anschließen. Ich habe dafür 0,5 mm2 Kabel verwendet und ebenfals Ringösen aufgepresst. Es können aber auch die 0,14 mm2 Kabel mit Aderendhülsen o.ä. verwendet werden.
Freie Kabelenden beschriften und richtung 3-Wegeventil legen.

### Einbau des Controllers

Der Microcontroller (ESP) sollte auf das von uns bereitsgestellte Adapterboard (PCB) gesteckt werden. Dieses kommt mit Klebefüßen, so dass es an einer beliebigen günstigen Position befestigt werden kann, an der die Kabel zusammenlaufen. Dies kann im hinteren oder vorderen Teil der Maschine sein, je nach Modell.

## Vollausbau

**Wichtig!: Beim anschließen des Brühschalters bitte unbedingt den Hinweis im Schaltplan zur Trennung von 230V und 3.3/5V am Schalter beachten.**

folgt (so lange können aber die Bauberichte studiert werden)

## Display

Es gibt unzählig viele Möglichkeiten das Display zu positionieren. Folgend könnt ihr zwei Beispiele sehen:

Displayhalterung | Powered by Dremel
:---:|:---:
![Display](../../img/Display.jpg)|![](https://clevercoffee.de/wp-content/uploads/2021/04/IMG_20210404_151123.jpg)

Wer einen Dremel besitzt, etwas Geschick mitbringt und kein Problem damit hat, dass Änderungen irreversibel sind, kann damit eine sehr saubere und solide Lösung ausarbeiten.

Wer hintgegen eine reversible Lösung sucht muss sich um eine Displayhalterung (aka 3D Case) bemühen. Eine "Standardlösung" ist aktuell nicht bekannt, aber für alle 3D-Drucker Besitzer, liegen entsprechende Vorlagen auf [Github](https://github.com/rancilio-pid/ranciliopid-handbook/tree/main/3d-designs) (inkl. [Anleitung](https://github.com/rancilio-pid/ranciliopid-handbook/blob/main/3d-designs/Einbauanleitung.pdf) für den Einbau und die Magnete):

* [Rancilio STL](https://github.com/rancilio-pid/ranciliopid-handbook/blob/main/3d-designs/Case%20Rancilio.stl){:target="_blank"}
* [Gaggia STL](https://github.com/rancilio-pid/ranciliopid-handbook/blob/main/3d-designs/Case%20Gaggia.stl){:target="_blank"}
* [Universal-Halter](https://www.thingiverse.com/thing:4897546){:target="_blank"}
* [Halterung zum reinklicken](https://www.thingiverse.com/thing:4662947){:target="_blank"}

## Spannende Addons die gleich mit erledigt werden können

* Senkschraube am Sieb
* Reinigung der Wasserschläuche (sofern die Maschine nicht neu ist)
* [LED-Umbau der Schalter](LED_Umbau.md)

## Ausblick

Features die ebenfalls eingebaut werden können:

* digitales Manometer
* [integrierte Waage](Waage.md)
* Silvia E Zeit für automatisches Ausschalten verändern
* Automatische Funktion zum Wechsel von Dampf auf Brühen
