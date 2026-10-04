# Tanzania Postcodes & Addresses

Every region, district, ward, and street in mainland Tanzania, with its postcode, as a PostgreSQL migration.

The dataset is also available on Kaggle as CSV: [kaggle.com/datasets/henrydioniz/tanzania-postcodes-addresses](https://www.kaggle.com/datasets/henrydioniz/tanzania-postcodes-addresses)

## Load into PostgreSQL

```bash
git clone https://github.com/Henryle-hd/Napa-Open-Address.git
cd Napa-Open-Address
psql "postgresql://user:password@localhost:5432/your_db" -f migrations/001_create_tanzania.sql
```

This creates a `tanzania` table with 68,571 rows. The migration runs in one transaction. If a `tanzania` table already exists, it fails and nothing is changed.

## Table: `tanzania`

| Column | Type | Description |
| --- | --- | --- |
| `id` | `SERIAL` | Primary key |
| `region` | `TEXT` | Region name (*mkoa*) |
| `region_code` | `TEXT` | 2-digit region postcode prefix |
| `district` | `TEXT` | District or council name (*wilaya*) |
| `district_code` | `TEXT` | 3-digit district postcode prefix |
| `ward` | `TEXT` | Ward name (*kata*) |
| `ward_code` | `TEXT` | 5-digit ward postcode |
| `street` | `TEXT` | Street or village (*mtaa / kijiji*), may be `NULL` |
| `places` | `TEXT` | Hamlet or local place (*kitongoji*), may be `NULL` |

```sql
SELECT DISTINCT ward_code FROM tanzania WHERE ward = 'SEKEI';
```
