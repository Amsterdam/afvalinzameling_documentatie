# Productbeschrijving huishoudelijk afval

## Context
Deze datasets beschrijven de gegevens over onder- en bovengrondse afvalcontainers, hun locaties en afvalfracties.
Alle data wordt dagelijks geactualiseerd.

De data wordt in de volgende vormen beschikbaar:
- rest api (Beta versie)
- tekengescheiden bestand
- OGC WFS (gebruik GIS software)

  
## Productinhoud
De productinhoud is voor alle vormen gelijk, per vorm kan de data anders zijn geordend. Op dit moment worden alleen de laatst bekende (actuele) gegevens beschikbaar gesteld. 

 - [productinhoud afvalcontainers](productinhoud_afvalcontainers.md)
 - [productinhoud container clusters](productinhoud_afvalcontainer_clusters.md)
 - [productinhoud weeggegevens](productinhoud_afval_wegingen.md)
 - [productinhoud loopafstanden panden, stand- en ligplaatsen](productinhoud_afval_loopafstand_bag_object.md)
 - [productinhoud loopafstanden adres](productinhoud_afval_loopafstand_adres.md)
 - [Kaartlagen op data.amsterdam.nl](kaartlagen_website.md)

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

### Rest api
De rest api is aan te roepen met de url:
 - afvalclusters: https://api.data.amsterdam.nl/vsd/afvalclusters/
 - afvalcontainers: https://api.data.amsterdam.nl/vsd/afvalcontainers/
 - afvalwegingen: https://api.data.amsterdam.nl/vsd/afvalwegingen/

**Filtering op de rest api** \
Op de drie endpoints is het mogelijk om op elk datumveld te filteren. 
Filtering is op basis van de onderstaande parameters geimplementeerd:

 - <naam_datumveld>=Exacte datum
 - <naam_datumveld>__lte=Lager dan exacte datum
 - <naam_datumveld>__gte=Groter dan exacte datum

**Voorbeeldaanroep**

Alle wegingen op een bepaalde datum: \
 https://api.data.amsterdam.nl/vsd/afvalwegingen/?weging_datum_wegingen=2020-02-17

Alle wegingen op __voor__ bepaalde datum: \
 https://api.data.amsterdam.nl/vsd/afvalwegingen/?weging_datum_weging__lte=2020-02-17

Alle wegingen __na__ een bepaalde datum: \
 https://api.data.amsterdam.nl/vsd/afvalwegingen/?weging_datum_weging__gte=2020-02-17

Voorbeeldaanroep containers op plaatsingsdatum: \
 https://api.data.amsterdam.nl/vsd/afvalcontainers/?container_datum_plaatsing__gte=2020-02-17

<br>

### Tekengescheiden bestand
Voor elke 'tabel' in de dataset is een csv bestand beschikbaar. Deze bestanden voldoen aan de volgende specificaties:
- inhoud: zie productinhoud
- karakterset: UTF-8
- scheidingsteken: semicolon `;`
- kopregel: Ja

### Web Feature Service (WFS)
De Web Feature Service (WFS) is een interface voor het opvragen van geografische vector data met bijbehorende administratieve data. Het maakt gebruik van de op Extensible Markup Language (XML) gebaseerde Geography Markup Language (GML) en GeoJson.
Het Open Geospatial Consortium (OGC) definieert de specificaties van WFS. 

Zie deze pagina voor meer details van deze service.
**[Productinhoud WFS](productinhoud_wfs.md)**

## Definities objectklassen


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
