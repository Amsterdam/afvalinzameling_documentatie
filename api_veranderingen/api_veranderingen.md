## Rest api's

| rest\-api V1   | api V2\.0                                                    | impact                                                       |
| -------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| containers     | **afvalcontainers**                                              | \- nieuwe structuur,   <br>- objectid’s blijven gelijk <br> \- fractie\-id’s gestandaardiseerd |
| wells          | \-                                                           | nog niet geimplementeerd als separate api                    |
| containertypes | \-                                                           | \- \(nog\) niet als apart endpoint, opgenomen in afvalcontainers, <br>  \- id’s blijven gehandhaafd en zijn beschikbaar in afvalcontainers |
| sites          | **afvalclusters**                                                | \- persistente identificatie van de clusters <br> \- objectid’s blijven gelijk <br> \- fractie\-id’s gestandaardiseerd \(gelijk aan wegingen\) |
| sitefracties   | \-                                                           | \- vervallen als apart endpoint <br> \- opgenomen in afvalclusters,nieuwe structuur, <br>  \- objectid’s blijven gelijk,  <br> \- fractie\-id’s gestandaardiseerd |
| \- | **afvalwegingen**  | nieuw endpoint, relatie met persistente identificatie afvalclusters |                                                              |

## bron api's 

| bron\-api’s V1         | bron\-api’s V1 | impact      |
|------------------------|----------------|-------------|
| kilogram               | \-             | ongewijzigd |
| enevo/containers       | \-             | ongewijzigd |
| enevo/containertypes   | \-             | ongewijzigd |
| enevo/sites            | \-             | ongewijzigd |
| enevo/sitecontenttypes | \-             | ongewijzigd |
| enevo/containerslots   | \-             | ongewijzigd |
| enevo/alerts           | \-             | ongewijzigd |
| enevo/contenttypes     | \-             | ongewijzigd |
| enevo/filllevels       | \-             | ongewijzigd |
| sidcon/filllevels      | \-             | ongewijzigd |


## Web Feature service (WFS)

| wfs afval V1                 | wfs afval V2 | impact      |
|------------------------------|--------------|-------------|
| containers                   | \-           | ongewijzigd |
| rest                         | \-           | ongewijzigd |
| glas                         | \-           | ongewijzigd |
| papier                       | \-           | ongewijzigd |
| plastic                      | \-           | ongewijzigd |
| textiel                      | \-           | ongewijzigd |
| gfe                          | \-           | ongewijzigd |
| kca \(klein chemisch afval\) | \-           | ongewijzigd |
| site\_coordinaten            | \-           | **onbruikbaar** |
| site\_geometrie              | \-           | **onbruikbaar** |
| well\_coordinaten            | \-           | **geen relatie naar clusters** |
| wegingen\_rest               | \-           | **geen relatie naar clusters** |
| wegingen\_glas               | \-           | **geen relatie naar clusters** |
| wegingen\_papier             | \-           | **geen relatie naar clusters** |
| wegingen\_plastic            | \-           | **geen relatie naar clusters** |
| rest\_pand\_distance         | \-           | **let op: afstand hemelsbreed, NIET over de weg** |
| glas\_pand\_distance         | \-           | **let op: afstand hemelsbreed, NIET over de weg** |
| papier\_pand\_distance       | \-           | **let op: afstand hemelsbreed, NIET over de weg** |
| plastic\_pand\_distance      | \-           | **let op: afstand hemelsbreed, NIET over de weg** |
| textiel\_pand\_distance      | \-           | **let op: afstand hemelsbreed, NIET over de weg** |
| kca\_pand\_distance          | \-           | **let op: afstand hemelsbreed, NIET over de weg** |

