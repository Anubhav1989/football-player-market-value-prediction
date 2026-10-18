# Data Dictionary

Source: Football Data from Transfermarkt (David Cariboo), Kaggle.
Table: `players_clean.csv`, 18,404 rows and 16 columns, one row per player.

## Columns

| Column | Type | Meaning |
|--------|------|---------|
| player_id | id | Transfermarkt player ID (not used as a feature) |
| name | text | Player name (kept for error analysis only) |
| country_of_citizenship | categorical | Player's nationality |
| position | categorical | Goalkeeper, Defender, Midfield or Attack |
| sub_position | categorical | Specific role, e.g. Centre-Back (Unknown if missing) |
| foot | categorical | Preferred foot (unknown if missing) |
| height_in_cm | numeric | Height; missing values filled with the median for the same position |
| international_caps | numeric | National team appearances (missing filled with 0) |
| international_goals | numeric | National team goals (missing filled with 0) |
| current_club_domestic_competition_id | categorical | League of the current club (UNKNOWN if the league is not covered) |
| age | numeric | Age in years on 2026-06-12 |
| contract_months_left | numeric | Months until the contract ends on 2026-06-12 (0 if expired or unknown) |
| caps_missing | binary | 1 if international caps data was missing |
| no_league | binary | 1 if the club's league is not in the dataset |
| has_contract_info | binary | 1 if a contract end date was available |
| market_value_in_eur | numeric | TARGET: market value in euros |

## Cleaning decisions

- Kept only players whose last season is 2025 and who have a market value.
- Reference date for age and contract time: 2026-06-12, the last date with recorded valuations.
- Dropped `highest_market_value_in_eur` because it leaks the target.
- Dropped identifiers, URLs, club names and other free-text columns.