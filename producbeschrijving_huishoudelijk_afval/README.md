# Productbeschrijving huishoudelijk afval

## Context
Deze datasets beschrijven de gegevens over onder- en bovengrondse afvalcontainers, hun locaties en afvalfracties.
Alle data wordt dagelijks geactualiseerd.

De data wordt in de volgende vormen beschikbaar:
- rest api (Beta versie)
- OGC WFS (gebruik GIS software)

  
## Productinhoud
De productinhoud is voor alle vormen gelijk, per vorm kan de data anders zijn geordend.

 - [productinhoud afvalcontainers](productinhoud_afvalcontainers.md)
 - [productinhoud container clusters](productinhoud_afvalcontainer_clusters.md)
 - [productinhoud weeggegevens](productinhoud_afval_wegingen.md)

## Populatiekarakteristieken
De producten die beschikbaar zijn bevatten actuele gegevens en (nog) geen historie. De weeggegevens zijn hierbij de uitzondering, deze bevatten alle wegingen vanaf 1 januari 2016.
Afgerond bevat de dataset de volgende aantallen:
 - containers: 13.900
 - containerClusters: 5678
 - wegingen 2016 - 2019: 1.028.787

## Geografische afbakening
De producten bevatten alle gegevens binnen de bestuurlijke gemeentegrens van Amsterdam

## gegevensmodel
Het gegevensmodel representeert de samenhang tussen objectklassen uit het domein afval en gerelateerde entiteiten. Dit model vormt de basis van alle dataproducten die hieruit (kunnen) worden afgeleid.
De samenhang tussen de objecten is gebaseerd op basis van thematische voorwaarden, ruimte en tijd (historie).
Voor een grafische weergave van het model zie [logisch gegevensmodel integratie](logisch_gegevensmodel_integratie.md)

## Beschikbare productvormen

# Tekengescheiden bestand
Voor elke 'tabel' in de dataset is een csv bestand beschikbaar. Deze bestanden voldoen aan de volgende specificaties:
- inhoud: zie productinhoud
- karakterset: UTF-8
- scheidingsteken: semicolon `;`
- kopregel: Ja

### Definities objectklassen


#### afvalcontainer
Conform IMBOR luidt de definitie als volgt:
Boven- of ondergrondse bak voor de inzameling van afvalstoffen die duurzaam met de aarde verbonden is.

#### put (well)
Een betonnen constructie voor de borging van ondergrondse afvalcontainers.

#### afvalcontainer cluster
Een afvalcontainer-cluster is een locatie waar 1 of meer afvalcontainers zijn geplaatst van 1 of meer afvalfracties.
De ondergrondse containers zijn geplaatst in putten, de bovengrondse zijn niet gemonteerd op putten. De containers zijn gerelateerd aan 1 containerlocatie van het type put/well of bovengronds.
Het cluster is afgeleid uit een verzameling van 1 of meer containerlocaties en is op basis van de volgende condities opgebouwd:
 - de maximale onderlinge afstand tussen het middelpunt tussen de nabijgelegen wells is gelijk of kleiner dan 12 meter.
 - de maximale grootte van een cluster bedraagt ook 12 meter
 - een cluster wordt niet doorsneden door een weg van het type rijbaan. Hierbij is de rijrichting niet van belang.


#### Weeggegevens
De wegingen worder per container uitgevoerd. Vanaf 2016 zijn er weeggegevens beschikbaar.
Een beperking is wanneer er meerdere containers van dezelfde fractie bij elkaar staan niet kan worden geidentificeerd welke weging op welke container betrekking heeft.
Van de volgende fracties worden wegingen uitgevoerd:
 - Rest    
 - Papier  
 - Plastic 
 - Glas    
 - Grof    
 - PMD     
 - Textiel 
 - GFT     
