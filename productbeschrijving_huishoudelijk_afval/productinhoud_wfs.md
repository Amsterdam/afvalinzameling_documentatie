# Specificatie Web Feature Service << CONCEPT >>

De Web Feature Service (WFS) is primair bedoeld voor het gebruik is GIS applicaties zoals [QGIS](https://www.qgis.org/en/site/) of [ArcGis](https://www.esri.com/en-us/arcgis/products/arcgis-pro/overview).

## WFS layers

**Coordinaatsystemen**
default crs     :  EPSG:28992
ondersteunde crs:  EPSG:4326
ondersteunde crs:  EPSG::3857

**outputformaat**
Conform beleid dataservices

**Logische operaties**
Conform standaard dataservices (ComparisonOperator,SpatialOperator,TemporalOperands)

In de WFS zijn de lagen  zoals onderstaand gedefinieerd. De datatypen komen in hoofdlijn overeen met de datatypen van de rest-api.

**Afvalcontainers**
 - afval_container : alle afvalcontainers zonder filter
 - afval_container_rest : alle __actuele__ afvalcontainers van de afvalfractie `Rest`
 - afval_container_glas : alle __actuele__ afvalcontainers van de afvalfractie `Glas`
 - afval_container_papier : alle __actuele__ afvalcontainers van de afvalfractie `Papier`
 - afval_container_plastic : alle __actuele__ afvalcontainers van de afvalfractie `Plastic`
 - afval_container_textiel : alle __actuele__ afvalcontainers van de afvalfractie `Textiel`

**Container Clusters**
 - container_cluster_actueel : alle __actuele__ containerclusters


**Weeggegevens**
 - afval_weging : alle wegingen afval zonder filter
 - afval_weging_rest : alle __actuele__ wegingen afval van de afvalfractie `Rest`
 - afval_weging_glas : alle __actuele__ wegingen afval van de afvalfractie `Glas`
 - afval_weging_papier : alle __actuele__ wegingen afval van de afvalfractie `Papier`
 - afval_weging_plastic : alle __actuele__ wegingen afval van de afvalfractie `Plastic`
 - afval_weging_textiel : alle __actuele__ wegingen afval van de afvalfractie `Textiel`

**Afval putten**
 - afval_put : alle putten t.b.v. afvalcontainers zonder filter


## Attributen per layer
Voor de layers die historie bevatten worden alle kenmerken opgenomen zoals beschreven in de productinhoud. Bij layers met alleen actuele data worden de identificerende kenmerken van gerelateerde basisgegevens weggelaten (gebieden, openbareruimte, adres).

### Attributen afval_containers
	container_id,
	container_serienummer,
	eigenaar_id,
	container_eigenaar_naam,
	container_status,
	container_afvalfractie,
	container_datum_creatie,
	container_datum_plaatsing,
	container_datum_operationeel,
	container_datum_aflopen_garantie,
	container_datum_oplevering,
	containerlocatie_id,
	cluster_id,
	containertype_id,
	containertype_naam,
	containertype_volume_m3,
	containertype_gewicht_kg,
	gbd_buurt_naam,
	gbd_buurt_code,
	gbd_buurt_cbs_code,
	gbd_wijk_naam,
	gbd_wijk_code,
	gbd_wijk_cbs_code,
	gbd_stadsdeel_naam,
	gbd_stadsdeel_code,
	gbd_ggwgebied_naam,
	gbd_ggwgebied_code,
	woonplaats_naam,
	bag_openbareruimte_naam,
	bag_openbareruimte_type,
	bag_adres_openbare_ruimte_naam,
	bag_adres_nummeraanduiding_huisnummer,
	bag_adres_nummeraanduiding_huisletter,
	bag_adres_nummeraanduiding_huisnummertoevoeging,
	bag_adres_nummeraanduiding_postcode,
	bag_adres_woonplaatsnaam

### Attributen containerclusters

	cluster_id,
	cluster_subcluster_indicatie,
	geometry,
	cluster_datum_opvoer_cluster,
	cluster_datum_wijziging,
	cluster_datum_ontstaan_cluster,
	cluster_datum_einde_cluster,
	cluster_status,
	cluster_fractie_volume,
	cluster_fractie_aantal,
	gbd_buurt_naam,
	gbd_buurt_code,
	gbd_buurt_cbs_code,
	gbd_wijk_naam,
	gbd_wijk_code,
	gbd_wijk_cbs_code,
	gbd_stadsdeel_naam,
	gbd_stadsdeel_code,
	gbd_ggwgebied_naam,
	gbd_ggwgebied_code,
	woonplaats_naam,
	bag_openbareruimte_naam,
	bag_openbareruimte_type,
	bag_adres_openbare_ruimte_naam,
	bag_adres_nummeraanduiding_huisnummer,
	bag_adres_nummeraanduiding_huisletter,
	bag_adres_nummeraanduiding_huisnummertoevoeging,
	bag_adres_nummeraanduiding_postcode,
	bag_adres_woonplaatsnaam

### Attributen weeggegevens
	cluster_id,
	cluster_subcluster_indicatie,
	cluster_fractie_volume,
	cluster_fractie_aantal,
	weging_id,
	weging_weegsysteem_id,
	weging_weegsysteem_omschrijving,
	weging_volgnummer,
	weging_datum_weging,
	weging_tijdstip_weging,
	weging_welvaarts_locatienummer,
	weging_fractiecode,
	weging_fractie_omschrijving,
	weging_eerste_weging,
	weging_tweede_weging,
	weging_netto_gewicht,
	weging_geometrie,
	weging_longitude,
	weging_latitude,
	weging_bediening_code,
	weging_bediening_omschrijving,
	cluster_id,
	cluster_subcluster_indicatie,
	geometry,
	cluster_datum_opvoer_cluster,
	cluster_datum_wijziging,
	cluster_datum_ontstaan_cluster,
	cluster_datum_einde_cluster,
	cluster_status,
	cluster_fractie_volume,
	cluster_fractie_aantal,
	gbd_buurt_naam,
	gbd_buurt_code,
	gbd_buurt_cbs_code,
	gbd_wijk_naam,
	gbd_wijk_code,
	gbd_wijk_cbs_code,
	gbd_stadsdeel_naam,
	gbd_stadsdeel_code,
	gbd_ggwgebied_naam,
	gbd_ggwgebied_code,
	woonplaats_naam,
	bag_openbareruimte_naam,
	bag_openbareruimte_type,
	bag_adres_openbare_ruimte_naam,
	bag_adres_nummeraanduiding_huisnummer,
	bag_adres_nummeraanduiding_huisletter,
	bag_adres_nummeraanduiding_huisnummertoevoeging,
	bag_adres_nummeraanduiding_postcode,
	bag_adres_woonplaatsnaam

### Attributen Afvalputten

	bk_afv_containerlocatie
	id
	bk_afv_aanbiedlocatie_cluster
	serienummer
	status
	geometrie
	eigenaar_id
	eigenaar_naam
	datum_creatie
	datum_plaatsing
	datum_operationeel
	datum_einde_garantie
	datum_oplevering