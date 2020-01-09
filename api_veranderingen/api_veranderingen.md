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
| site\_coordinaten            | \-           | ongewijzigd |
| site\_geometrie              | \-           | ongewijzigd |
| well\_coordinaten            | \-           | ongewijzigd |
| wegingen\_rest               | \-           | ongewijzigd |
| wegingen\_glas               | \-           | ongewijzigd |
| wegingen\_papier             | \-           | ongewijzigd |
| wegingen\_plastic            | \-           | ongewijzigd |
| rest\_pand\_distance         | \-           | ongewijzigd |
| glas\_pand\_distance         | \-           | ongewijzigd |
| papier\_pand\_distance       | \-           | ongewijzigd |
| plastic\_pand\_distance      | \-           | ongewijzigd |
| textiel\_pand\_distance      | \-           | ongewijzigd |
| kca\_pand\_distance          | \-           | ongewijzigd |

