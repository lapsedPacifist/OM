# OM - Ontology of units of Measure

The **Ontology of units of Measure (OM) 2.0** models concepts and relations important to scientific research. It has a strong focus on units, quantities, measurements, and dimensions.
OM is modelled in [OWL 2 - Web Ontology Language](https://www.w3.org/TR/owl2-overview/).

**Base URI:** `http://www.ontology-of-units-of-measure.org/resource/om-2/`

**Namespace Prefix:** `om`


#### Overview

* [Ontology of units of Measure](#om)
* [RecordTable ontology](#recordtable)
* [Software](#software)
* [Previous versions](#previous-versions)
* [Acknowledgements](#acknowledgements)
* [Papers on OM](#papers)


### <a name="om"></a>Ontology of units of Measure

The OM ontology provides classes, instances, and properties that represent the different concepts used for defining and using measures and units. It includes, for instance, common units such as the SI units metre (`om:metre`) and kilogram (`om:kilogram`), but also units from other systems of units such as the mile (`om:mile`) or nautical mile (`om:nauticalMile-International`). For many application areas it includes more specific units and quantities, such as the unit of the Hubble constant: km/s/Mpc `om:kilometrePerSecond-TimePerMegaparsec`, or the quantity vaselife `om:VaseLife`.

The following *application areas* are supported by OM:

* Geometry
* Mechanics
* Thermodynamics
* Electromagnetism
* Fluid mechanics
* Chemical physics
* Photometry
* Radiometry and Radiobiology
* Nuclear physics
* Astronomy and Astrophysics
* Cosmology
* Earth science
* Meteorology
* Material science
* Microbiology
* Economics
* Information technology
* Typography
* Shipping
* Food engineering
* Post-harvest technology
* Dynamics of texture and taste
* Packaging

![The UML structure of the OM ontology](images/OM2.0-UML-diagram.png)

**Figure 1.** The UML diagram below shows the class structure of the OM ontology.

The following triples express, for example, the diameter of an apple:
	ex:_10Centimetre rdf:type om:Measure ;
	  om:hasNumericalValue "10"^^xsd:double ;
	  om:hasUnit om:centimeter .
	ex:diameterOfApple1 om:hasValue ex:_10Centimetre ;
	  a om:Diameter ;
	  om:hasPhenomenon ex:apple1 .
	ex:apple1 rfd:type ex:Apple .

where `ex` is a prefixes for another namespace.

The RDF structure for this example shows as follows:

![Example: Apple size](images/OMAppleExample.png)

**Figure 2.** An RDF diagram representing the size of an apple as 10 cm.

Please not that:

> In OM, scales, such as the temperature scale are handled differently than their corresponding units. For instance a temperature difference will be expressed as a measure with a unit such as °C or K, where 28°C = 28 K. On the other hand an absolute temperature of 28°C is being referred to the **Celsius scale** and is equal to 301 K. Usually, the scale is used. [Here is an example of using a temperature scale.](Weather-example.md)

OM is based on several official paper standards, such as: [The Guide for the Use of the International System of Units](http://physics.nist.gov/cuu/pdf/sp811.pdf), by the NIST. 



### <a name="recordtable"></a>RecordTable Ontology

Included in the OM repository is the [RecordTable](https://github.com/HajoRijgersberg/OM/blob/master/record_table.ttl) vocabulary for semantically modelling tabular data, as a supplement to the existing RDF Data Cube standard. RDF Record Table has a nested structure of records that contain self-describing observations, and is able to cope with irregular, missing and unexpected data. This allows it to escape the constraints of RDF Data Cube and to model complex data, such as that occurring in science and engineering.

### <a name="software"></a>Software

Several software packages support the use, or make use of, OM:

* [`om-java-libs`](https://github.com/dieudonne-willems/om-java-libs): A software library written in Java that uses OM to convert between units.


### <a name="previous-versions"></a>Previous versions

Previous versions were published on the wurvoc platform.

* OM 1.8: [http://www.wurvoc.org/vocabularies/om-1.8/](http://www.wurvoc.org/vocabularies/om-1.8/)


### <a name="acknowledgements"></a>Acknowledgements

We would like to thank Jan Martin Keil and Sirko Schindler of the University of Jena for reviewing OM (see [Unit Ontology Review](https://github.com/fusion-jena/unit-ontology-review) and [publication](http://www.semantic-web-journal.net/system/files/swj1825.pdf)).


### <a name="papers"></a>Papers on OM

1. H. Rijgersberg, M.L.I. Wigham, J.L. Top, “How semantics can improve engineering processes. A case of units of measure and quantities.” *Advanced Engineering Informatics*, **25**, 2, 2011, pp. 276-287.
2. H. Rijgersberg, M.F.J. van Assem, J.L. Top, “Ontology of Units of Measure and Related Concepts.” *Semantic Web*, **4**, 1, 2013, pp. 3-13.
3. Top, J., Wigham, M., Rijgersberg, H. “Semantically Enriched Spreadsheet Tables in Science and Engineering.” *SEMAPRO 2014*.
4. Mari Wigham, Hajo Rijgersberg, Martine de Vos, Jan Top. “Semantic Support for Tables using RDF Record Table.” *International Journal On Advances in Intelligent Systems*, **8** (1 and 2), 2015, 128-144.
5. Jan Martin Keil, Sirko Schindler, “Comparison and Evaluation of Ontologies for Units of Measurement.” *Semantic Web*, **1**, 2018, pp. 1-19.


### <a name="uses-of-om"></a>References to uses of OM

1. D.J.M. Willems, H. Rijgersberg, J.L. Top, “Identifying and extracting quantitative data in annotated text”, *Proceedings of the Workshop on Semantic Web and Information Extraction (SWAIE 2012)*, Galway, Ireland, 2012, pp. 43-54.
2. Martine de Vos, Jan Wielemaker, Hajo Rijgersberg, Guus Schreiber, Bob Wielinga, Jan Top. Combining Information on Structure and Content to Automatically Annotate Scientific Spreadsheet Tables. *Int. J. Human-Computer Studies*, 103, 2017, pp. 63-76.
3. Bonsai, “BONSAI – Big Open Network for Sustainability Assessment Information.” 2019, https://bonsai.uno/.
4. Thorben Iggena, Daniel Kümper, Ralf Tönjes, Martin Strohbach, Pavel Smirnov, Juan A. Martinez, Sahr Thomas Acton, Roonak Rezvani, Josiane Parreira, “IoTCrawler. D4.1 IoT Data Attributes and Quality of Information.” University of Applied Sciences Osnabrück, 2019, https://iotcrawler.eu/wp-content/uploads/2019/07/D4.1_final.pdf.
5. Gkotse B., Jouvelot P., Ravotti F. (2019) IEDM: An Ontology for Irradiation Experiments Data Management. In: Hitzler P. et al. (eds) The Semantic Web: ESWC 2019 Satellite Events. ESWC 2019. Lecture Notes in Computer Science, **11762**, Springer, Cham, 2019.
6. Berrahou, S., Buche, P., Dibie-Barthelemy, J. , Roche, M., How to Extract Unit of Measure in Scientific Documents? In Proceedings of the International Conference on Knowledge Discovery and Information Retrieval and the International Conference on Knowledge Management and Information Sharing (SSTM-2013), 2013, pp. 249-256.
7. Mark S. Fox, A Foundation Ontology for Global City Indicators, University of Toronto, 2015.
8. Megan Katsumi, The Ontology of Units of Measure, https://enterpriseintegrationlab.github.io/icity/OM/doc/index-en.html.

*Under constuction*


### <a name="references-to-om"></a>References to OM
1. Loli Burgueño, Tanja Mayerhofer, Manuel Wimmer, Antonio Vallecillo, “Specifying quantities in software models.” *Information and Software Technology*, **113**, 2019, pp. 82-97.

*Under construction*
