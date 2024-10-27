---
title: Abgabe Übungsblatt 01
subtitle: Technische Informatik 2 Wintersemester 2024/25
author: Hannes Muster, Zara Muster, Fredo Muster
group: H04
tutor: Hier den Namen Eures Tutors eintragen
bibliography: bibueb01.yaml
---

# Aufgabe 1

Hier schreibt Ihr Euren Text für Eure Aufgabenlösung. 

Aus dieser Datei könnt Ihr mithilfe des Programms
[pandoc](https://pandoc.org/) ein PDF erzeugen. Ihr könnt pandoc
direkt aufrufen: `pandoc --pdf-engine=lualatex --citeproc --csl=chicago-author-date-de-adapted.csl --data-dir=. --template ti2 -o ti224_ueb01_grpH04.pdf ti224_ueb01_grpH04.md`. Da das etwas
länglich ist, könnt Ihr auch das Makefile verwenden: `make
ti224_ueb01_grpH04.pdf`.

Denkt bei der Benennung der Datei an die Dateinamenskonventionen: Euer
PDF heißt dann `ti224_uebXX_grpYY.pdf`, wobei XX der Nummer des
Übungsblattes und YYY Eurer Gruppennummer entspricht.

Einige Hinweise zur Verwendung von Markdown findet Ihr in diesem
Dokument. Weitere Informationen gibt es im [Pandoc
Manual](https://pandoc.org/MANUAL.html).

## Kollaboratives Arbeiten

Für das gemeinsame Editieren von Dokumenten könnt Ihr das unieigene
Hedgedoc verwenden: <https://hackmd.informatik.uni-bremen.de>. Nach
dem Anmelden könnt Ihr dort neue Dokumente anlegen
(<https://hackmd.informatik.uni-bremen.de/new>). Dann könnt Ihr dort
den Inhalt dieses Dokuments hineinkopieren und editieren. Wenn Ihr
fertig seid, kopiert Ihr es wieder zurück oder verwendet
Menu->Markdown zum Herunterladen. Falls Grafiken eingebunden werden,
müsstet Ihr die Links darauf auf Eure lokalen Grafiken ändern. Die in
Hedgedoc hochgeladenen Grafiken können wir nicht werten, weil sie nach
der Abgabe noch verändert werden könnten.  Die fertige Markdown-Datei
könnt Ihr dann wie oben beschrieben in ein PDF wandeln.

## Source Code

Code lässt sich folgendermaßen einbinden:

``` {.cpp .numberLines}
#include <iostream>

const int zeilen=6;

int main() {
    int n=zeilen;
    while (n>=0){
        int i=0;
        while (i<n){
            cout << " ";
            i=i+1;
        }
	}
}
```

In Markdown sind auch Exponenten darstellbar, z.B. 2^128^. Ebenso können Subskriptionen verwendet werden, z.B. A~20~.

## Literatur

Gebt immer alle von Euch verwendeten Quellen an und achtet auf eine
korrekte Zitierweise. Ihr könnt Literaturangaben manuell in Eure
Abgaben schreiben (siehe Abschnitt [Manuelle Literaturverweise]). Etwas komfortabler ist es, sie
erzeugen zu lassen: in Markdown können Literaturangaben in einer extra
yaml-Datei angegeben werden, die im Yaml-Header der Markdown-Datei
angegeben wird. In diesem Beispiel heißt die Datei bibueb01.yaml
(siehe yaml-Header oben). In der yaml-Datei werden dann die
Informationen zur Quelle angegeben. Mögliche Felder für die
Literaturangaben finden sich
[hier](https://aurimasv.github.io/z2csl/typeMap.xml).

[Manuelle Literaturverweise]: #manuelle-literaturverweise

Ein Beispiel für eine Quellenangabe im Text sähe dann so aus: laut
@Herold2017 wurden für den Abakus meist Holz- oder Glasperlen
verwendet [@Herold2017, S.28].

Wörtliche Zitate sind als solche kenntlich zu machen, hier ein
Beispiel: Die Fähigkeiten des Abakus beschreiben die Autoren
folgendermaßen: "Mit einem Abakus sind die Grundrechenarten Addition,
Subtraktion, Multiplikation und Division durchführbar, aber auch das
Ziehen von Quadrat- und Kubikwurzeln." [@Herold2017, S. 29].

Auch die Kommunikation mit Chatbots ist eine Quelle und muss
entsprechend referenziert werden. Die Kommunikation mit dem Chatbot
wird wie ein Interview zitiert. Gebt die **gesamte Kommunikation** zu
dem entsprechenden Thema im Anhang an.

Beispiel: Die Kommunikation mit ChatGPT (siehe Anhang) ergab, dass ein
Elektroauto bei einer Durchschnittsgeschwindigkeit von 100 km/h
mehrere tausend Jahre für die 384400 km von der Erde zum Mond brauchen
würde, ein Hyperschallflugzeug mit einer Geschwindigkeit von 1227 km/h
würde mehrere Jahre benötigen und das schnellste Elektroauto der Welt
mit einer Geschwindigkeit von 412 km/h nur 38.7 Tage
[@chatgpt230321]. Diese Ergebnisse sind allerdings so nicht
korrekt. Bei 100 km/h bräuchte ein Fahrzeug (hypothetisch) 384.4
Stunden, also ungefähr 160 Tage, bei 1227 km/h wären es ca 313.3
Stunden, also etwa 13 Tage und bei 412 km/h ca 933 Stunden, was etwa
39 Tagen entspricht. Zudem fehlen Referenzen für wesentliche
Informationen wie z.B. die Entfernung von der Erde zum Mond oder die
Geschwindigkeit des schnellsten Elektroautos.

Im Literaturverzeichnis werden die Quellen dann so eingebunden:

::: {#refs}
:::

### Manuelle Literaturverweise

Wenn Euch Markdown-Verweise zu umständlich sind, könnt Ihr die
Literatur auch manuell angeben, z.B. so: Eine Central Processing Unit
(CPU) enthält den Befehlszähler (Program Counter), der auf den Befehl
zeigt, der als nächstes auszuführen ist (Tanenbaum und Austin 2014,
S. 75).

Und dann im Literaturverzeichnis:

Andrew S. Tanenbaum, Todd Austin: Rechnerarchitektur — Von der digitalen Logik zum Parallelrechner.
6. Aufl., Pearson, 2014. ISBN 978-3-8689-4238-5.


## Verschiedenes

Auf eine Webseite kann man folgendermaßen verweisen: [Name des
Verweises](https://www.uni-bremen.de).

Grafiken bindet man so ein (auf Groß- und Kleinschreibung achten!):
![Name der Grafik](ti2-2024.png){width=20%}. 

Falls Ihr ein Abbild Eures Bildschirms anfertigen wollt, verwendet
dazu bitte die Screenshot-Funktion Eures Systems. Auf vielen Systemen
kann dazu die Taste `Druck` oder `prt sc` verwendet werden. Unter
macOS solltet Ihr `Shift-Command-5` verwenden können.

Eine Liste von Dingen kann man mit \* anlegen:

* erster Punkt
* zweiter Punkt
* dritter Punkt

## Literaturverzeichnis


::: {#refs}
:::

# Anhang

Chatverlauf mit [ChatGPT](https://chat.openai.com/chat) am 21.03.2023:

Frage: Wie lange braucht ein Elektroauto von hier zum Mond?

>Ein Elektroauto kann nicht zum Mond fahren, da die Entfernung zum Mond zu groß ist und die Oberfläche des Mondes nicht befahrbar ist. Der Abstand zwischen der Erde und dem Mond beträgt durchschnittlich etwa 384.400 Kilometer, was selbst für die schnellsten Fahrzeuge auf der Erde unmöglich zu erreichen ist.

>Es ist wichtig zu beachten, dass Elektroautos für den Straßenverkehr ausgelegt sind und für den Betrieb auf der Erde optimiert wurden. Die Reise zum Mond erfordert vollständig andere Technologien und Materialien, die für die Raumfahrt geeignet sind.


Frage: Berechne trotzdem, wie lange das Elektroauto brauchen würde

>Wie bereits erwähnt, kann ein Elektroauto nicht zum Mond fahren, da es nicht für die Raumfahrt geeignet ist. Daher lässt sich die Frage nach der Reisedauer nicht sinnvoll beantworten.

>Wenn wir jedoch hypothetisch annehmen, dass ein Elektroauto mit einer durchschnittlichen Geschwindigkeit von 100 km/h zum Mond fahren könnte (was nicht der Fall ist), würde es mehrere tausend Jahre dauern, um den Mond zu erreichen. Selbst mit der schnellsten Geschwindigkeit, die jemals von einem Fahrzeug erreicht wurde (ca. 1.227 km/h von einem Hyperschallflugzeug), würde die Reise zum Mond immer noch mehrere Jahre dauern.

Frage: Wie lange genau würde das schnellste Elektro-Auto brauchen?

>Das schnellste Elektroauto der Welt, der Rimac C_Two, hat eine Höchstgeschwindigkeit von 412 km/h. Selbst wenn wir annehmen, dass das Auto in einem Vakuum fahren könnte und keine Hindernisse auf dem Weg zum Mond zu überwinden hätte, würde es immer noch fast 930 Stunden oder 38,7 Tage benötigen, um den Mond zu erreichen. Dies liegt daran, dass die Entfernung zwischen der Erde und dem Mond etwa 384.400 Kilometer beträgt.

>Es ist jedoch wichtig zu beachten, dass Elektroautos nicht für die Raumfahrt geeignet sind und die Technologien und Materialien, die für die Raumfahrt benötigt werden, vollständig unterschiedlich sind. Daher ist es nicht sinnvoll, die Reisezeit eines Elektroautos zum Mond zu berechnen.
