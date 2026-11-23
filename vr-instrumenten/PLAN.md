# VR-instrumenten: plan

Werktitel. Een VR-game waarin je allerlei instrumenten met je handen bespeelt: gitaar, piano, drums en meer. Om te oefenen, of gewoon voor de lol, zonder dat iemand anders er last van heeft (geluid via de koptelefoon of de speakers van de bril).

## Waarom VR

Lightstrings (in deze repo) liet zien waar een laptopcamera tekortschiet: geen diepte, wazig bij snelle bewegingen, handen vallen uit beeld. Een VR-bril meet je handen in 3D met meerdere camera's. Je raakt een snaar of toets pas als je vinger hem in de ruimte echt raakt, en dat maakt spelen geloofwaardig.

## Voor wie

- Mensen die een instrument willen proberen voordat ze er een kopen.
- Mensen die willen oefenen zonder huisgenoten of buren te storen.
- Iedereen die gewoon wil jammen voor de grap.

## Platform

- **Meta Quest** (3 / 3S / 2), in de browser via **WebXR**. Geen app store nodig: je opent een link in de Quest-browser.
- Hostbaar op GitHub Pages, net als Lightstrings (WebXR vereist https, dat heeft Pages).
- Tech: Three.js voor 3D, WebXR Hand Input voor handtracking (controllers als terugval), Web Audio voor geluid.
- Testen: met de Quest van een vriend, door de link te openen in de Quest-browser.

## Instrumenten

| Instrument | Hoe je speelt | Lastigste deel |
| --- | --- | --- |
| Lichtsnaren (Lightstrings in VR) | Snaren in de ruimte spannen en tokkelen | Eerste test van handtracking in 3D |
| Gitaar | Linkerhand houdt akkoorden op de hals, rechterhand tokkelt of slaat aan | Vingerposities op de hals herkennen |
| Piano / keyboard | Toetsen indrukken met alle vingers, aanslagsterkte telt | Precisie van losse vingers, toetsen niet per ongeluk raken |
| Drums | Stokken (controllers) of handen op pads en bekkens | Timing en lage vertraging |
| Later | Harp, xylofoon, theremin, bas | |

## Modi

- **Vrij spelen:** gewoon jammen, met keuze uit toonladders zodat het altijd goed klinkt.
- **Oefenen:** akkoorden, toonladders of een simpel liedje stap voor stap, met feedback (goed / te vroeg / te laat).
- **Ritme-modus:** noten komen op je af in de maat van een nummer en je speelt ze op tijd. Eigen ontwerp, geen kopie van bestaande games.
- **Opnemen en terugluisteren:** je eigen spel opnemen, later met loops.

## Wat we uit Lightstrings meenemen

- Plukken voelt pas goed als de snaar eerst meebuigt en pas daarna klinkt.
- Alleen de wijsvinger laten plukken voorkomt veel per ongeluk spelen; in VR kunnen er meer vingers bij, omdat diepte dan wel klopt.
- Gebaren met vasthouden (knijpen + even houden) voorkomen per ongeluk acties.
- Leeg beginnen werkt beter dan een vol scherm; geef uitleg op de lege plek zelf.
- Geluid zelf genereren (Karplus–Strong) klinkt goed voor snaren; piano en drums hebben samples nodig.

## Stappenplan

1. **VR-lichtsnaren:** Lightstrings ombouwen naar WebXR met handtracking. Doel: testen of tokkelen in 3D goed voelt op de Quest. Klein en snel te maken.
   *Status: gebouwd, staat in [`lichtsnaren/`](lichtsnaren/). Nog testen op een echte Quest.*
2. **Gitaar, vrij spelen:** gitaar in je handen, akkoorden kiezen op de hals, aanslaan met de andere hand.
   *Status: gebouwd, staat in [`gitaar/`](gitaar/). Akkoorden kies je met akkoordvakken op de hals (echte vingerposities zijn te fijn voor handtracking). Nog testen op een echte Quest.*
3. **Piano, vrij spelen:** keyboard op tafelhoogte, losse vingers, aanslagsterkte.
4. **Oefenmodus:** eerst voor gitaarakkoorden en pianotoonladders.
5. **Drums en ritme-modus.**
6. **Opnemen, liedjes, meer instrumenten.**

Elke stap levert iets speelbaars op dat je met de Quest kunt testen voordat de volgende begint.

## Open vragen

- Welke Quest heeft je vriend? Handtracking werkt het best op de Quest 3.
- Handen of controllers als hoofdbesturing? Handen voelen echter, controllers zijn preciezer (vooral voor drums).
- Instrumentgeluiden: zelf genereren, of gratis samples gebruiken (licentie checken)?
- Blijft het een browsergame, of later een echte Quest-app?
