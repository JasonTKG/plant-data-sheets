# USDA PLANTS characteristics for 534 plants, one row per plant

**Site: [plant-data-sheets.at01.io](https://plant-data-sheets.at01.io/)** · Download: [latest release](https://github.com/JasonTKG/plant-data-sheets/releases/latest)

Archived on Zenodo: [doi:10.5281/zenodo.24496790](https://doi.org/10.5281/zenodo.24496790) · also on [Kaggle](https://www.kaggle.com/datasets/jasontkg/usda-plants-characteristics-534-plants) and [Hugging Face](https://huggingface.co/datasets/lakerguy16/plant-data-sheets)

One row per plant for the 534 plants that Plant Data Sheets has a data sheet for: names, native status, the conservation plant characteristics PLANTS records (83 fields) and counts of the states and counties where PLANTS records the plant.

## Files

| File | Rows |
|---|---|
| `plants.csv` | 534 |
| `plants_by_state.csv` | 10,312 |

## Columns

**`plants.csv`**

- `symbol`: USDA PLANTS symbol
- `scientific_name`: scientific name with author
- `common_name`: PLANTS common name
- `family`: family
- `rank`: Species, Subspecies, Variety or Genus: the record PLANTS keeps
- `group`: PLANTS group (Dicot, Monocot, Gymnosperm, ...)
- `durations`: Annual, Biennial, Perennial
- `growth_habits`: Tree, Shrub, Forb/herb, ...
- `native_status`: PLANTS region code and status code, e.g. L48:N (native in the lower 48 states), I = introduced
- `cold_limit_zone`: worked out by the site: the USDA hardiness zone band (2023 map definitions) that contains the plant's `Temperature, Minimum (°F)`
- `us_states_recorded`: number of U.S. states (and D.C.) where PLANTS records the plant
- `us_counties_recorded`: number of counties with a PLANTS record, summed over those states
- `plants_profile`: the plant's PLANTS profile page
- `(83 further columns)`: PLANTS conservation plant characteristics, values as PLANTS gives them; blank where PLANTS records none: `Active Growth Period`, `Adapted to Coarse Textured Soils`, `Adapted to Fine Textured Soils`, `Adapted to Medium Textured Soils`, `After Harvest Regrowth Rate`, `Anaerobic Tolerance`, `Berry/Nut/Seed Product`, `Bloat`, `Bloom Period`, `C:N Ratio`, `CaCO3 Tolerance`, `Christmas Tree Product`, `Cold Stratification Required`, `Commercial Availability`, `Coppice Potential`, `Drought Tolerance`, `Fall Conspicuous`, `Fertility Requirement`, `Fire Resistant`, `Fire Tolerance`, `Flower Color`, `Flower Conspicuous`, `Fodder Product`, `Foliage Color`, `Foliage Porosity Summer`, `Foliage Porosity Winter`, `Foliage Texture`, `Frost Free Days, Minimum`, `Fruit/Seed Abundance`, `Fruit/Seed Color`, `Fruit/Seed Conspicuous`, `Fruit/Seed Period Begin`, `Fruit/Seed Period End`, `Fruit/Seed Persistence`, `Fuelwood Product`, `Growth Form`, `Growth Rate`, `Hedge Tolerance`, `Height at 20 Years, Maximum (feet)`, `Height, Mature (feet)`, `Known Allelopath`, `Leaf Retention`, `Lifespan`, `Low Growing Grass`, `Lumber Product`, `Moisture Use`, `Naval Store Product`, `Nitrogen Fixation`, `Nursery Stock Product`, `Palatable Browse Animal`, `Palatable Graze Animal`, `Palatable Human`, `Planting Density per Acre, Maximum`, `Planting Density per Acre, Minimum`, `Post Product`, `Precipitation, Maximum`, `Precipitation, Minimum`, `Propagated by Bare Root`, `Propagated by Bulb`, `Propagated by Container`, `Propagated by Corm`, `Propagated by Cuttings`, `Propagated by Seed`, `Propagated by Sod`, `Propagated by Sprigs`, `Propagated by Tubers`, `Protein Potential`, `Pulpwood Product`, `Resprout Ability`, `Root Depth, Minimum (inches)`, `Salinity Tolerance`, `Seed Spread Rate`, `Seed per Pound`, `Seedling Vigor`, `Shade Tolerance`, `Shape and Orientation`, `Small Grain`, `Temperature, Minimum (°F)`, `Toxicity`, `Vegetative Spread Rate`, `Veneer Product`, `pH, Maximum`, `pH, Minimum`

**`plants_by_state.csv`**

- `symbol`: USDA PLANTS symbol
- `state`: U.S. state or District of Columbia
- `counties_recorded`: counties in that state with a PLANTS record; 0 where PLANTS records the state but no county

## Sources

| Source | URL | Terms | Retrieved |
|---|---|---|---|
| USDA, NRCS. 2026. The PLANTS Database. National Plant Data Team, Greensboro, NC USA | https://plants.usda.gov | PLANTS states that its plant information "is not copyrighted and is free for any use" | 2026-11-24 |
| USDA Plant Hardiness Zone Map, 2023: zone definitions | https://planthardiness.ars.usda.gov/pages/how-to-use-the-maps | U.S. government work; definitions only, not the map data | 2026-11-24 |

## How it was checked

The data was read by program from the PLANTS Database's own responses, saved on the retrieval date. A second program, with its own readers, compares every figure on every page of the site with those saved copies before each release, and a test with planted errors confirms it catches them. Values are as PLANTS gives them; the one worked-out field is `cold_limit_zone`. Where PLANTS' profile data and its characteristics search disagree on a value, the field is blank.

## Left out

Monthly observation counts from GBIF, shown on part of the site, are not included: they are counts over many datasets with their own CC0 and CC BY terms and citations. The 534 plants are a selection (PLANTS holds characteristics for about 2,200); the rule is on the site's About page.

## Licence

USDA PLANTS data is not copyrighted. This arrangement and the worked-out column are dedicated to the public domain under CC0 1.0 (see `LICENSE`). Please cite PLANTS as in the Sources table.

## Maintainer

Built and maintained by [JasonTKG](https://github.com/JasonTKG); corrections and questions: open an issue.

Exported 2026-11-24 from the data the site's pages are generated from.
