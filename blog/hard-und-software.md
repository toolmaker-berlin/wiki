---
description: >-
  Hier findet man meine persönlichen Abwägungen zu verwendeter Hard- und
  Software seit Anfang 2020. Aktuelle Informationen befinden sich am Anfang der
  Seite.
---

# Hard- und Software

## Neuausrichtung 2023

### Aktuell

* Sichten der vorhandenen Notizen und Experimente zum Wissenstransfer ins neue private Wiki
* Sortieren vorhandener Programmbeispiele und präsentierten in verschiedenen Umgebungen
* Herrichten einiger exemplarischer Umgebungen zum benutzen und präsentieren



### Cloud Nativ als Ziel

* Livedrive, iCloud und Git sind die Backbones meiner Daten neben lokalen Backups.
* Wichtige Cloud Dienste: CoCalc, Replit und ein paar Nischenanbieter z.B. für Swift, sowie neu: Gitbook
* Wichtige Werkzeuge sind iTerm2, Vim, JupyterLab, VSCode für Python, Julia und vielleicht auch etwas Swift.
* CoCalc ist die allumfängliche Lösung. Für JupyterLab und VSCode braucht es aber ein Upgrade auf eine bessere Lizenz (4 CPU, 4GB RAM)

### Hardware

* MacPro und 32“ Monitor zum intensiven arbeiten&#x20;
* Reserve bilden alte iMac‘s&#x20;
* Mobil konzentriert es sich auf iOS iPhone - weniger auf Tabletts
* Falls nötig Mobil eher ein altes MacBook 12"
* Immer wieder verlockend: kleines iPhone, iPad mini (neu) und eine Apple Watch
* Neu: Kompromiss MacBook Pro 13“ M1&#x20;
* Outdoor möglichst nur iOS - besonders mein iPhone benutzen.&#x20;

## iOS/MacOS und Geräte 2022/23

* Der M2 hat ein Memory Speed Problem abhängig von der Größe der SSDs. Siehe Mark Ellis Video Export Test. Ab 512GB/1TB gehts wohl gut.
* Mosh via „Zero Tier One“ geht wieder. Konfiguration musste erneuert werden
* Replit ist teuer geworden, aber Dank meiner bisherigen Optimierungen auch gut zu gebrauchen. Vorteil iOS Integration besonders des Editors, GIT und Browser.
* Replit funktioniert auch am Mac gut. Der Editor ist allerdings Mist.
* Es gilt trotz allem: ich habe genug gute Geräte (solange diese funktionieren).
* Auch mein iPhone kann noch lange durchhalten, zudem erst ab 15/16er Generation wirkliche Fortschritte zu erwarten sind: USB3, Titan, Zoom, Nits, Speed.
* Ein faltbares iPhone wäre der Hit.

## iPhone 13 Pro Max

* Der neue iPhone Ständer ist echt klasse. Dünn, leicht und man kann ganz nahe an ihn ran rücken, so das man mit der externen Tastatur nahe wie bei einem Laptop sitzt. Mit der Falttastatur kommt man sogar so weit runter, dass man die Zifferntasten nicht mehr richtig sieht wie beim Magic Keyboard von Apple. Das ganze passt dann in eine kleine Tasche.
* Auch der neue Fingerring gibt einen guten vertikalen Ständer ab.
* Replit ist insofern mies als APP, als man nicht zwischen den Apps hin- und herschalten kann ohne das die App ein reconnect zum Server erzwingt. Und der dauert. Vielleicht hilft dualscreen. Leider nein, wird nicht unterstützt. Aber der App-wechsel scheint jetzt schneller zu gehen als früher. Die App wächst!
* Blink hat mosh, aber CoCalc hat es nicht. Dafür hat ShellFish Tmux integriert was gut läuft.
* Blink bietet dafür auf iPads mit Tastatur VSCode!
* CoCalc bleibt der große gemeinsame Nenner für remode Arbeit mit vim/Julia oder Python. Ggf. auch Juno Connect.

> I don’t think NeoVim is faster than other text editors. However, knowing Vim motions will undoubtedly make you faster.

> I will stick with enabling vim motions in Visual Studio Code. The best of both worlds.

### Teste Swift (wegen neuem Compiler)

```swift
var gen = 0
    for i in 1...1_000_000 {
        gen = (gen * 3 + 5 + i) % 0xfffffff
    }
```

| System                | Zeit                                    |
| --------------------- | --------------------------------------- |
| MPro Swift Playground | 1872 ms                                 |
| MPro Coderunner       | 531 ms                                  |
| MPro XCode            | **482 ms und 5 ms mit -O Optimierung**  |
| MPro Python 3.10      | 198 ms                                  |
| Replit free           | 2014 ms                                 |
| Code App              | 40 ms                                   |
| Swifty iPhone         | 6 ms hier hab ich auch schon 98 gesehen |
| Cocalc Julia          | 6 ms                                    |

### Python numba, cython, etc.

Keep in mind that while Cython and Numba can significantly improve the performance of your code, they’re not silver bullets. They’re best used in conjunction with other performance optimization techniques, such as algorithmic improvements, data structure optimizations, and parallelization.

Also, note that Cython and Numba are just two of the many tools available for optimizing Python code. Other tools, such as PyPy, Shed Skin, and f2py, may be better suited for your particular use case. Shed Skin is an experimental restricted-Python (3.8+) to C++ programming language compiler. F2PY is a tool that provides an easy connection between Python and Fortran languages. F2PY is part of NumPy. F2PY creates extension modules from (handwritten or F2PY generated) signature files or directly from Fortran sources.

Codon is a high-performance Python compiler that compiles Python code to native machine code without any runtime overhead. Typical speedups over Python are on the order of 10-100x or more, on a single thread. Codon’s performance is typically on par with (and sometimes better than) that of C/C++. Unlike Python, Codon supports native multithreading, which can lead to speedups many times higher still. Codon grew out of the Seq project.

### REPLIT Julia (bis April)

* Bisher konnten Pakete nur über Sessions gehalten werden, wenn man die Repl auf always on gebucht hat. Für 2 Cent pro Tag war das ok aber ab **April** werden es 20 Cent. Das ist nicht vertretbar!
* Das Julia Problem hat noch kein fertiges Workaround. Alternativ eigene Repl definieren, damit es einfacher geht.
* Ausprobiert: .julia kopieren mit Skript **FUNKTIONIERT - Problem gelöst!** mal mit symbolischen link setzen probiert und geht auch.

### M2 Mini’s

**What I tell most people is this: buy the machine you need when you need it. There will always be something newer and better just around the corner.**

> _What really caught my eye with the release of these new Macs wasn’t the performance enhancements of the M2, M2 Pro & M2 Max chips, it was three key hardware updates that these Macs received that I think might have a bigger impact in the day-to-day lives of some creative professionals than these new SOCs will have:_ **Bluetooth 5.3, HDMI 2.1 and WI-FI 6E**

> Ende Januar 2023 hat Apple mit den aktualisierten Mac Mini‘s M2 und M2 Pro sein Angebot erneuert. Der M2 Max debütiert in den neuen MacBooks Pro’s.

> Weiterhin besteht kein Handlungsbedarf, da es zur Zeit keine Anwendung für mehr In-house Performance über den aktuelle vorhandenen Geräten gibt. Mobil wird noch viel experimentiert und „cloud native“ beim Coden wird sogar immer attraktiver.

> Damit wird der Bedarf an stationärer Hardware auch immer anspruchsloser. Im Extremfall tut es immer noch ein M1 Mac Mini oder ein älterer Intel-Mac, je nach attraktiver Ausstattung. Angebote liegen jeweils um die 1000€, auch MacBooks in Shell-Mode wären gebraucht eine Alternative.

> Möchte ich auch lokale Performance dann liegt der Sweet-Spot beim Mac Mini M2 pro bis Mac Studio rund bei 2000€ +-300€.

> Ein Einstieg in die Mx-Welt ist aber problemlos mit der M2 Mini Basis-Konfiguration oder einem gebrauchten M1 Mini mit besserer Konfiguration von 700-1000€ möglich. Auch ein iMac könnte eine Alternative unter Umständen werden, ebenso wie mobile 12-16 Zoll MacBooks zwischen 2500-4000€.

> _Entwickler standen jetzt öfter vor dem Problem, dass ihre Rechner mit 16GB Ram dauernd am Limit waren. 32GB oder mehr sind für einen Rechner, auf dem VMs und Docker-Images laufen sollen, kein Luxus mehr, sondern Minimum._

> Die Zukunft bleibt entspannt offen. Je länger desto besser. Aber alles spricht für Zukunftssicherheit mit M2 oder neuer.

> Aktuell bevorzugt **Mac Mini M2 Pro** - wegen 4x Thunderbolts - mit Minimum 16GB/512GB für 2000€ oder maximal 32GB/1TB für 2500€. Letzteres ist besser wegen der SSD Geschwindigkeit die mit 512GB nur 1/2 beträgt. Da muss man dann aber auch nochmal über einen Mac Studio nachdenken. Also besser Preise für zukünftige Mac Studio‘s mit M2 abwarten.

### Aktuelle Erfahrungen Hardware

* Ein iPhone Pro Max ersetzt bequem ein Tablett, ist immer dabei, immer online, hell und ausdauernd. Die Bildschirm-Tastatur ist dabei das entscheidende, da sie in diesem Format ausreichend sicher zu bedienen ist, ggf. sogar mit Zusatzzeile. Möchte man das noch verbessern reicht eine externe Tastatur und ggf. ein Phone-Ständer bzw. Fingerring.
* Ein Tablett ist insofern auf Reisen überflüssig, da man dann ggf. lieber gleich ein MacBook 12 Zoll zum intensiven Arbeiten mitnimmt. Allerdings wird dieses eventuell leichter geklaut als nur eine Tastatur. Das iPhone hat man in der Regel immer sicher bei sich.
* Für ein 10.5 Zoll iPad inkl. Tastatur, egal welche, spricht dann nur noch die etwas bessere Portabilität, eingebautes unabhängiges Mobilfunknetz und der hellere Bildschirm. Mit Produkten wie Replit, CoCalc, Codespace und Deepnote ist per Browser auf einem Tablett immerhin noch gutes onlinebasiertes Arbeiten möglich. Python und Textverarbeitung offline sowieso. Etliche Apps laufen aber auf dem iPhone besser, da sie auf iPadOS ungenügend angepasst sind. Allerdings ist ein Tablett auch immer besser für den Medien-Konsum unterwegs geeignet.
* Alternativ kann auch die Mitnahme eines iPads (Mini) zur Entlastung des iPhones sinnvoll sein. Mein iPad Mini 4 ist allerdings mit 500 nits etwas dunkel, also für outdoor im Sommer nur schlecht geeignet.
* Mit Spannung beobachte ich nun die Weiterentwicklung der iPhones: Helligkeit, Geschwindigkeit und Ausdauer durch 3nm, Leichter durch Titan und vor allem bequemes USB-C Laden. Durch alternative AppStore‘s könnte zudem mit iOS 17 ab Ende 2023 softwareseitig eine weitere Öffnung für Entwicklersoftware anstehen.
* Allerdings ist ein iPhone Max auch unhandlicher als kleinere iPhones. Daher muss sich zeigen welche Funktionen auf die iWatch ausgelagert werden können. Bisher ist die iWatch nur ein besserer Ersatz für meine ältere Withings (Signalisierung, Ablesbarkeit) allerdings mit Potenzial.

### Update iPhone 13 Pro Max

* Einfach alles Super, besonders das große iPhone selbst, das ein **Tablet gut ersetzen** kann, hat den Sprung nach vorne gebracht.
* **MagSafe** selbst und kompatibles Zubehör auf Aramidhülle: Magnetischer Fingerring, Ständer und Powerbank mit Logitech **Minitastatur** erhöhen die Funktionalität erheblich.
* **1000 Nits** und mattes Panzerglas in der Sonne sind besser als jedes iPad oder Notebook.
* Trotz Größe und Gewicht mehr Komfort beim Lesen und Schreiben dank besserem **Bildschirm und Bildschirmtastatur** (mit Fingerring). Man gewöhnt sich schnell daran und das iPhone 11 Pro wirkt plötzlich winzig. Nach ein paar Wochen tritt Gewöhnung ein: Das iPhone Max wirkt „normal Groß“.
* Bessere Kamera, mehr Speicher und mehr **Speed** z.B. bei Python (entspricht M1 MacBook Air).
* Trotz Replit fragt sich, ob nicht mehr **Python** mit Pyto (oder Juno) statt **Julia**, da Pyto stand-alone läuft und iOS Funktionen integriert. Zudem ist es unwahrscheinlich, das ich nochmal die extreme Geschwindigkeit von Julia benötige. Leider ist die Working Copy (**Git**) Integration mit Pyto irgendwie noch nicht rund. Pyto selbst aber auch Juno brauchen noch Weiterentwicklung. Aktuell gibt es auch ein Update von Pythonista3!
* Also, trotz allem bleiben **Replit** und **CoCalc** die Tools der Wahl auf dem iPhone, besonders wenn es um **Julia** geht!
* Das beste ist natürlich, das beim **cloud native** programmieren die Performance des iPhones nicht so wichtig ist und den Akku somit schont.

> Inzwischen macht auch die Software Fortschritte: Replit kommt aufs iPad, Code wird verbessert aber noch kein Julia, Juno kommt in besserer Standalone Version aber noch Python 3.6, Pyto und a-shell stehen für Speed und Kompatibilität, Blink unterstützt VSCode.

### Status

> Durch meine Mac/Unix Praxis der letzten Jahre fühle ich mich inzwischen im Unix-Umfeld ausreichend breit und sicher aufgestellt. Vertieft und verbessert werden sollte noch mein Umgang mit Julia, Git und Vim, sowie die Wartung meines Fuhrparks.

> Mobil zeigt sich zunehmend, dass CoCalc und Replit auf dem iPhone 11 Pro und 11 Max, bzw. 7 Plus, besser zu händeln sind als mit iPad(s) jeder Größe. Zuhause wird zur Zeit ein fester Mac Arbeitsplatz mit VSCode bevorzugt, wahlweise mit Cloud Anbindung (keine Konfiguration, keine Backups, mehr Leistung) und natürlich mit Remote Zugang zu CoCalc und Replit.

> **Zentraler Ort für Konsum und Alltagsleben ist und bleibt das iPhone. Ich habe deshalb auf ein iPhone 13 Pro Max gesetzt. Für den Sprung auf 14/15er ist es noch zu früh. Ein 13er, wegen dem hellem, großen und guten Bildschirm und der guten Akku-Leistung, musste es sein. Mein 11er bleibt Reserve.**

> Steht kein Mac zur Verfügung wäre ein größeres iPad bei umfangreichen Aufgaben eine hilfreiche mobile Option (Akkulaufzeit, Helligkeit, Mobilfunk), mehr aber auch nicht. Mittels externer Tastatur ist ein iPhone sogar quer genauso breit wie ein iPad mini im Hochformat. Bei gleicher Größe zum iPad bleibt ein MacBook immer noch vorteilhafter, da vielseitiger, allerdings ohne Mobilfunk.

> Zuhause muss irgendwann ein Mx Upgrade ran, möglichst gebraucht, etwa ein Mac Studio M1 Max 64gb/4tb. Meine 12er MacBooks langen noch lange hin.

### Getestet

Geprüft welche Apps (primär Coding und Textverarbeitung) wirklich vom großen iPhone Bildschirm (Max) profitieren: Keine besonders, außer Bildschirm-Tastaturen lassen sich besser tippen und Medien besser konsumieren, dafür ist aber das Gewicht größer.

* Quer geht immer für lange Code Zeilen, aber Tastatur kann stören mit extra Zeile (abschaltbar)
* iPhone und besonders iPad mini machen eine gute Figur mit Stand bzw. Cover und logi Mini Tastatur.
* Beim normalen 11er 33-36 oder auch 40 Zeichen und beim Max 45 sind vollkommen ok (c64 bzw. vc20)!
* Programme entwickeln sich weiter, z.B. Juno wird besser
* Ein 12er von der Breite her ok mit REPLIT und UpNote getestet, besonders die Tastatur ist schon besser.
* Zu meinem 11er Pro ist das 12er schon 3mm breiter und das Max sogar 9mm. Im Querformat also nur 1-3 zusätzliche Zeilen mit BT-Tastatur, also unerheblich.
* Folglich nächstes Model erstmal ein Max und anschließend ggf. ein normales Pro für mich, falls die Größe oder das Gewicht stören.

### Erprobten Tools & Dienste

* VSCode
* iTerm2
* Vim
* Zsh
* SSH
* Tmux
* Python
* Julia
* Jupyter
* CoCalc
* Deepnote
* Replit
* Git
* Docker
* Codespace
* Juno
* Shellfish
* Blink
* Pyto
* Carnets

### Meine bewährten Setups

* VSCode (GUI primär) lokal/ssh und mit Codespace arbeiten am Mac
* iTerm2 (Text primär) lokal/ssh arbeiten am Mac
* Remote (CoCalc, Codespace/Git, Replit, Deepnote, Google CoLab) von überall her gut arbeiten via Browser
* Remote & Desktop NEU: GitPod (sieht auch gut aus)
* iOS mobil (Julia remote und Python local) leider nur zum ausprobieren, tüfteln oder zum hotfixen wegen einiger Einschränkungen und iPad am besten nur mit externer Tastatur

### Meine primären Dienste

* CoCalc
* GitHub
* Replit
* Deepnote
* GitPod
* iCloud
* GDrive
* Livedrive
* Dropbox

### Hardware (Update)

* iPhone Pro (Max) ab 15er mit USB-C und ggf. Periskope Zoom und 3nm und WLAN 6E dann erst Anfang 2024. Bei dem hohen Preis muss es länger ok sein. Max oder nicht Max bleib die Frage! Tendenz: Das iPhone für alles!
* iPad mini 7 mit OLED und Mx auch USB-C wäre nett
* MacBook (ab 12“) mit 5G und USB-C am besten mit OLED, primär für Cloud Nutzung ausgelegt wäre auch nett
* Mac (Mini/Studio/Pro) alt oder neu mit hohem Single Core Wert ca 4-5 GHz gewünscht. **Alternativ, besonders unter Cloud Computing Gesichtspunkten, ist auch ein wie auch immer iMac nett!**
* Apple’s Watch. Es reicht Serie 7 Cellular für Erfahrungen. Die Ultra erst mit Blutzucker Sensor. Derzeit wäre mein 11er mit Nokia Watch noch ok, aber wegen der Erfahrungen hab ich jetzt eine 7er.

#### iPhone Maße und Gewicht

```
5.76 140g mini 64.2x131.5x7.40

6.24 188g 11er 71.4x144.0x8.10
6.46 162g 12-- 71.5x146.7x7.40
6.46 203g 13er 71.5x146.7x7.40
6.51 206g 14er 71.5x147.5x7.85

6.84 188g 7er+ 77.9x158.2x7.30
6.89 226g 11er 77.8x158.0x8.10
7.12 226g 12er 78.1x160.8x7.40
7.12 238g 13er 78.1x160.8x7.40
7.12 255g 14er 77.6x160.7x7.85

```

Don’t worry if it doesn’t work right. If everything did, you’d be out of a job. (Mosher’s Law of Software Engineering)

### Fazit Sommer 2022

> _Das iPhone 11 Pro ist revitalisiert zurück: mit Carbon Hülle, neuer virtueller Tastatur und minimierter Schriftgrösse sowie neuer Software._ Im Sommer macht sich auch das geringe Gewicht angenehm bemerkbar.

> Ein 11er Pro Max musste her zum ausprobieren. Kann ich dann bestimmt hier und da benutzen, ergänzend zum meinem altem 7 Plus und herausfinden was mir beim 14/15 oder 13er liegen wird. Seit Replit Tendenz zum Max.

> Privat musste ich noch eine Apple Watch Model 7(++) mit GPS und Celuar haben. Auch ein neuer(er) Mac Desktop reizt.

> Blinde Flecken wurden inzwischen beseitigt. Neben GIT jetzt auch mal RUST und SWIFT angesehen. GO und LUA ziemlich uninteressant außer für NVIM mit LUA. PYTHON zunehmend lustlos außer Quick & Dirty. Was bleibt? Wieder mehr Julia, vielleicht meine alten Projekte?

**Hardware:** iPad Mini mit Option Cellular geupdatet. Mobil also jetzt nur noch iOS/iPadOS. Notfalls MacBook (12“). Daher kein neues Notebook und auch vorerst kein neues iPhone notwendig. iPhone 11 Pro reicht aus und neuere Modelle sogar 2 mm breiter. Daher eher kein Max mehr notwendig. Abwarten wie es mit viel Schreiben und programmieren läuft. Weitere Modelle 2022 und Sommer/Herbst 2023/2024 abwarten. **Warum: Mobil iOS ist leichter, kleiner, heller und ausdauernder, sowie immer Online.**

**Software:** Julia/Python mit VSCode/Vim am MacPro und via Blink/JUNO und Replit am iPhone/iPad (CoCalc). Python auch nativ am iPhone/iPad (Pyto/etc). Neu jetzt auch VSCode in Blink und Git/Codespaces. Und zuletzt noch ShellFish und WorkingCopy, perfekt! **Fazit: Mobil zum ausprobieren und lernen - Ernsthaft dann wieder am Desktop oder großen iPad (10,5“) mit Tastatur (primär Codespaces).**

**Konsequenz:** Keine neue Hardware auch keine Schnäppchen. Mittel werden für mögliche Ersatzbeschaffungen gebraucht. Der MacPro kann durch Mac Mini/Studio oder neues MacBook ersetzt werden. Ein Tablett durch iPhone Pro (Max). **Also weiter Erfahrungen sammeln und abwarten.**

### Zusammenfassung

**Julia** sollte ziemlich sicher wegen ihrer Eleganz und Skalierbarkeit meine Zukunft sein. **Python** andererseits ist defacto auf iOS und besonders **offline** schon etabliert und inzwischen auch ausgereift anzuwenden. Julia bedingt daher für mich **LAN/WLAN und CELLUAR.**

Somit zur Zeit noch abwarten und probieren wie gut bzw. intensiv iPads vs iPhones zum programmieren benutzt werden können, siehe auch **VSCode, GIT und Codespaces etc.**

**Neue Hardware und Gerüchte:** Ein neues oder gebrauchtes Notebook gibt es erst wenn nötig bzw. als Ersatzbeschaffung. 12er oder 15er in 2023 oder M2 14er? Alles ist möglich. Bevorzugt (endlich) ein MacBook mit 5G! Bis dahin wird iPhone und iPad mobil weiter kultiviert: 11er M2 oder ein Mini mit M1/M2 ggf. OLED? Oder iPhone 14/15 Pro Max?

**Lokales Arbeiten** ist nett, aber man braucht trotzdem den systemweiten Abgleich über die **cloud**. Dann kann man auch gleich in der cloud arbeiten, braucht aber **LAN/WLAN und CELLUAR.**

> **VSCode** ist vielleicht gekommen um zu bleiben, besonders mit dem **VIM-Plugin.** Das verändert einiges, da alle Entwicklungen und Spielereien bestens primär am Desktop oder am Notebook erledigt werden können, ohne die **VIM** Routine aufzugeben. Browser Versionen und **Codespaces** von Microsoft sind auf dem Weg. Die Durchgängigkeit von VSCode zwischen Desktop bzw. Cloud/CoCalc sowie Shell/VIM und damit iOS/Handy ist allerdings noch nicht vollständig gegeben, besonders wegen Julia.

**iPad Pro und mein 11er iPhone sind Outdoor eine super gute Kombination. Selbst ein eigener neuer M1 Mac Mini zuhause macht dank CoCalc/Replit und meinem alten Mac Pro zur Zeit keinen Sinn. Zudem gibt es ja noch das kleine MacBook mit dem ich gut mobil arbeiten kann. Und erstaunlich wie hell das 11er iPhone mit 800 Nits ist. Mehr als die 600 Nits vom iPad Pro sind zur Zeit auch nicht drin. Daher fällt mein iPad Mini 4 für draußen - außerhalb eines Schattenplatzes - aus, ebenso wie Notebook’s mit 400/500 Nits. Und ggf. ist ein 11er Max immer noch eine preiswerte Alternative zu einem 13/14er Max. Allerdings wird der Accu bei großer Helligkeit und Schwarz auf Weiß auch schnell leer. Das spricht für ein iPhone Max!**

Um es nochmal deutlich zu sagen: Mit dem iPhone zum Konsum und geringfügige Produktion von Inhalten ist man gut und portable unterwegs. Remote programmieren geht auch (besser allerdings mit iPad oder MacBook), aber nur mittelmäßig mit Julia und lokal eigentlich nur gut mit Python. Also vielleicht “back to the roots” und Projekte nur per Desktop und mit Python?

> _Julia und VSCode bleiben vielleicht nur ein interessanter professioneller “Ausflug”. Als “Hobbyist” bleibe ich vielleicht eher bei iOS und Python, wobei durch Replit die Chancen für Julia seit kurzem wieder steigen._

**Verrückte Situation: nicht “VS” sondern sowohl als auch - etwas Julia und Python (vertiefen) und auf Desktop, Notebook, Tablett und iPhone anwenden. Mit der am besten funktionierenden Methode. Bezüglich Projektarbeit und Lernen geht derzeit nix über einen richtigen Arbeitsplatz mit allen Tools!**

> Daher rüste ich meinen MacPro Arbeitsplatz gerade etwas auf, besonders mit einem neuem Monitor. Tendenz: kein weiteres Notebook oder Mac Studio/Mini, eher **iPhone Pro Max oder iPad Pro Mx oder Mini Celluar (wir warten auf Mini 7 wegen Nits und CPU) und da mobiles OS dann auch kein VSCode außer großes iPad mit externer Tastatur, sondern nur BLINK oder JUNO mit CoCalc IDE und Replit.**

> Also (zuerst) neues IPhone 11/13/14 Pro (Max) oder doch (zuerst) neues iPad Mini (6/7) - das bleibt derzeit die Frage. Das jeweils Andere bleibt hinten an. Zeitpunkt wahrscheinlich Frühjahr 2023/2024.

> Besser ein iPhone 14/15 da bessere Performance per Watt und besserer Bildschirm mit 1000 und mehr Nits. Dieser Sommer ist gelaufen, da noch Kurse am MacPro und es bleibt Zeit die Systeme zu testen.

Vorerst alles gelaufen da neues iPad Mini, iPhone 11 Max, Ersatz iMac mit Thunderbolt und iWatch angeschafft. Daher jetzt keine Vorentscheidung für neue Hardware, aber vertiefen der Software bis mindestens 2023++.

**Allenfalls zur Überbrückung noch ein 13er oder 12er iPhone Max, falls ich viel schreibe oder editiere und der Preis stimmt.**

***

***

***

## Details

### Technik leaks

Für das iPhone 14 und iPhone 14 Pro wird eine Display-Auflö­sung von 2532 mal 1170 Pixel und 460 PPI erwartet. Beim iPhone 14 Max sind es 2778 mal 1284 Pixel und 458 PPI. Unge­wöhn­lich ist die Angabe von 120 Hz als Bild­wie­der­hol­fre­quenz beim iPhone 14. Das wäre der gleiche Wert wie bei den Pro-Modellen. Für das iPhone 14 Max belässt es Apple den Angaben zufolge bei 90 Hz.

MAX = 7,12 cm wie 11/13er 15,41 hoch Pro = 6,46 cm dass sind 6,6 mm weniger. Altes Pro 2 mm weniger.

### Gedanken

**iPad Pro 10.5 512GB Cellular** ist jetzt mit Logitech Keyboard (teilweise) optimales Outdoor Gerät. Display leider spiegelnd (jetzt mit zusätzlichem Entspiegelglas) aber hell genug mit 600+ nits. Nur ein Handy ist noch etwas besser (vorhanden). Test **BLINK ca 20% je Arbeitsstunde also ca 5 Stunden.** Daher auch vorerst kein neues MacBook Pro 14 Zoll notwendig (zum Experimentieren reichte ein Mac Air von Flora).

**MacBook Pro 14 wäre die sinnvollste Neuanschaffung: Mehrwert ohne Verdrängung des MacPro’s. Hier möglichst warten auf M2 und Kapital für maximale Ausstattung.** Ein Notebook mit Thunderbolt könnte auch einen defekten Mac ersetzen. **Achtung: 4TB SSD wegen großer iCloud macht es teuer (4-5-6k)!**

> MBP 308 nits MB 12 Zoll 350 nits. Im Schatten oder bewölktes Wetter ist noch lesbar. Auf Schoß besser als iPad und je leichter je besser. Also die alten Notebook’s packen es noch zuhause und im Café.

Es wird aber immer noch ein OSX Mac mit Thunderbolt benötigt (mein MacPro). Ab Mac Mini aufwärts ggf. mit Studio Display (optional späteres Model), oder Ersatz iMac/MacPro. **Möglichst warten auf M2 Mac Mini oder Studio falls Ersatzgerät nötig!**

**Apple’s Spring Event** macht nachdenklich. Mobil hat sich nichts getan (p.s. das alte iPad macht sich gut, besonders im Garten in der Sonne). Notebooks sind nur wegen M1 interessant **(Speed und Accu)** und machen derzeit keinen Mehrwert. Zudem gibt es noch das 12er MacBook!

> Also wo noch einen Mac (Mini) M1 unterbringen und wozu? Ein M1 ist ca 2-3 mal schneller im Rechnen. Die neuen werden nicht viel schneller sein nur mehr Kerne und etwas mehr Bandbreite. Das ist zur Zeit von MacPro und CoCalc aber auch alles. Aber da alle M1 Single Core gleich schnell warten wir besser auf M2 und zwischendurch auf Flora.

**Julia ist sehr interessant.** Jupyter Lab unterstützt es. Das Terminal mit Vim verlockt zum programmieren ähnlich IPython. Pluto als Jupyter Alternative ist der Hammer muss aber noch wachsen.

> **Python** ist mir vertraut geworden. Weiterer Einsatz und weiterlernen jedoch nur bedingt für iOS lokale Anwendung noch sinnvoll (**Pyto** und **Pythonista**). Das bedingt schnellere Geräte auch für ein mögliches **Julia mit iSH.** Aber braucht es das? **Swift** wäre dann wohl zukunftsweisend.

> **Julia** ist sehr attraktiv. Besonders da weniger objektorientiert. Andererseits so Python-Verwandt das Routine und Wissen leicht auch auf Python zurück transportiert werden kann.

> **Ärgerlich das Julias Performance wegen der Compiler nicht lokal auf iOS zum laufen zu bekommen ist.** Blink bzw. JUNO und ein Server sind die einzigen Möglichkeiten. Da aber nur noch eine zeitkritische Aufgabe zu erfüllen wäre fragt sich ob man nicht besser doch bei **Python** bleiben sollte.

**Ich halte besonders nach meiner ersten JULIA Erfahrung am 11 Pro fest. Hinzu kommt, daß ich das alte iPad 10.5 und iPad Mini 4 demnächst mehr für JULIA einsetzen werde. Vom Ergebnis hängt die Größe und der Zeitpunkt eines neuen iPhone‘s für mich ab. Wenn mehr JULIA benutzt wird, ist das Terminal am wichtigsten und Speed eher unwichtig. Python lokal wird dann auch eher unwichtig. Für das Cloud Computing stehen aktuell zwei Mac’s und zwei MacBook’s rum. Davon jeweils einer/eines noch aktuell. Mit JULIA geht es ab Richtung Cloud bzw. CoCalc. Daher, wie alles zur Zeit: abwarten!**

Überraschend macht sich ein CASE mit Fingerring gut für die Couch. Das könnte mobiles arbeiten und konsumieren nochmal eine neue Richtung geben. Auch tippen macht sich so bedeutend besser.

QUERFORMAT ist jedoch mühsam weil Mann die Breite bildschirmtastatur mit Ring nicht „Wippen“ kann, daher breiteres iPhone bevorzugt.

Vielleicht bald ein 13er Pro Max da das 14er/15er also erst 16er in 2024 in 3 Jahren von jetzt an das interessante TOK ist. Aber 11er/7plus immernoch gute Kombination und nur 3 mm schmaler! Das lohnt kaum. In 2023/2024 könnten auch MacBooks mit 5G kommen.

Julia via CoCalc und JUNO auf dem 11er läuft und Codespaces auch.

Überlegen Desktop vs Laptop: Laptop ist zwar Portable, damit aber auch anfällig für Diebstahl.

### Wozu der Desktop besser ist

* Bessere **Sitzhaltung** beim Arbeiten (Eingabe) und Video Konsum und Vorträge (verzichtbar)
* **SaveTV** und Livedrive bzw. Promise (Irgendwann obsolet also verzichtbar)
* Zum programmieren meist grosser Bildschirm (**JupyterLab** für Test und Recherche aber verzichtbar)
* Mitschneiden **YouTube** (alternativlos aber verzichtbar)
* Tendenz iMac/MacMini/MacBook !!!

### Vorteil Laptop

* Quasi eingebautes **UPS**
* **Mobil** dh. wohnortunabhängig
* **Bildschirm** in der Regel ausreichend groß und hell
* Universelle Software wie Desktop **Betriebssystem**
* M2 MacBook Air oder 14er Pro !!!

### Vorteil iPad

* Format und **Gewicht** von Mini bis Pro 12.9
* Option **Mobile Daten** eingebaut
* ggf. Kann Handy kleiner ausfallen
* Falls iPad dann mit Tastatur und/oder Dock (Kensington) und ggf. externer Monitor (Ergonomie)
* M1/M2 11er Pro bevorzugt !!!

### Vorteil iPhone

* Immer dabei
* Immer online
* 1000 nits
* Alles ist „machbar“
* Neuestes Plus: **Fingerring**
* Tendenz Pro/Max !!!

### Drucker

* Schriftverkehr (ersetzbar)
* Als Fotokopierer (kein Ersatz)
* Per AirPrint immer im Haus

## Neue Überlegungen

> JupyterLab und vim/ipython werden meine Spielzeuge bevorzugt via CoCalc bleiben inkl. C und Assembler. Offline A-Shell, iSH, Pythonista, etc. kann Spaß bringen ebenso wie iPad Swift.

> ok - das iPad 10.5 ist repariert und bekommt die neue eSIM vom iPhone übertragen. **Achtung: Tastaturen geprüft: schwer aber Logitech ist super auch im Sommer. Mit SIM optimal!**

> Neue iPhone Gerüchte: Superzoom kommt erst mit 15er, so dass erst das 16er in 2024 das gewünschte TOCK wird. Dann also vielleicht doch schon beim nächsten in 2022 zuschlagen? Nein, denn das 11er ist gut.

> Alle MacBooks sind aktuell kein Kauf. Auch erste M2 Air nicht. A) Weil die ersten. B) M2 Pro’s wären 2. Generation und ok. Also noch viel Zeit. iPhone 15 ist dann auch erst in zwei Jahren dran. Mein 11er tut es noch gut und auch alle vorhandenen Geräte. Also fragt sich Nutzen vom iPad. 11er M1 bzw. 4/3. Generation 12.9er bieten Geschwindigkeit für lokale Arbeit und CoCalc im Browser. Ggf. auch aktuelles Gerät falls echter Bedarf. Neues 11/12er iPad’s kommen Ende 2022! **Also warten?** Geld sparen für Neuanschaffung. Wie wäre es mit einem 11er M2 iPad Ende 2022? Oder 15er iPhone Max Ende 2023? Trotzdem immer auf 4.Generation des iPad 12.9 mit Magic Keyboard achten. Bei Schnäppchen mit 4G kann man zuschlagen (WARUM?). Achtung: C zuvor noch auf M1 nativ selber benchmarken!

> **Also neues iPhone und ggf. MacBook erst ab 2023/2024 und auf Black Friday achten (amazon & apple & andere).**

> Alle iPhones und iPads eignen sich für Blink, a-Shell, iSH und Phytonista/Juno/Carnet. CoCalc/Deepnote/Google und Codespace via Browser ist ohne Tastatur/Maus nicht komfortable. Daher zur Zeit **keine neuen Investitionen in iOS-Hardware.**

## Daten usw

Wi‑Fi + Cellular Modelle iPad 12.9 Pro 3.Gen

```
Höhe: 280,6 mm
Breite: 214,9 mm
Tiefe: 5,9 mm
Gewicht: 633 g
```

Das Macbook Abmessungen und Gewicht

```
Höhe: 0,35 bis 1,31 cm
Breite: 28,05 cm
Tiefe: 19,65 cm
Gewicht: 0,92 kg2
```

Smart Keyboard (2017) vs. Smart Keyboard Folio (2018):

Für 12,9-Zoll-Modelle: 340 g (2017) < 407 g (2018)

Für 11- bzw. 10,5-Zoll-Modelle: 245 g (10,5 Zoll, 2017) < 297 g (11 Zoll, 2018)

* **Achtung: kein 12.9 (?!) da MacBook 12“ vorhanden! MacBook 12” für CoCalc ist ok.**
* pro Max für Arbeiten und als MIFI mit großer Batterie
* Das 13er ist aktuell und das derzeitige TOCK bis auf die nächsten 2 Jahre
* Verbesserung bei bat nits speed 5G und Fotos
* **Einzig es wäre nicht notwendig dieser schöne Plan**
* Vielleicht dann auch das 512er Model ist 250 mehr - wohl eher nicht
* Contra iPad mini -> ist in der Hand zu schwer aber transportabel. Performance leider unterirdisch. Besser normales iPad das ist auch noch transportabel.
* Contra ZWEI-> **mein 7 Plus ist wieder da und durchaus benutzbar.** RECONTRA Gelegenheit für Trade-In bzw. RERECONTRA dann 11er bleibt Top Reserve.

Neue Erkenntnisse Okt./Nov. 2021:

* Stärkung von **CoCalc** / GoLab / Deepnote -> minimale Wartung auf allen Geräten
* Einschränkung Browserzugriff mit iPadOS nur mit Externer Tastatur ok
* iPadOS und iOS am besten mit externer Tastatur aber
* Blink und Juno auch mit OnScreenKeyboard ok
* Auf allen Geräten auch lokales Arbeiten möglich
* Windows und Chromebook via Browser ok
* MacPro mit 27 Zoll und FireFox einfach super
* Jetzt noch den Online-Switch im Kopf umlegen

> **Oktober 2021 Status: Alle Gerätekategorien sind vorhanden. Einige sogar redundant. Daher höchstens Ersatzbeschaffungen im Fall der Fälle und warten (bis zu zwei Jahre) auf M2 MacBook Air und 14/15er iPhone‘s. iPhone 11 Pro ist ok. Neues währe 2 mm breiter und ein iPhone Mini 5 mm schmaler und rund 40 Gramm leichter. Ein iPhone Max vielleicht zu groß. Alle (!) iPad‘s erlauben lokal und remotes arbeiten. Mit Tastatur sogar recht komfortabel. Für entspanntes Arbeiten sollten allerdings die Mac‘s und MacBook‘s bevorzugt benutzt werden. Aktuelle M1er bringen zur Zeit kaum Vorteile eher noch einige Kompatibilitätsprobleme. Also auch hier entspannt abwarten. Zwischenzeitlich noch mit RASPI4 experimentieren. Software Werkzeugkasten ist zudem gut gefüllt.**

> The 12 Mini and the 13 mini both come in at 64.2mm wide x 131.5 high. Where the 12 was 7.4mm deep the 13 mini is 7.65 deep and weighs 40 grams more at 173 grams to the previous phone’s 133 grams. More on this later. So apart from the extra depth and slightly greater heft, the iPhone 13 mini is identical and almost indistinguishable (on the outside at least) from its forbear.

Abmessungen und Gewicht2  • Breite: 64,2 mm • Höhe: 131,5 mm • Tiefe: 7,65 mm • Gewicht: 140 g

Apple iPad Mini 6 (2021): Datenblatt Bildschirmdiagonale 8,3 Zoll Arbeitsspeicher 4 Gigabyte Abmessungen 195,4 x 134,8 x 6,3 Millimeter Interner Speicher 64 / 256 Gigabyte Gewicht 297 Gramm

**Sep 2021 Installation Python etc**

* **CoCalc** ist via APP, Browser oder SSH immer erreichbar (+Alternativen z.B. **Deepnote**)
* von iPhone, iPad, MacPro, MacBook einfach erreichbar
* also nur 1x pflegen: shell, vim, python, jupyterlab
* Lokal dann Apps wie Pythonista oder das neue lab, Carnets etc. Mit wenig konfigurieren und pflegen. Als Spielwiese dann eher virtuelle Maschinen nutzen.
* Schwierig wird es bei grundlegenden Änderungen wegen den Reflexen. **Daher wenig(er) Re-Mapping**

—

**Sep 2021 iPhone 13 / iPad Mini 6 Event:**

* 13er Mini ist **jetzt** akzeptabel, ggf. Downsizing (falls Ersatz nötig). Da aber mein 11er pro noch sehr ok ist wird es leider KEIN 13er Mini geben.
* 13er Pro bleibt Kompromiss, aber **improved** (Nits, Bat.,Screen, Foto z.B. Makro)
* iPad Mini 6, es fehlte noch ein Keyboard (kein Anschluss) & OLED & A16+ & 2TB, aber arbeitsfähig wie 4er. Als Terminal zu teuer. ABER: Transportable und leicht. Neues case wie 11er Pro ok und chic: Sofort einsatzfähig, **aber altes iPad 4 Mini genauso.**
* Jetzt noch Macbook Pros und neues Air **abwarten** (und weiter Bedarf testen)
* Weiterhin iPhone 14/15 im Blick da leichter, schneller, kleinere Kamera und bessere Laufzeit
* Jederzeit Rückgriff auf 13++ Modelle aus Kostengründen
* **Mini oder Max** wird immer die Frage bleiben

So das ist kleiner Test wie es mit dem Pro 11“ und einem kleinem Keyboard so läuft. Auch hier ist die Bildschirmtastatur ausreichend. Also 11“ sind dann doch angenehme Verhältnisse. Das macht es dem Mini dann doch schwer. AHA noch kein neues Multitasking. Ich denke … aha Center Stage wird es wohl so auch nicht geben. Also Mini ist ok, sogar das alte 4er. Aber mit 11“ und Position wie mit Magic Keyboard ist schon echt arbeitsfähig. Ich habe zur Zeit allerdings eine Tastatur dran die eher dem 12,9 Zoll entspricht. Damit kommt man dann in Notebook Reichweite. Aber der erhöhte Bildschirm ist dann doch sehr ergonomisch da näher vor den Augen. So ein 12“ iPad mit Magic Keyboard kommt nicht in Frage, da die Größe und das Gewicht ein MacBook Air entspricht. Zusätzlich weniger Laufzeit. Im 11“ liegt der Vorteil jedoch in der Größe und der Nachteil in den inkompatiblen Programme (Unix). Das neue Mini ist noch leichter und am besten mit Bildschirm oder BT-Tastatur wenn nötig. Ich vertraue dem Magic Keyboard nicht wegen der engen Tastatur. Ständig hauen die Finger gegen das Pad und die Zahlenreihe ist verdeckt. Jetzt mal noch ein Test mit der angesteckten Mini-Tastatur von ARTECK Da auch das Mini 4 noch gut funktioniert heisst die Devise eher abwarten, ggf. nur Ersatzbeschaffung.

> Allerdings passt das 12.9er dann nicht überall mit. Hab gerade mal das 4er ohne Tastatur ausprobiert - ist immer noch ok. Ich denke aber ein 11er wird mehr Spaß machen wegen des besseren Bildschirms. Mit Magic Keyboard aber nur indoor z.b. im Café. Sozusagen dann doch alternative zu Notebook … von der Ergonomie her betrachtet die (Reise-) Zukunft. Kein Logitec wegen eben dieser Ergonomie…

So nochmal ein test mit iPad mini. So für unterwegs würde es schon gehen.

—

## Die ganze Welt im iPhone oder iPad

* ✅ **Blink** (Backup **Shelly**) mit **CoCalc:** Hier stimmt aktuell etwas nicht mit LTE und VPN. Außerdem WOL prüfen.
* **iSH** mit Bash - langsam (Faktor 20-100 langsammer) mit Python aber für Skripts reicht es. Das geht jetzt aber auch mit **CoCalc** jedoch online.
* **LibTerm** keine Weiterentwicklung dafür guter C Compiler aus selben Stall.
* **c++** Compiler IDE vielversprechend.
* ✅ **A-Shell** incl. **Vim** und **C** - weiter in Entwicklung und Top!
* **iVim** (offen) ggf. mit **Pyto** - hier ist noch einiges zu fixen. Aber vielversprechend. **bis auf Abonnement - das ist ein no go**
* ✅ **Pythonista** noch Potenzial! Echter Schub durch **STASH Schell**
* **Pyto** wird auch besser.
* **Juno** und **Carnets** in Entwicklung.
* Etliche **IDEs** und **Editoren** für C/Lua/Colab u.a.
* ✅ **Taio** u.a. **Textsysteme** & **Notizen** Apps (Achtung OS 15 Kompatibilität)
* ✅ **JUNO connect** mit **CoCalc** - tolle Entwicklung neue Perspektiven!
* Spaß: iDOS2 (noch) installiert. Ernst: MASM usw. mal testen auf iPad mit Tastatur
* Überlegung: Power iPadOS ausnutzen via Swift Playground -> noch testen

> Alle **Aufgaben** und **Anwendungen** sind machbar. **Konsum** von Inhalten und **Organisatorisches** sowieso. Einiges besonders gut dank **CoCalc**, jedoch nur online. Handy immer stärker im Vorteil u.a. **800 nits.** Da kommt ein Tablett nicht mit zur Zeit. Das Pro ist Kompromiss in Gewicht und Größe. Das Max wäre vermutlich besser. Vom tippen und Batterie her betrachtet. Sieht man am fast gleich großen 7 Plus. iPad mini mit iPadOS 15 eingerichtet. Gut zum arbeiten. Ein iPad 11 mit Tastatur ist dann ein Notebookersatz obwohl nur MacBooks vollwertig sind wegen Unix! Größtes Problem ist der Nacken und der Tennisarm (Cellbow) beim längeren Arbeiten und Konsum von Medien. Daher bevorzugt Desktop und Notebook benutzen, lesen möglichts eInk-Reader. Auch bei Schulung besser. iPhone/iPad möglichst nur Mobil oder im Urlaub sowie auf der Couch oder im Garten (wegen der Sonne )verwenden.

_**Wenn überhaupt dann müsste es ein 13er besser 14er Pro oder Max in 2022 sein oder nächster Schritt iPhone 15 (S Variante) Pro/Max und MacBook Air 2.Generation, denn alles wird besser in 2023 sein. Allenfalls ein 13er MINI als „Lüstling“ 2021/22 vor Urlaub das jetzt auch 800 nits bringt!**_

### Ergebnise (tldr):

* Neu: **CoCalc Kein Problem3 mehr mit 3$/mtl.:** Sonst per SSH ins Terminal zu kommen (wichtig für‘s iPhone) muss man eingeloggt sein via WEB-Browser oder Juno. Und das 30 Minuten Timeout ist nervig! Erledigt durch neue Lizenz. Noch testen wie Lizenz und Projekt zusammenpassen. Ggf. Etwas teurer (60€pa)! Lizenzen sehr flexibel.
* Python: Speed ähnlich wie M1 und doppelt so schnell wie MacPro außer (iSH).
* Alles Stand Alone (außer Blink und CoCalc) möglich.
* Fenster ca 45x30 quer 9x100 ok. Achtung Einstellung Fit und Fond 13!
* ggf. breitere Tastatur und Schirm & Batterie mit iPhone Max 11, 12 oder 13-15
* Tastatur schwach aber man kann sich dran gewöhnen (nur iPhone hier vorteilhaft da iPads alle anders belegt sind was nervt).
* Pythonista gutes GUI spanende iOS Erweiterungen!
* ggf. auf iPads (Mini) oder Mac nahtlos weitermachen.
* Auch Jupyter möglich! Stand alone oder via CoCalc. Viele unterstützte Kernel.
* Fokus auf alles (Produktion & Konsum) auf dem Phone!
* C geht auch - Speed getestet. Mit WASM: ca. Faktor 3,2 langsamer als MacPro (25:80 Minuten) -> ok aber zieht auch mächtig am Akku!
* Gerade die Microsoft SwiftKey Tastatur entdeckt. Gut zum programmieren. Aber alles nicht optimal. Weitersuchen oder akzeptieren.
* Für Textverarbeitung kann auch voice Eingabe gut sein. Genaue Satzzeichen noch rausfinden und üben!

### Ziel

* Lernen
* Spaß
* Konfigurieren
* Schnipsel in Bash und Python/Jupyter
* Dokumentation und/oder neues Buch

### Folgen

1. Später iPhone Max auch wegen Batterie wahrscheinlich Minimum ein Pro (die 13er sind NOCH besser) aber vielleicht reicht auch mein aktuelles 11er. Tippen geht immer besser. Wohl kein MINI mehr (nits), Schade!
2. iPad Mini und / oder 11er besser 12/13er Pro (Max) denkbar
3. Weiter testen bevorzugt mit Terminal und diverse Geräte
4. 2021++ Fokus Doku & Test & lernen
5. Auch mehr mit iPhone 7plus probieren (Tastatur ähnlich Max). Achtung Bild ist wie bei Max und Anleitung wie man Umlaute ausschaltet für breitere Tastatur beachten. Vorerst ggf doch kein neues Phone? Kann mit dem plus's im Garten sitzen!
6. Das neue MD Programm macht echt was her: Loseblatt - Sammlung damit anlegen und somit editieren üben (ein Finger) - aber jetzt auch neue Mac-Version

### Fazit …

Wenn ich mit dem Pro zurecht komme (testen testen testen) sollte ich mir ein Max zur Zeit verkneifen. Auch Zeitpunkt schlecht: sofort macht Sinn. Neues 13er aber erst September. Dito Sommerproblem 2022. macht dann erst Anfang 2022 (ggf. 13er vor Winterurlaub) oder erst Anfang 2023 oder sogar 2024 Sinn! Diesen Sommer und Winter kann das 7 Plus retten. Also Geld sparen. Und gerade festgestellt: zum 7er hab ich noch ein Batteriecase.

**Also 7er reaktivieren!**

**Achtung Urlaub**: 13er haben fette Kamera und 120er Schirm nicht nötig, aber 13er macht Sinn für Urlaub(e) wieder ab 2022 ⚠️

***

## Zukunftsgedanken

Wenn SaveTV und Livedrive erledigt sind wird der MacPro nicht mehr durchgängig laufen. Stromkosten sind dann mehr als gemieteter Server. **Alternativ zu CoCalc** Mac Mini oder (doch) Mini PC oder RASPI4 🍓 im Netz für Shell etc. und primär Python mit Vim (via Blink). Ein RASPI4 🍓 könnte direkt an der FritzBox hängen … Unwahrscheinlich, da CoCalc gut und preiswert und vor allem Unabhängig. Jedes Terminal/Browser reicht.

So hier nur noch Test mit **iPhone 7 Plus!** Einfach besseres Format. Das 12s bzw. 13er wird teuer. Aber es sollte dann bis zum 15ner reichen. Daher jetzt kein Upgrade. Oder gerade doch? Denn das 11er ist nicht schlecht. Könnte man dann aber auch im Winterurlaub 2022 machen.

**Alternativ:** Es könnte sich durch einbeziehen des iPad Minis herausstellen, daß 2x Mini bzw. iPhone Pro und iPad Mini die geeignetste Kombination fürs digitale Hobby/Leben ist! Zum Mini gibt es dann ggf. auch noch Tastaturen. Das Mini läßt sich zudem prima auf dem Schoß tippen. So wird auch die Hand entlastet.

Dann also auch abwarten und kein Pro Max kaufen, denn das 7 Plus ist nur 0,03 schmaler als 11 Pro Max und 0,28 als 12 Pro Max. Und das 12er Pro ist wiederum doch 0,38 weniger als das 7 Plus aber schon besser zu tippen als 11 Pro obwohl nur 0,22 breiter als 11er Pro. Also zur Arbeit im Garten und auf dem Sofa tut es das gute alte 7 Plus noch eine Weile.

### Fakten Fakten Fakten

Das iPhone 11 Pro Max Display hat gerundete Ecken, die den Kurven des Designs folgen und sich innerhalb eines normalen Rechtecks befinden. Als Standardrechteck gemessen hat das Display eine Diagonale von 6,46" **(16,40 cm).**

Das iPhone 12 Pro Max Display hat gerundete Ecken, die den Kurven des Designs folgen und sich innerhalb eines normalen Rechtecks befinden. Als Standard­rechteck gemessen hat das Display eine Diagonale von 6,68" **(16,95 cm).** Der tatsächlich sichtbare Displaybereich ist kleiner.

Kein Pro Max vor Anfang 2022 !!! Achtung iPadOS 15 wird Super !!!

***

5,76 Mini 12er 0,5 schmaler als 11er Pro 5,84 iPhone 8 !

6,46 12er pro und normal 0,38 zum 7plus 7,12 12er pro Max auch 13er Pro Max x 15,4 hoch

6,24 11er pro + 0,22 12er (0,88 12er Max) 0,6 zum 7Plus

6,89 11 Max +0,23 zu 12er Max 6,45 XR 6,89 XS Max

6,84 7plus !!!! + 0,28zu 12er Max **(nur 0,3 schmaler als 12 Max)** und nur 0,05 zum 11er Max!!!

On the iPhone 7 Plus it reaches 618 nits, which is right around Apple's claimed 625 nits. The iPhone 7 goes above and beyond, hitting 706 nits in the boost mode, which is 13% higher than what is advertised. Each of the iPads has a similar max brightness, measuring in at 415 cd/m2 (nits) for the iPad Air 2, 424 nits for the iPad Pro, and 450 nits for the iPad mini 4.

**Achtung 13er nits prüfen!**

***

#### iPhone 12 mini

Breite: 64,2 mm Höhe: 131,5 mm Tiefe: 7,4 mm Gewicht: 133 g

625 Nits maximale typische Helligkeit, 1200 Nits maximale Helligkeit (HDR) (625 entsprechen 7 plus - zu wenig)

#### iPhone 11 Pro

Abmessungen 144 x 71.4 x 8.1 mm Gewicht 188 Gramm

#### iPhone 12 Pro

Breite: 71,5 mm Höhe: 146,7 mm Tiefe: 7,4 mm Gewicht: 187 g

800 Nits maximale typische Helligkeit, 1200 Nits maximale Helligkeit (HDR)

#### iPhone 12 Pro Max

Breite: 78,1 mm Höhe: 160,8 mm Tiefe: 7,4 mm Gewicht: 226 g

#### iPhone 7Plus

Höhe: 158,2 mm Breite: 77,9 mm Tiefe: 7,3 mm Gewicht: 188 g

5,5" Widescreen LCD Multi-Touch Display (13,94 cm Diagonale) mit IPS Technologie 1920 x 1080 Pixel bei 401 ppi Typisches Kontrastverhältnis: 1300:1 Display mit großem Farbumfang (P3) Maximale typische Helligkeit: 625 cd/m²

#### iPhone 11 Pro Max

Breite: 77,8 mm Höhe: 158,0 mm Tiefe: 8,1 mm Gewicht: 226 g

6,5" All‑Screen OLED Multi‑Touch Display (16,5 cm Diagonale) HDR Display 2688 x 1242 Pixel bei 458 ppi Typisches Kontrast­verhältnis: 2.000.000:1 True Tone display Display mit großem Farbraum (P3) Haptic Touch 800 Nits maximale typische Helligkeit 1200 Nits maximale Helligkeit (HDR)

#### Externer Accu

```
•	MagSafe Batterie – 11,13 Wh
•	iPhone 12 mini – 8,48 Wh
•	iPhone 12 – 10,73 Wh
•	iPhone 12 Pro – 10,73 Wh
•	iPhone 12 Pro Max – 14.05 Wh
```

Damit könnte die MagSafe Batterie also auch ein iPhone 12 Pro problemlos vollständig laden? Nein. Trotz der höheren Kapazität kann dies sogar für das iPhone 12 mini knapp werden. Der Grund dafür ist in der Ladetechnologie zu suchen. Das drahtlose Laden ist nicht sonderlich effizient, da Energie in Form von Hitze verloren geht. Experten sprechen hier von bis zu 50 Prozent Verlust, wobei Apple perfekte Ausrichtung durch MagSafe natürlich den Prozentsatz reduzieren dürfte, sodass mehr Energie im iPhone ankommt. Unterstützt wird dies durch ein intelligentes Lademanagement, das auch die Temperatur im Auge behält und damit die Effizienz nochmals erhöht.

> Das iPhone 13 Pro Max erreichte mit seinen großen Akku den Spitzenplatz und hält 9 Stunden und 52 Minuten bei ununterbrochener Nutzung durch. Der YouTube-Kanalbetreiber betonte, dass dies das bisherige Top-Ergebnis aller bisher getesteten Smartphones sei. Wer also ein Smartphone mit extremer Akkulaufzeit sucht, braucht das iPhone 13 Pro Max. Das hat allerdings auch mehrere Nachteile: Es ist ziemlich groß und es ist sehr teuer. Das kleinste Modell der neuen Serie ist das 5,4 Zoll große iPhone 13 mini. Es hielt immerhin noch 6 Stunden und 26 Minuten aus. Das iPhone 13 kommt auf eine Akkulaufzeit von 7 Stunden und 45 Minuten. Das sind fast zwei Stunden mehr als das iPhone 12, das 5:54 aushielt. Das iPhone 13 Pro kommt im Test von Mrwhosetheboss auf eine Laufzeit von 8 Stunden und 17 Minuten. Um den Fortschritt einmal zu dokumentieren. Das iPhone 11 kam auf 5:08 Stunden, das iPhone 11 Pro erreichte 7:36 Stunden, das iPhone 12 Pro auf enttäuschende 6:35 Stunden.

#### A-Shell

* iPhone 7plus 50% Batterie nach nur einer Stunde bei 100% Helligkeit (2 Std.)
* iPad mini 4 mit iOS 15 40% und vim only 20% pro Stunde (5 Std.)
* **iPhone 11 Pro 8% Verbrauch für eine Stunde (!) bei 100% Helligkeit (12 Std.)**
* iPad Pro 2020 bei 100 Prozent Helligkeit 10% je Stunde (10 Std.)

#### Blink

* iPhone 7plus 20% bei 100% in einer Stunde (5 Std.)
* iPad mini 4 mit iOS 15 10% in einer Stunde (10 Std.)
* **iPhone 11 Pro 3% bei 100% Helligkeit in einer Stunde weniger als gedacht (25-30 Std.)**

### Abwegen

* Breitegewinne minimal (Max)
* Mini leider viele Nachteile
* iPad Mini und echter Bedarf unbekannt
* Besser weniger mit Handy arbeiten
* Alle Geräteklassen vorhanden
* Handys (OLEDs & ACCU) im Vorteil!
* **Berücksichtige 5G in ca 2 Jahre!**
* **11 Pro ist (noch) guter Kompromiss**
* **Warten 15 Pro (Max/S) in 2 Jahre**
* **Und: Neues Max zuerst für Petra**

### Mitspieler M1

* Aktuelles MacBook Air M1 insgesamt so schnell MacPro (Multicore) und doppelt so schnell pur (Singlecore) aber gleich schnell mit iPhone!
* Macbook Air etwas zu groß und etwas zu schwer im Vergleich 12er Macbook (Batterie noch 6 von 8 Std. und Speed 50% geht noch so)
* Harald hat alles (ausser mini's und max zum spielen) auch dank cocalc
* **Auch hier neue Generationen (Air und Pros) abwarten falls nötig**
* **iPhone zuerst an neues MAX für Petra denken**
* Denke eher **keine Aufrüstungen und Reparaturen** mehr (altes iPad Batterie/LCD?, ~~MacBook Batterie~~, ~~MacPro SSD reicht~~ -> X mal 500,- und mehr -> iPhone's / Mini6 / M1)

https://www.gq-magazin.de/video/watch/unboxing-apple-iphone-12-mini-12-pro-und-12-pro-max-im-vergleich-gq-germany

### iPhone SE Model 2022

Abmessungen und Gewicht2 • Höhe: 123,8 mm • Breite: 58,6 mm • Tiefe: 7,6 mm • **Gewicht: 113 g**

Display • Retina Display • 4" Widescreen LCD Multi-Touch Display (10,16 cm Diagonale) mit IPS Technologie • 1136 x 640 Pixel bei 326 ppi • Typisches Kontrastverhältnis: 800:1 • Maximale typische Helligkeit: 500 cd/m² • Voller sRGB Farbstandard • Fettabweisende Beschichtung • Unterstützung für die Anzeige mehrerer Sprachen und Zeichen gleichzeitig

> Identisch mit iPod touch 5cm breiter Schirm bei 88 Gramm

## Stromkosten vs Server

Stromkosten (und Lärm) Server laufen rund um die Uhr. Ein Jahr hat 8760 Stunden; ein Watt kontinuierlicher Leistungsaufnahme führt also zu 8,76 Kilowattstunden (kWh) auf der Jahresrechnung. Die kosten 2,63 Euro, wenn Sie pro kWh 30 Cent bezahlen. Für 5, 10, 15, 25 oder 50 Watt werden folglich rund 13, 26, 40, 66, 130 Euro fällig. Server für kleine Netze verbringen die meiste Zeit im Leerlauf. Das ist der wichtigste Betriebszustand für die Energiekosten. Selbst wenn man zwei Stunden tägliche Volllast ansetzt – bei einem NAS mit 90 MByte/s Datentransferrate entspricht das mehr als 300 GByte an übertragenen Daten –, sind das bei 230 Werktagen nur fünf Prozent der jährlichen Betriebsdauer. Energiesparfunktionen senken den Bedarf, etwa die automatische Abschaltung von Festplattenmotoren (Spindown). Eine 5400-Touren-Platte braucht im Leerlauf ohne Zugriffe 4 bis 5 Watt, bei stehender Spindel nur 0,8 bis 2 Watt. Unscheinbare Erweiterungen können aber den Stromverbrauch erheblich steigern. Einige RAID- und SAS-Hostadapter erhöhen die Leerlaufleistung um 15 bis 20 Watt. Manche externe (USB-)Platte im 3,5-Zoll-Format frisst 8 Watt oder mehr. Wartungsfunktionen wie ein RAID-Rebuild können sehr lange dauern, bei 20 TByte zum Beispiel einen ganzen Tag \[10]. Typische Fertigserver mit Fernwartung sind für Dauerbetrieb ausgelegt: Sie benötigen mehrere Minuten zum Booten und beherrschen Stromsparmodi wie Suspend-to-RAM (ACPI S3) und Suspend-to-Disk (S4) nicht. Aufwecken bei Bedarf per Wake-on-LAN (WoL) ist dann unpraktisch.
