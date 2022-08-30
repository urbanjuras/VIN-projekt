# VIN-projekt
## Vremenska postaja Arduino


![VremenskaPostaja](https://user-images.githubusercontent.com/74730730/186911517-553fd865-cd43-4907-b625-8e57805e6d44.jpg)


### Potrebščine:
- Arduino Uno
- breadboard 
- kabli za povezovanje
- I2C OLED zaslon
- DHT senzor za vlago in temperaturo

### Postopek:
Sprva sem moral povezati vse komponente z Arduino Uno ploščico. Sepravi povezava z GND in povezava z napetostjo, v mojem primeru je bila ta 5V napetost. 
Naslednji korak je bil pravilno povezati temperaturni senzor in sicer na breadboardu GND z GND in 5V s 5V ter OUT povezavo na senzorju z sprejemnikom A0.
Zadnja stvar pa je bila zvezava I2C OLED zaslona. To je predstavljal malo bolj zapleten del tega projekta, saj sem moral vsak "pin" povezati s pravim na Arduinu. 
Nakoncu je to izgledalo tako:
- GND -> GND
- 5V -> 5V
- D0 -> 10
- D1 -> 9
- RES -> 13
- DC -> 11
- CS -> 12

### Delovanje
Naša vremenska postaja preko senzorja za temperaturo in vlago zajame ta dva podatka. Vendar brez ustrezne kode se ne bi zgodilo nič. Oba podatka moramo prikazati
na zaslončku. To smo naredili s funkcijami iz knjižnjice za naš I2C OLED zaslon. Temperaturo in vlago pa smo dobili iz DHT knjižnjic.

### Končen produkt
![Video_MOV_AdobeExpress](https://user-images.githubusercontent.com/74730730/186915828-ee5e2fe2-f0b5-4c9f-b9d2-c916ee9f60da.gif)
