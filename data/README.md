# Tanzania Postcodes & Addresses

Every region, district, ward, and street in mainland Tanzania, with its postcode (*Anwani za Makazi*).

## What's inside

| Item | Count |
| --- | --- |
| Regions | 26 (all of mainland Tanzania) |
| Districts / councils | 158 |
| Wards (unique postcodes) | 3,945 |
| Street / village records | 68,571 |

## Files

| File | Contents |
| --- | --- |
| `all_tanzania.csv` | All 26 regions combined (68,571 rows) |
| `arusha.csv`, `dar_es_salaam.csv`, `dodoma.csv`, … | One file per region, with the same columns |

## Columns

| Column | Description | Example |
| --- | --- | --- |
| `region` | Region name (*mkoa*) | `ARUSHA` |
| `region_code` | 2-digit region postcode prefix | `23` |
| `district` | District or council name (*wilaya*) | `ARUSHA CBD` |
| `district_code` | 3-digit district postcode prefix | `231` |
| `ward` | Ward name (*kata*) | `SEKEI` |
| `ward_code` | 5-digit ward postcode | `23101` |
| `street` | Street or village (*mtaa / kijiji*) | `SANAWARI` |
| `places` | Hamlet or local place name (*kitongoji*). Often empty. | |

## SQL

For a PostgreSQL version of this dataset, go to [https://github.com/Henryle-hd/Napa-Open-Address.git](https://github.com/Henryle-hd/Napa-Open-Address.git)
