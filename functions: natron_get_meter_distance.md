This function converts degree to meter, it allows geographical distance analisys with postgis functions running 
geographical dataset having a metric projection.

```sql
-- FUNCTION: data.natron_get_meter_distance(double precision)

-- DROP FUNCTION data.natron_get_meter_distance(double precision);

CREATE OR REPLACE FUNCTION data.natron_get_meter_distance(
	degrees double precision)
    RETURNS double precision
    LANGUAGE 'sql'
    COST 100
    IMMUTABLE SECURITY DEFINER 
    ROWS 0
AS $BODY$

	--documentation: https://stackoverflow.com/questions/8444753/st-dwithin-takes-parameter-as-degree-not-meters-why
    SELECT (($1 * 6378137) * pi()) / 180

$BODY$;

```
