<h1>NaTron</h1>

NaTron is a web driven geo-database application holding and managing ecological data collection for the Natural History museum of Trondheim at NTNU-VM. https://natron.vm.ntnu.no/datacollection/.

<h2>Plattform and program installation</h2>
  <h3>Postgresql (9.6.4, server 9.5.10)</h3> https://www.postgresql.org/
  <h3>Extensions</h3>
    <ul>
        <li>postgis 2.2.2 http://postgis.net/. Enables geographical and geometrical process.</li>
        <li>plpythonu https://www.postgresql.org/docs/9.1/static/plpython.html. Enables procedural programmering in python language.</li>
        <li>plpgsql 1.0. Enables procedural programmering in PL/pgSQL language.</li>
        <li>uuid-ossp 1.0. Enables uuid generator</li>
        <li>mgrs 1.3.5 https://pypi.python.org/pypi/mgrs. Enables geographical coordinate convertion between metric and geodesic, the program requiers plpythonu installation</li>
        <li>dblink https://www.postgresql.org/docs/10/static/dblink.html. enables database connectivity across palttform.</li>
    </ul>
    <h3>NaTron trigger functions</h3>
    <ul>
        <li>consolidate_data. PL/pgSQL procedural function which is triggered at record edition, the function processes and ensures data quality through editing rules. The function invokes procedural functions deployed in plpython.</li>
    </ul>
    <h3>Natron functions</h3>
    <ul>
        <li>natron_get_geodesic. python procedural function converting metric geographical coordinates (mgrs, utm) to geodesic coordinates as latitude and longitude decimal.</li>
        <li>natron_get_mgrs. python procedural function converting geodesic coordinates as latitude and longitude decimal to the metric mgrs coordinates.</li>
        <li>natron_get_mgrs_from_utm. python procedural function converting utm coordinates to mgrs coordinates.</li>
        <li>natron_get_verbatim_coordinate_system. python procedural function determining the coordinate based on a well known gps format. supported format are mgrs, utm and geodesic.</li>
        <li>median. PL/pgSQL functional aggregate that calculate the median.</li>
    </ul>

<h2>Programming languages</h2>
    <ul>
      <li>VB.NET</li>
      <li>Asp.NET</li>
      <li>HTML</li>
      <li>CSS</li>
      <li>JavaScript</li>
      <li>Python</li>
      <li>SQL</li>
      <li>PL/pgSQL</li>
    </ul>

<h2>Development</h2>
    <ul>
      <li>pgAdmin 4</li>
      <li>Visual Studio 15</li>
    </ul>

<h2>Database</h2>
  <h3>Model and architecture</h3>
      <span>See https://natron.vm.ntnu.no/DataCollection/dbDocumentation/rdbms/ for interactive database diagram.</span>
  <h3>Application</h3>
  <h3>Scoping</h3>
