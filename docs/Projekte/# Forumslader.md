## Nachbau (ShutterPrecision, Matteo)

_Vorschlag: erst nur Lader, dann kl. Powerbank ohne Schalter ohne LEDs, nur USB-PD/QC_

_Vorteil: schlank, mechanisch vereinfacht_

### Besorgungen

- Reichelt ([v.a. Lader](https://www.forumslader.de/fileadmin/user_upload/Individuelle%20Geraete/jensd/Download/UniladerUSB/Bestellnummern.txt))
    - [ ] Tuning- und Stütz-Elkos
        - 2x RAD FC 220/63
        - 1x RAD 105 1.000/25
    - [ ] Suppressor-/Zenerdiode
        - 2x 1,5KE 18CA
        - 2x 1,5KE 22CA
        - 1x ZF 15
    - [ ] Dioden (alles Hühnerfutter, wir messen die besten Dioden aus!)
        - 10x SB 120
        - 10x 1N 5817
        - 10x SB130
        - 10x 1N 5818
    - [ ] Schalter, Abdeckung
        - billig: GOOBAY 10023
        - besser: 1x MS 500H
        - Kappe finde ich keine bei Reichelt mit den Maßen (M6. 0.75), hab aber eine weiße vorrätig, Ebay: [https://www.ebay.de/itm/233188578079?mkevt=1&mkcid=1&mkrid=707-53477-19255-0&campid=5339002231&toolid=20006&_trkparms=ispr%3D1&amdata=enc%3A1cDu09VmiRYOBc-HvBcMuXQ21&customid=0a69f8938b9e1edeb88492c355539168&loc_physical_ms=129332&loc_interest_ms=&msclkid=0a69f8938b9e1edeb88492c355539168](https://www.ebay.de/itm/233188578079?mkevt=1&mkcid=1&mkrid=707-53477-19255-0&campid=5339002231&toolid=20006&_trkparms=ispr%3D1&amdata=enc%3A1cDu09VmiRYOBc-HvBcMuXQ21&customid=0a69f8938b9e1edeb88492c355539168&loc_physical_ms=129332&loc_interest_ms=&msclkid=0a69f8938b9e1edeb88492c355539168)
    - [ ] DC-Kupplung
        - DC-Hohlstecker & -buchse mit 2.1mm Stift, da gibt es bei Reichelt etliche, je nach Wunsch mit rundem Kabel oder Zwillingslitze. Kannst aber
- AliExpress (v.a. Powerbank)
    - [ ] ~~BMS~~
    - [ ] ~~3S USB Lader~~
    - [ ] Schalter mit wasserdichter Kappe
    - [ ] QC/PD USB Modul
    - [ ] LiPo Holder
    - [ ] USB Powermeter

### Variante

- Lenkerbefestigung/Tasche

## ToDo

- [ ] DC-Hohlbuchse aus Kunststoff statt Verschraubung
- DONE
    - [x] 3S mit Balancing
        - [x] Akkupack vorbereiten
        - [x] Diode einlöten
    - [x] Akkuanzeige bei USB-Anschaltung
    - [x] USB-Ladung einbauen
    - [x] LEDs lesbar grün/rot
    - [x] Gehäuse
    - [x] Schalterstellung markieren
    - [x] Kabel verlegen
    - [x] KontrollLeds
        - [x] Laden
        - [x] Unterspannung
    - [x] Input USB (StepUp auf 13V?)
    - [x] Gehäuse FL
    - [x] cockpit
        - elektronik
        - led laden/voll
        - kippschalter
        - festes kabel zum dynamo
        - steckbares kabel zur powerbank
    - [x] USB-PD?
    - [x] powerbank
        - 3s lipo
        - bms
        - batteriestandsanzeige extra button
        - usb normal
        - usb pd
    - [x] Output USB QC (Modul)
    - [x] benötigt
        - [x] Schalter
    - [x] LED bei Sonne
    - [ ] ~~Schalter drehen~~
    - [x] **Gehäuse**
    - [x] LED: sparsam, aber hell! (gelb wechseln)
    - [x] Amperemeter USB umschaltbar in/out mit Schiebeschalter direkt nach Akku
        - [x] USB-C Stecker mit Lötkontakt zum Anschließen
        - [x] Tests mit USBMeter
        - [x] Zerlegen
            - Erkenntnisse
                - gut kontaktierbar
                - Meter hochkant in Powerbank, sodass Display ablesbar und in/out gut abbildbar
                - Stecker dürfte abcutterbar sein
                - Plus wird durchgeführt, Minus mit Shunt
                    - minus immer durch Meter, Plus bei Bedarf anklemmen
            - [x] Anschlüsse (mit Menütaster)
            - [x] Test mit Meter
            - [ ] ~~USB-Lader mit Balancer, extra Balancer?~~
            - [x] Balancer im BMS
            - [x] BMS aktivierbar durch richtiges Einlegen?
    - [x] Schiebeschalter zum Anschalten des Meter
    - [x] Taster für Meter
    - [x] evtl. Schiebeschalter für USB

## Konzept

- **Lader und Powerbank als zwei separate Geräte**
- festes Kabel von Dynamo zu Lader, steckbares zur Powerbank
- Powerbank kann ohne Rad bei Ausflügen verwendet werden
- Powerbank kann zwischen Rädern oder [Riemengenerator](https://app.notion.com/p/Riemenlader-280c6558747481d8aba0d238f0cb24ea?pvs=21) getauscht werden
- BMS mit Balancing
- 3x wechselbare 18650er Li-Ion in Reihe
- Simultanes Laden (Generator, Solar, Steckdose) und Entladen (Telefon, Navigation)
    - 2x Entladen: USB 5V und USB PD
    - 2x Aufladen USB 5V@10W (PD: 15W) und 12V DC-Hohlbuchse
- Gemeinsamkeiten mit Forumslader
    Konzept, Schaltung und Bauelemente: Tuningkondensatoren, Spannungsverdopplung, Stufen manuell wählbar → Leistung au
- Unterschied zu Forumslader
    Li-Ion mit BMS, austauschbare Industriestandards, keine ineffiziente Linearregelung (Laderegler/USB), Zweiteilung: schlanker/leichter Lader am Rad, Powerbank portabel, multiple Lade-/Entlade-Möglichkeiten
    

## Leistung

_Bisherige Tests an Shimano DH3D72, Shimano DH3N72, ShutterPrecision SP PD-8_

- Zwischenstecker mit gut lesbaren Momentanwerten (Strom, Spannung)
    
    ![signal-2026-07-05-11-27-19-914.jpg](attachment:8edb0638-5502-445d-8574-9a960b5945b0:signal-2026-07-05-11-27-19-914.jpg)
    
- Messung der Momentanwerte
    
    - 12km/h: 200mA (2/3W)
    - 20km/h: 500mA (5/6W)
    - Spitze: >1000mA (10W-12W)
- Streckenszenario: 100km
    
    - 8.3hx200mA=~1.7Ah@12V, 4Ah@5V, 20Wh
    - 5hx500mA=~2.5Ah@12V, 6Ah@5V, 30Wh
- Streckenmessung: 70km
    
    - 22km/h, 17.5Wh
- Kapazitätsmessung gebrauchter Zellen bei einer Vollladung
    
    - 26.5/27Wh, 2.3Ah von 3.2V zu 12.4

# Lader

## Elektronik

- Schaltplan
    
    ![1000043755.jpg](attachment:f90ca9db-ae60-426a-a9ec-a776405fdc20:1000043755.jpg)
    
- linke Hälfte der Schaltung inkl. Diode (z.b. 1N5819), die LEDs von Powerbank trennt
    
- Fliegender Aufbau (ohne Platine) in zwei Stufen zum Platz sparen
    
    - oben: Brückenschaltung und Tuningkondensatoren
    - unten: Stützelko und Suppressordiode mit Thermoschalter

## Bauelemente

- LEDs (grün/rot): zwei einzelne statt Duo für bessere Identifizierung, Modelle stromsparende Signal- statt ScheinLEDs
- Kippschalter mit wasserdichter Kappe ([AliExpress](https://de.aliexpress.com/item/1005002470034011.html?spm=a2g0o.order_list.order_list_main.345.59c15c5frWqVr4&gatewayAdapt=glo2deu))
- Schottky-Dioden mit geringer Vorwärtspannung/geringen Verlusten

## Gehäuse

![[Pasted image 20261112172534.png|298]]![[Pasted image 20261112172553.png|395]] 
 

![[Pasted image 20261112172635.png|183]]

- mehrteiliger 3D Druck
- Werkzeugfreie Klemmung zwischen Lenker und Klickfix
- Clips anpass- und tauschbar, stabiler Druck in anderer Orientierung
- Schnittstellen
    - wasserdichte Kabelverschraubung zweier Rundkabel oder
    - offene Kabelaustritte für Feuchtigkeitsaustritt und zwei Zwillingslitzen
    - Kabel mit DC-Hohlstecker zur Powerbank
    - Kippschalter mit wasserdichter Kappe
    - 2x LED (3mm) wegen Streulicht (Sonne) versenken, Möglichkeit Abdichtung mit Epoxy/Sekundenkleber

## Powerbank

### Elektronik

- BMS mit aktivem Balancing ([BMS Modul, Aliexpress](https://de.aliexpress.com/item/1005001511789393.html?spm=a2g0o.order_list.order_list_main.75.59c15c5frWqVr4&gatewayAdapt=glo2deu))
- Laden
    - USB-C, QC/PD: (Überspannungsschutz der Ladeplatine bei Ladespannungen an Hohlbuchse über Ladeschlusspannung: Pluspol zwischen BMS und Akku, Minuspol am gemeinsamen Massepunkt zur Strommessung) ([Modul, Aliexpress](https://de.aliexpress.com/item/1005004846721350.html?spm=a2g0o.order_list.order_list_main.250.59c15c5frWqVr4&gatewayAdapt=glo2deu))
    - DC-Hohlbuchse
- Entladen
    - USB, 5V DCDC ([Modul, Aliexpress](https://de.aliexpress.com/item/1005006216365115.html?spm=a2g0o.order_list.order_list_main.80.59c15c5frWqVr4&gatewayAdapt=glo2deu))
    - USB QC/PD
- USB-Meter ([Modul, Aliexpress](https://de.aliexpress.com/item/1005009123526203.html?spm=a2g0o.order_list.order_list_main.145.59c15c5frWqVr4&gatewayAdapt=glo2deu))
    - Shunt des Meter sitzt zwischen allen Lade- und Entladevorgängen und dem BMS

### Akku

- Konfiguration: 3S1P: 9V (Entladeschlusspanunng) - 12.6V (Ladeschlussspannung)
- Kapazität: 3300mAh @ 10.8V = 36Wh

### Gehäuse

![00.png](attachment:f0696834-16be-4044-b9a8-7a2f49f60948:00.png)

![01.png](attachment:15761087-6af9-41f7-a40b-2b54d6a2cde4:01.png)

## Prototypen

??? note "Test"
	erfergre


???+ note "Meine Notizen"
    Dieser Bereich ist standardmäßig geöffnet.

> [!NOTE]- Meine Notizen
> Inner Bereich


### Lader und Powerbank

Erfahrung: Strom-/Energiezähler wäre der Akkuanzeige überlegen. Test am Atlantik.

![1000043775.jpg](attachment:d65d1f2d-f5c2-4dfc-ba95-1131fda75344:1000043775.jpg)

### All-in-One, Li-Ion

Erfahrung: Lose Verstauung in Gabeltasche suboptimal: Schalter gegen unbeabsichtigte Betätigung schützen, LED bei Sonnenlicht kaum erkennbar. Wunsch nach Trennung von Akku und Lader (Wanderung; Aufladung an Steckdose). Test in Skandinavien

![](attachment:9a91d39c-5b7d-4ebb-bd4e-251c100e829e:nse-2344099742115726083-1000043736.jpg)

![](attachment:27490683-f53f-433c-acbd-924e6b0c05cb:nse-1970005992075019229-1000043739.jpg)

![](attachment:a93fb1d9-4a6d-45a1-83c4-a0a4db0324d9:nse-6665184798726610918-1000043737.jpg)

![](attachment:a2620ea0-ffea-48a5-9278-963917fc3245:nse-1500071252589205020-1000043740.jpg)

![](attachment:4e338546-1a1c-4908-b6bf-00ba0d5df72b:nse-5411058561067116480-1000043738.jpg)

### All-in-One, NiMH

Erfahrung: schlechte Energiedichte. Wenig Gewinn trotz Größe und Gewicht. Test auf Balkan.

![1000043754.jpg](attachment:2dd1fb6d-fee0-43a8-ac5e-41487ee7893b:1000043754.jpg)

![IMG_20240912_163905.jpg](attachment:aac53176-61cc-4b43-8cdf-0d6fa0a25fd9:IMG_20240912_163905.jpg)

![IMG_20240912_163914.jpg](attachment:4077edc8-b65a-430c-9b3e-2a8c4d946da2:IMG_20240912_163914.jpg)

## Quellen

- [Forumslader](https://www.forumslader.de/aeltere-versionen-des-forumsladers/12v-version-mit-zusaetzlichem-usb)
- [Funktion](https://rad-forum.de/topics/764340) I, [Funktion II](https://www.rad-forum.de/topics/530892/forumslader_freaks_suche_step_down_wandl)