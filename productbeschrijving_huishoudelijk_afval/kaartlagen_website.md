# Kaartlagen op data.amsterdam.nl

Een deel van de gegevens betreffende ondergronds afvalcontainers zijn opgenomen in de kaart van data.amsterdam.nl
De volgende kaarlagen zijn beschikbaar.

## afvalcontainers

| **kaartlaag**                        | opmerking                                                             |
|--------------------------------------|-----------------------------------------------------------------------|
| Restafval                            | bestaand                                                              |
| Papier                               | bestaand                                                              |
| Glas                                 | bestaand                                                              |
| Plastic                              | bestaand                                                              |
| Textiel                              | bestaand                                                              |
| GFE                                  | bestaand                                                              |
| Brood                                | nieuw                                                                 |
| onbekend                             | nieuw                                                                 |
| PMD                                  | nieuw                                                                 |
| Grof                                 | nieuw                                                                 |


## afval loopafstanden pand

| **kaartlaag**                        | opmerking                                                             |
|--------------------------------------|-----------------------------------------------------------------------|
| Restafval [0-30-90-120-150-210-1000] | Zie uitwerking afstandsklassen, nog valideren met frequentieverdeling |
| Papier  [0-30-90-120-150-210-1000]   | Zie uitwerking afstandsklassen, nog valideren met frequentieverdeling |
| Glas  [0-30-90-120-150-210-1000]     | Zie uitwerking afstandsklassen, nog valideren met frequentieverdeling |
| Plastic  [0-30-90-120-150-210-1000]  | Zie uitwerking afstandsklassen, nog valideren met frequentieverdeling |
| Textiel  [0-90-180-300-480-1000]     | Zie uitwerking afstandsklassen, nog valideren met frequentieverdeling |


## Attributen kaartlaag afvalcontainers

| attribuut          | omschrijving                                                                 | categorie             |
|--------------------|------------------------------------------------------------------------------|-----------------------|
| container_id       | Uniek identificerend kenmerk van het object                                  | metadata              |
| cluster_id         | Uniek identificerend kenmerk van cluster waaraan de container is gerelateerd | metadata              |
| datum_plaatsing    | Datum waarop het object op de locatie is geplaatst                           | metadata              |
| datum_operationeel | Datum dat de container operationeel is voor het aanbieden van afval          | metadata              |
| afvalfractie       | Type afvalfractie waarvoor de container is bedoeld                           | functioneel attribuut |
| volume container   | inhoud container in m3                                                       | functioneel attribuut |
| container type     | type container volgens de fabricant                                          | functioneel attribuut |

## Attributen loopafstanden pand

| attribuut          | omschrijving                                                        | categorie             |
|--------------------|---------------------------------------------------------------------|-----------------------|
| object_id          | Uniek identificerend kenmerk van het object                         | metadata              |
| peildatum_gegevens | datum afleiding loopafstand                                         | metadata              |
| object_type        | type obect {pand, ligplaats, standplaats}                           | functioneel attribuut |
| afvalfractie       | Type afvalfractie waarvoor de container is bedoeld                  | functioneel attribuut |
| loopafstand        | berekende afstand over de weg in meters naar meest nabije container | functioneel attribuut |

## Indeling loopafstanden
Uiteraard bestaat er variatie in de loopafstanden. Deze afstanden zijn verdeel in zgn. klassen.
De onderstaande geeft de indeling van deze klassen weer.

**Voor de afvalfracties restafval, papier, glas en plastic**

| categorie_omschrijving | categorie_afstand_vanaf | categorie_afstand_tot |
|------------------------|-------------------------|-----------------------|
| uitstekend             | 0                       | 30                    |
| zeer goed              | 30                      | 90                    |
| goed                   | 90                      | 120                   |
| voldoende              | 120                     | 150                   |
| onvoldoende            | 150                     | 210                   |
| zeer onvoldoende       | 210                     | 1000                  |
| buiten bereik          | 1000                    | -                     |
| geen afstand           | null                    | null                  |


**Voor de afvalfractie textiel**
| categorie_omschrijving | categorie_afstand_vanaf | categorie_afstand_tot |
|------------------------|-------------------------|-----------------------|
| uitstekend             | 0                       | 90                    |
| zeer goed              | 90                      | 180                   |
| goed                   | 180                     | 300                   |
| voldoende              | 300                     | 370                   |
| onvoldoende            | 480                     | 100                   |
| zeer onvoldoende       | 1000                    | -                     |
| geen afstand           | null                    | null                  |
