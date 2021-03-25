De huishoudelijk afval API v2.1 wordt uitgebreid met een aantal attributen in de volgende tabellen.
- Container
- Containerlocatie
- Containertype

container

| container                 | nieuw?   | Containerlocatie | nieuwe? | Containertype | nieuw? |
|------------------------|----------------|----------------|--------------|-------------|--------------| 
|container_id            |   nee |containerlocatie_id         |nee  |containertype_id|nee|             |   
|container_id_nummer    |       nee   |containerlocatie_serienummer | nee |containertype_naam|nee       |                         
|container_serienummer  | nee    |containerlocatie_status| nee|containertype_volume_m3|nee|              |                 
|container_geadopteerd_ind  | nee |containerlocatie_geometrie|nee|containertype_gewicht_kg|nee|              |  
|container_eigenaar_id  | nee     |containerlocatie_wgs84_lon|nee|containertype_wijzigingsdatum_dp|nee|              |  
container_eigenaar_naam  | nee   |containerlocatie_wgs84_lat|nee|containertype_verwijderd_dp|nee|              |  
container_status  | nee          |containerlocatie_eigenaar_id|nee|containertype_artikelcode|ja|              |  
container_fractie_code  | nee    |containerlocatie_eigenaar_naam|nee|containertype_hijskraantype_naam|ja|              |  
container_fractie_omschrijving|nee|containerlocatie_datum_creatie|nee|containertype_container_type|ja|              |  
container_datum_creatie  | nee   |containerlocatie_datum_plaatsing|nee|containertype_compressie_container_ind|ja|              |  
container_datum_plaatsing  | nee |containerlocatie_datum_oplevering|nee|containertype_compressiefactor|ja|              |  
container_datum_operationeel  | nee|ind_bevat_container|nee|containertype_hijskraan_opmerking|ja|              |  
container_datum_aflopen_garantie  | nee   |containerlocatie_datum_operationeel|nee|              |             |              |  
container_datum_oplevering  | nee|containerlocatie_datum_einde_garantie|nee|              |             |              |  
containerlocatie_id  | nee       |gbd_buurt_id|nee|              |             |              |  
container_geometrie  | nee       |bag_openbareruimte_id|nee|              |             |              |  
container_wgs84_lon  | nee       |bag_hoofdadres_verblijfsobject_id|nee                |              |             |              |  
container_wgs84_lat  | nee       |bag_nummeraanduiding_id|nee                |              |             |              |  
cluster_id  | nee                |containerlocatie_type_naam|ja|              |             |              |  
containertype_id  | nee          |containerlocatie_id_nummer|ja|              |             |              |  
gbd_buurt_code  | nee            |containerlocatie_datum_wijziging|ja|              |             |              |  
gbd_buurt_id  | nee              |containerlocatie_opmerking|ja|              |             |              |  
bag_openbareruimte_id  | nee     |containerlocatie_end_of_life|ja|              |             |              |  
bag_hoofdadres_verblijfsobject_id  |nee|containerlocatie_eigenaarschap|ja|              |             |              |  
bag_nummeraanduiding_id  | nee   |containerlocatie_eigenaarschap_opmerking|ja|             |              |  |
container_wijzigingsdatum_dp|nee |containerlocatie_type_artikelcode|ja|             |              |  |
container_verwijderd_dp  | nee   |        |                |              |             |              |  
container_ral_kleur_naam  | ja   |        |                |              |             |              |  
container_ral_kleur_code  | ja   |        |                |              |             |              |  
container_ral_kleur_hexcode  |ja |        |                |              |             |              |  
container_chip_nummber  | ja   |
container_unit_card_lezer_id |ja |        |                |              |             |              |  
container_kleur  | ja                    |                |              |             |              |  |
container_mark  | ja             |        |                |              |             |              |  
container_datum_vervanging  | ja |        |                |              |             |              |  
container_datum_wijziging  | ja  |        |                |              |             |              |  
container_end_of_life  | ja      |        |                |              |             |              |  
container_eigenaarschap  | ja    |        |                |              |             |              |  
container_eigenaarschap_opmerking  | ja   |        |                |              |             |              |  
container_opmerking  | ja        |        |                |              |             |              |  
     

