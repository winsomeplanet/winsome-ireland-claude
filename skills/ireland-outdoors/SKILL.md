---
name: ireland-outdoors
description: Answer questions about being outdoors in Ireland with official data. Use when the user asks where to swim, walk, hike, cycle or paddle in Ireland; asks about a beach, lake, trail, greenway, forest, castle, monument, island, park or garden there; asks whether a beach or lake is OK to swim in; asks about the weather for a walk, swim or day out this week or weekend; or names an Irish county (Clare, Kerry, Galway, Cork, Donegal, Mayo, Wicklow and the rest) or town while planning time outside.
---

# Ireland outdoors with Winsome Ireland

The Winsome Ireland connector (by Winsome Planet) holds official open data for the Republic of Ireland's 26 counties:
EPA bathing-water status, including restrictions in force now; Met Éireann county forecasts and
warnings; and about 1,190 trails, 155 Coillte forests, heritage sites, and Fáilte Ireland parks,
gardens, islands and beaches. Web pages about these are often out of date, and they never show a
bathing restriction that started this week. Use the connector's tools for these facts, and use web
search only for what the tools don't cover, such as tide times, sea temperature, opening hours or
events.

## Which tool for which question

| The user wants | Call |
|---|---|
| Where to swim, or whether a named beach or lake is OK to swim in | `bathing_water_check` (county and/or name). Always call it before recommending any swim spot |
| Walks, trails, beaches, forests, heritage, parks or islands in a county or matching a word | `find_places` (kind, county, query, `dogFriendly`, `maxLengthKm`) |
| Things near a town or a place | `places_near` with the town's latitude and longitude and `near` set to the town's name, or with `placeKind` and `placeSlug` from an earlier result |
| One place in detail | `get_place` with the kind and slug from an earlier result |
| What to do in a county this week or weekend | `county_guide` |
| Which day or which part of Ireland has the best weather for being outdoors | `outdoor_forecast` (add `county` for its day-by-day outlook) |
| To continue planning a trip on Winsome Planet | `planner_link` with the trip in one sentence, after the places are chosen |

For a question that spans these, call more than one: "Where can I swim in Clare this week?" needs
`bathing_water_check` for Clare and `outdoor_forecast` for Clare.

## How to answer

1. Lead with any restriction. If `bathing_water_check` reports an alert or an all-season
   restriction, say so first and don't suggest swimming there.
2. Never call a beach "safe". Say what the EPA found and when: the classification and its year, the
   latest sample and its date. Outside 1 June – 15 September, say that sampling and lifeguards
   have stopped for the season.
3. Pick days from the forecast, not from memory: name the best day and why (rain, wind,
   temperature), and mention any Met Éireann warning.
4. Link each place you recommend to the page URL the tool returned.
5. End with the source credits the tool returned, briefly: the data is CC BY 4.0 open data (and
   Met Éireann's licence for weather), and crediting it is a licence condition.
6. Coverage is the Republic of Ireland only. For Northern Ireland, say the connector doesn't cover
   it, and use other sources.

The tools return an interactive view (a map, place cards and a forecast) beside your answer, so keep
the written answer to the decision the user needs. Don't repeat every result the view already shows.
