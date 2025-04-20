# chatdbt

Kaip sukonstruoti AI agentą, kuris paimtų žmogaus užklausą ir ją paverstų duomenų rinkinio iš duomenų sandėlio?

* ???
* Sugeneruoti SQL kodą
* Paleisti SQL sandėlyje
* Gražinti rezultatą

Mano prielaida, jog dbt manifest.json yra puikus šaltinis suprasti vartotojo užklausą, susirasti panašų SQL kodą ir jį adaptuoti konkrečiam use case'ui.

Ką gali LLM išnaudoti?


Ko reikėtų?

* manifest.json parser'io
* Ar

Kaip prieiti prie problemos?

1. Vienas būdas yra manifest.json atverti kaip įrankių rinkinį, kurį modelis galėtų query'inti.
2. Kitas būdas yra parse'inti manifest.json ir sugeneruoti llm kontekstą - gali būti, jog tai reikalautų daug token'ų? Taip pat ar tikrai reikia viso konteksto iš pat pradžių, kai dažnai užklausai reikės 3 lentelių (visas manifest.json turi 600+ modelių)?

## Naivus būdas

1. Parse'inam visą manifest.json failą, jį pateikiame kaip prompt'o dalį - gali būti, jog tai reikalautų daug token'ų? Taip pat ar tikrai reikia viso konteksto iš pat pradžių, kai dažnai užklausai reikės 3 lentelių (visas manifest.json turi 600+ modelių)?

## Mažiau naivus būdas

Pirma paprašome, jog modelis susirastų aktualias lenteles? Gal reikėtų daryti fuzzy paiešką pagal raktinius žodžius modelių pavadinimuose, column pavadinimuose, descriptione, kode ir dokumentacijoje? Pagal tai tada LLM turi kontekstinius modelius, pagal kuriuos galėtų formuoti užklausą.



