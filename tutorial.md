# Åpne hemmelig boks!

## Steg 1

Vi må sette opp en radiogruppe, slik at microbiten vår kan snakke med microbiten inni boksen. 

Sett derfor opp ``[radio.setGroup(1)]`` inn i blokken, ved start.

```blocks
radio.setGroup(1)```

## Steg 2

Vi skal forsøke å finne de skjulte trykksensorene på boksen. Når du trykker på disse, vil det sendes et tall til din micro:bit. 

Derfor trenger vi å lage et program som kan vise disse tallene.

Finn frem blokken ``[radio.onReceivedNumber(function (receivedNumber)]``, og inn her settes en ``[basic.showNumber(receivedNumber)]``.

Last opp koden, finn knappene og skriv ned tallene du får!

```blocks
radio.onReceivedNumber(function (receivedNumber) {
    basic.showNumber(receivedNumber)
})```

## Steg 3

Nå som vi har funnet alle knappene, skal vi sende disse tallene tilbake til boksen. Dette vil gi oss løsningen på oppgaven!

Plasser en ```[radio.sendNumber()]``` for hvert tall du samlet inn, inni en ```[input.onButtonPressed(Button.A, function ()]```. 

```blocks
input.onButtonPressed(Button.A, function () {
    radio.sendNumber(2)
    radio.sendNumber(5)
    radio.sendNumber(9)
})```

## Steg 4



Derfor trenger vi å lage et program som kan vise disse tallene.

Finn frem blokken ``[radio.onReceivedNumber(function (receivedNumber)]``, og inn her settes en ``[basic.showNumber(receivedNumber)]``.

Last opp koden og send den tilbake til boksen!

```blocks
radio.onReceivedString(function (receivedString) {
    basic.showString(receivedString)
})```