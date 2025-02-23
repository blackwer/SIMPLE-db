# Gravities

The Gravities table contains gravity measurements for sources listed in the Sources table. 
The combination of *source*, *regime*, and *reference* is expected to be unique.
Note that *gravity* and *regime* are strings constrained from a list of enumerated values. 
Columns marked with an asterisk (*) may not be empty.

| Column Name | Description  | Unit  | Data Type | Key Type  |
|---|---|---|---|---|
| *source    | Unique identifier for the source |   | String(100)  | primary and foreign: Sources.source   |
| gravity | Gravity value |  | Enumeration  |   |
| *regime | Regime for gravity value |  | Enumeration  | primary |
| comments  | Free form comments |   | String(1000) |   |
| *reference | Reference |   | String(30) | primary and foreign: Publications.name |

Enumeraions for gravity include:
 - alpha
 - beta
 - gamma
 - delta
 - beta/gamma
 - unknown
 - vl-g
 - int-g
 - fld-g

Enumerations for regime include:
 - gammaray
 - xray
 - ultraviolet
 - optical
 - infrared
 - millimeter
 - radio
