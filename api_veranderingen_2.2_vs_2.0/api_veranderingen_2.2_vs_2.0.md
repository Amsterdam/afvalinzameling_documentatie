## Vergelijking van API's v2.1 vs v2.0
In de onderstaande tabel de verschillen tussen twee API's te zien. 

| Rest API v2.0  | Impact/change | Rest-api V2.1 |
| --- | --- | --- |
| afvalcontainers | containertypegegevens in aparte endpoint | container |
|                 | Containerlocatiegegevens (put) in aparte endpoint |   |
|                 | Naast RD geen andere expliciete coördinatenstelsel|   |
|                 | Opbouw DSO-conform: linked data principe naar Gebieden en BAG |   |
|         -        | aparte endpoint op basis van containertypes |  containertype |
|                 | Objectgegevens check  toegevoegd: wijzigingsdatum|  |
|         -        | aparte endpoint op basis van wells, object-id’s blijven gelijk| containerlocatie |
|                 | Status en eigenaar toegevoegd|  |
|                 | datum plaatsing en oplevering toegevoegd|  |
|                 | Indicator bevat container toegevoegd|  |
|                 | Naast RD geen andere expliciete coördinatenstelsels|  |
|                 | Structuur gewijzigd, opbouw DSO-conform: linked data principe naar Gebieden en BAG|  |
|                 | objectgegevens check  toegevoegd: wijzigingsdatum en verwijderd indicator|  |
| afvalclusters   | clusterfractiegegevens in aparte endpoint| cluster |
|                 | Naast RD geen andere expliciete coördinatenstelsels| |
|                 | Opbouw DSO-conform: linked data principe naar Gebieden en BAG|  |
|       -          | aparte endpoint op basis van sitesfracties| clusterfractie |
|                 | clusterfractie-id toegevoegd |  |
|                 | Fractie-id’s gestandaardiseerd |  |
|                 | datum opvoer wijziging en einde toegevoegd |  |
|                 | Objectgegevens check  toegevoegd: wijzigingsdatum  |  |
| afvalweging     | Naast RD geen andere expliciete coördinatenstelsels  | weging |
|                 | Opbouw DSO-conform: linked data principe naar Gebieden en BAG  |  |
