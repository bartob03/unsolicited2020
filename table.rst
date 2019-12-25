

Zoning Service API
====================

.. table:: Service API

+---------+-------------------------+----------------------------------------+---------------------+-------------------+
| Method  | Endpoint                | Description                            | Example Request     | Example Response  |
+=========+=========================+========================================+=====================+===================+
| GET     | /status                 | Returns application status             |                     |                   |
+---------+-------------------------+----------------------------------------+---------------------+-------------------+
| GET     | /info                   | What is available                      |                     |                   |
|         |                         | inthewebservice(thecontents of this    |                     |                   |
|         |                         | table).                                |                     |                   |
+---------+-------------------------+----------------------------------------+---------------------+-------------------+
| POST    | /zone                   | Creates a new zone                     | /zone Body:zoneJson | CREATED           |
+---------+-------------------------+----------------------------------------+---------------------+-------------------+
| GET     | /zone/{type}/{zoneName}?version=<value> | Morton tiles (completely or partially) |                     | OK                |
+---------+-------------------------+----------------------------------------+---------------------+-------------------+
| GET     | /info                   | What is available                      |                     |                   |
|         |                         | inthewebservice(thecontents of this    |                     |                   |
|         |                         | table).                                |                     |                   |
+---------+-------------------------+----------------------------------------+---------------------+-------------------+
| GET     | /info                   | What is available                      |                     |                   |
|         |                         | inthewebservice(thecontents of this    |                     |                   |
|         |                         | table).                                |                     |                   |
+---------+-------------------------+----------------------------------------+---------------------+-------------------+
| GET     | /info                   | What is available                      |                     |                   |
|         |                         | inthewebservice(thecontents of this    |                     |                   |
|         |                         | table).                                |                     |                   |
+---------+-------------------------+----------------------------------------+---------------------+-------------------+

.. csv-table:: test table
   :file: testtable.csv
   :widths: 10, 15, 35, 20, 20
   :header-rows: 1

.. list-table:: Empty sample table
   :widths: 25 25 50
   :header-rows: 1

   * - Heading row 1, column 1
     - Heading row 1, column 2
     - Heading row 1, column 3
   * - Row 1, column 1
     -
     - Row 1, column 3
   * - Row 2, column 1
     - Row 2, column 2
     - Row 2, column 3

.. list-table::
   :widths: 5 15 20 25 35
   :header-rows: 1

   * - Method
     - Endpoint
     - Description
     - Example Request
     - Example Response
   * - GET
     - /status
     - Returns application status.
     -
     -
   * - GET
     - /info
     - Display data available in the web service (contents of this table).
     -
     -
   * - GET
     - /zone/{type}/{zoneName}?version=<value>
     - Morton tiles, complete or partial, that the zone contains.
     - /zone/AA7/Belgie.VlaamsGewest.Oost-Vlaanderen.Gent
     - ::

        OK
        {"name" : "België.Vlaams Gewest.Oost-Vlaanderen.Gent",
        "type" : "AA7",
        "version" : "12.4.1",
        "geometry" : "",
        "tiles" : [[CPEQAE:14,235422661,"POLYGON (((34216750 508996583, 34277344 508996583, ...)))"],[CPEQAE:14,235422681,""]... }
        The morton tiles that are completely in the zone do not have polygons in the response.
        The morton tiles that are partially in the zone do have geometry in the response.
   * - GET
     - /zone/{type}/{zoneName}/related?version=<value>&relatedType=<value>
     - Gets the JSON representing the ZoneInfos describing zones that are geographically related to the target zone. This method can be used to find spatial relationships (i.e. within, contains) between zones of different types.
     - /zone/AA7/België.Vlaams Gewest.Oost-Vlaanderen.Gent
     - ::

        OK
        <stream of zones>
   * - GET
     - /zone/{type}/{zoneName}/tiles?version=<value>&level=<value>
     - Gets zone tiles.
     - /zone/AA7/België.Vlaams Gewest.Oost-Vlaanderen.Gent
     - ::

        OK
        <stream of tiles>
   * - GET
     - /zone/{type}/{zoneName}/tiles/{density}?version=<value>
     - Gets zone tiles for specified density
     - /zone/AA7/België.Vlaams Gewest.Oost-Vlaanderen.Gent
     - ::

        OK
        <stream of density tiles>
   * - GET
     - /zoneview/{type}/{zoneName}?version=<value>&level=<value>
     - Shows page with zone view (visualization of multi-polygon).
     - /zoneview/AA7/België.Vlaams Gewest.Oost-Vlaanderen.Gent
     - ::

        OK
        <html>
   * - GET
     - /zonesforgeometry/{wkt}?version=<value>&type=<value>
     - Retrieves zones for passed WKT geometry
     - /zonesforgeometry/
     - ::

        OK
        [{"name":"BEL","type":"TIFCOUNTRY","version":"12.7.2"},
        {"name":"FRA","type":"TIFCOUNTRY","version":"12.7.2"},
        {"name":"BEL","type":"TIFDATASET","version":"12.7.2"},
        {"name":"F19","type":"TIFDATASET","version":"12.7.2"}]
   * - GET
     - /zonesintile/{tileLevel14}?version=<value>&type=<value>&level=<value>
     - Zones that contain the Morton tile of this ID; Default level is 14 (param is not required)
     - /zonesintile/14713859
     - ::

        OK
        [{"name":"BEL","type":"TIFCOUNTRY","version":"12.7.2"},
        {"name":"FRA","type":"TIFCOUNTRY","version":"12.7.2"},
        {"name":"BEL","type":"TIFDATASET","version":"12.7.2"},
        {"name":"F19","type":"TIFDATASET","version":"12.7.2"}]
   * - GET
     - /zonesforkeyword/{keyword}?version=<value>&type=<value>
     - Returns the breadcrumbs that contain the keyword.
     - /zonesforkeyword/ledeberg
     - ::

        OK
        [{"name":"BEL","type":"TIFCOUNTRY","version":"12.7.2"}, ... ]
   * - GET
     - /zonesforcoord/{longitude}/{latitude}?version=<value>&type=<value>
     - Zones on this location.
     - /zonesforcoord/23071290/488238795
     - ::

        OK
        [{"name":"BEL","type":"TIFCOUNTRY","version":"12.7.2"},
        {"name":"FRA","type":"TIFCOUNTRY","version":"12.7.2"},
        {"name":"BEL","type":"TIFDATASET","version":"12.7.2"},
        {"name":"F19","type":"TIFDATASET","version":"12.7.2"}]
   * - GET
     - /zoneversions/{type}/{zoneName}
     - All version of the given zone.
     - /zoneversions/TIFDATASET/AND
     - ::

        OK
        [{"name":"AND","type":"TIFDATASET","version":"12.4.1"},
        {"name":"AND","type":"TIFDATASET","version":"12.7.2"}]
   * - GET
     - /getrel/{timestamp}
     - Gets the release label for this timestamp (long).
     - /getrel/1317420000000
     - [CPEQAE:"11.10.1"]
   * - POST
     - /zone
     - Creates a new zone.
     - ::

        /zone
        Body:zoneJson
     - CREATED
   * - POST
     - /tiles/{density}
     - Adds zone density tiles.
     - ::

        /tiles/target
        Body: WKT
     - ::

        OK
        <stream of density tiles>

.. list-table:: Parameter Values
   :widths: 20 20 60
   :header-rows: 1

  * - Parameter
    - Format/Value
    - Example
  * - version
    - yy.M.d.HH.mm
    - "12.3.4" (represents 4/3/2012 0:00.00.000)
  * - version
    - (empty)
    - (displays the latest version)
  * - type
    - dataset
    - ?
  * - type
    - country
    - ?
  * - type
    - breadcrumbs
    - ?
  * - zonename
    -
    - "België.Vlaams Gewest.Oost-Vlaanderen.Gent"
  * - tileLevel14
    - morton tile level 14
    - 235026145
  * - keyword
    - any string to search on
    - "Ledeberg"
  * - longitude, latitude
    - Geographic Coordinate System (GCS)
    - 23071290, 488238795
  * - timestamp
    - long
    - 1317420000000 (long representation of date)

.. note::

   *Type* is taken from the type value in the zone info JSON files consumed by the *zone-create-tool*. There is no ENUM in the code.
