---
layout: page
meta_title: "About deegree"
subheadline: ""
teaser: ""
permalink: "/about-deegree/"
---

## Introduction

deegree web services are implementations of the Geospatial Web Service Specifications of the [Open Geospatial Consortium (OGC)](http://www.opengeospatial.org/) and the [INSPIRE Network Services](http://inspire.ec.europa.eu/index.cfm/pageid/5).

deegree web services include the following services:

  * **Web Feature Service** (WFS): Provides access to raw geospatial data objects
  * **Web Map Service** (WMS): Serves maps rendered from geospatial data
  * **Web Map Tile Service** (WMTS): Serves pre-rendered map tiles
  * **Catalogue Service for the Web** (CSW): Performs searches for geospatial datasets and services
  * **Web Processing Service** (WPS): Executes geospatial processes

With a single deegree webservices installation, you can set up one of the above services, all of them or even multiple services of the same type. 

## Characteristics of deegree webservices
<br/>
{% capture accordion_body %}
deegree WFS is a reference implementation of the OGC Web Feature Service specification. Notable features are:

   * Implements WFS standards 1.0.0, 1.1.0 and 2.0.0
   * Fully transactional (even for rich data models)
   * Supports KVP, XML and SOAP requests GML 2/3.0/3.1/3.2 output/input
   * Support for GetGmlObject requests and XLinks
   * High performance and excellent scalability
   * On-the-fly coordinate transformation
   * Designed for rich data models from the bottom up
   * Backends support flexible mapping of GML application schemas to relational models
   * ISO 19107-compliant geometry model: Complex geometries (e.g. non-linear curves)
   * Advanced filter expression support based on XPath 1.0
   * Supports numerous backends, such as PostGIS, Oracle Spatial, MS SQL Server, Shapefiles or GML instance documents
{% endcapture %}
{% include _accordion.html content=accordion_body title="deegree WFS" active=1 start=1 %}

{% capture accordion_body %}
deegree WMS is a reference&nbsp;implementation of the OGC Web Map Service specification. Notable features:

  * Implements WMS standards 1.1.1 and 1.3.0
  * Extensive support for styling languages SLD/SE versions 1.0.0 and 1.1.0
  * High performance and excellent scalability
  * High quality rendering
  * Scale dependent styling
  * Support for SE removes the need for a lot of proprietary extensions
  * Easy configuration of HTML and other output formats for GetFeatureInfo responses
  * Uses stream-based data access, minimal memory footprint
  * Nearly complete support for raster symbolizing as defined in SE (with some extensions)
  * Complete support for TIME/ELEVATION and other dimensions for both feature and raster data
  * Supports numerous backends, such as PostGIS, Oracle Spatial, Shapefiles or GML instance documents
  * Can render rich data models directly
{% endcapture %}
{% include _accordion.html content=accordion_body title="deegree WMS" %}

{% capture accordion_body %}
deegree WMTS is a reference implementation of the OGC Web Map Tile Service specification. Notable features:

  * Implements Basic WMTS standard 1.0.0 (KVP)
  * High performance and excellent scalability
  * Supports different backends, such as GeoTIFF, remote WMS or file system tile image hierarchies
  * Supports on-the-fly caching (using EHCache)
  * Supports GetFeatureInfo for remote WMS backends
{% endcapture %}
{% include _accordion.html content=accordion_body title="deegree WMTS" %}

{% capture accordion_body %}
deegree CSW is an implementation of the OGC Catalogue Service specification. Notable features:

  * Implements CSW standard 2.0.2
  * Fully transactional Supports KVP, XML and SOAP requests
  * High performance and excellent scalability
  * ISO Metadata Application Profile 1.0.0
  * Pluggable and modular dataaccess layer allows to add support for new APs and backends
  * Modular inspector architecture allows to validate records to be inserted against various criteria
  * Standard inspectors: schema validity, identifier integrity, INSPIRE requirements
  * Handles all defined queryable properties (for Dublin Core as well as ISO profile)
  * Complex filter expressions
{% endcapture %}
{% include _accordion.html content=accordion_body title="deegree CSW" %}

{% capture accordion_body %}
deegree WPS is an implementation of the OGC Processing Service specification. Notable features:

  * Implements WPS standard 1.0.0
  * Supports KVP, XML and SOAP requests
  * Pluggable process provider layer
  * Easy-to-use API for implementing Java processes
  * Supports all variants of input/output parameters: literal, bbox, complex (binary and xml)
  * Streaming access for complex input/output parameters
  * Processing of huge amounts of data with minimal memory footprint
  * Supports storing of response documents/output parameters
  * Supports input parameters given inline and by reference
  * Supports RawDataOutput/ResponseDocument responses
  * Supports asynchronous execution (with polling of process status)
{% endcapture %}
{% include _accordion.html content=accordion_body title="deegree WPS" %}

{% capture accordion_body %}
deegree is distributed under the GNU Lesser General Public License, Version 2.1 (LGPL 2.1). Generally speaking this means that you have essential freedoms such as: Run the software for any purpose, find out how it works, make changes, redistribute copies (of modified versions). Practically, with these freedoms, you do not have to pay a license fee, you can create as many installations as you need, and you're not bound to one single vendor. Instead you can contact a service provider of your choice to make necessary configurations or code adjustments. Or you may even step up and do this yourself.

More information about free software can be found at the free software foundation. A good starting point is <a href="http://www.gnu.org">www.gnu.org</a><a href="http://www.gnu.org"> </a>

{% endcapture %}
{% include _accordion.html content=accordion_body title="Open Source License" %}

{% capture accordion_body %}
deegree is a standards-based Java framework for spatial data infrastructures.

#### Standards-based

Interoperability is a major driver for the development of deegree. Besides being free software - which already is an important aspect of openness and hence interoperability - it implements geospatial IT standards and uses general IT technology. deegree implements the major standards of the Open Geospatial Consortium (OGC) and the ISO Technical Committee 211. deegree core subsystems like the geometry or the metadata model are based on ISO 19107 (Geographic information -- Spatial schema) and ISO 19115 (Geographic information -- Metadata).

deegree web services and other applications use these core modules. They are implementations of OGC specifications, such as Web Map Service (WMS), Web Feature Service (WFS), Catalogue Service (CSW), Web Coverage Service (WCS) and Web Processing Service (WPS).

#### Java technology

deegree is pure Java and can therefore be run on all platforms supporting the Java runtime environment. The currently preferred platform is OpenJDK. Oracle JDK is also supported. For web services deployment we recommend Apache Tomcat.
{% endcapture %}
{% include _accordion.html content=accordion_body title="Technology" %}

{% capture accordion_body %}
The deegree project was born in summer 2002 as a consistent follow-up of a research &amp; development project at the Geography Department of the University of Bonn in Germany. Based on one of the first implementations of the early Simple Features model of the Open Geospatial Consortium (OGC) it started under the label "Jago" and was renamed to be "deegree" in 2002.

  * deegree 1 (2002 - 2004) includes CSW, WFS and Simple Features client, WMS (OGC reference implementation) and WCS
  * deegree 2 (2004 - 2012) includes CSW, WCS, WCTS, WFS, WMS, WPS, WPVS - Encodings: FE, GML, Metadata - Applications: iGeoDesktop, iGeoPortal, iGeoSecurity
  * deegree 3 (2007 - ) is focused on the main OGC web services such as WFS, WMS, WMTS, CSW, WPS and a stable API.

<strong>Please note that current development is focused on version 3. Version 1 and 2 are not maintained anymore! For more information on the maintained versions checkout our [End of Life wiki page on GitHub](https://github.com/deegree/deegree3/wiki/End-of-Life-and-Support-Matrix).</strong>
{% endcapture %}
{% include _accordion.html content=accordion_body title="Short History" %}

{% capture accordion_body %}
deegree is coordinated by a Project Steering Committee (PSC) and technically governed by a Technical Management Committee (TMC). Both institutions work closely together while each one has its designated responsibilities.

&gt; Read more on Structures and Procedures of the deegree project on the <a href="https://github.com/deegree/deegree3/blob/master/CONTRIB.md#structures-and-procedures-of-the-deegree-project" target="_blank" rel="noopener noreferrer">deegree Contribution Guidelines</a>.

In 2010 deegree was officially accepted to be an OSGeo project after a two-years incubation process which was a major step towards more transparency and quality, both in structures, procedures and the software itself. Being an OSGeo project deegree has a strong commitment to enhance its overall accessibility and make the software as easy to use as possible.

{% endcapture %}
{% include _accordion.html content=accordion_body title="Project Organisation" end=1 %}
