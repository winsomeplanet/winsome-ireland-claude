# Winsome Ireland for Claude

A Claude plugin by [Winsome Planet](https://winsomeplanet.com).

Plan time outdoors in the Republic of Ireland with answers from official open data. Ask Claude where
you can swim this week, which walks suit a dog, what to do in a county this weekend, or which part of
the country has the best weather for a hike. Claude checks EPA bathing-water status before it
recommends a swim, picks days from Met Éireann's forecast, and shows the results on an interactive
map with place cards.

## Install

- **Claude (web, desktop, mobile):** Customize → Plugins → Discover, and search for Winsome Ireland
  (once it's listed in the directory). Then connect the bundled Winsome Ireland connector from the
  plugin's Connectors tab. It needs no sign-in.
- **Before it's listed:** download this repository as a zip and use Customize → Plugins → Add → Upload
  plugin.
- **Connector only:** add `https://winsomeplanet.com/api/mcp` as a custom connector (Settings →
  Connectors). Setup guide: https://winsomeplanet.com/claude

## What's in the plugin

- **Connector**: the Winsome Ireland MCP server at `https://winsomeplanet.com/api/mcp` (declared in
  `.mcp.json`). Seven read-only tools: `find_places`, `places_near`, `get_place`, `county_guide`,
  `bathing_water_check`, `outdoor_forecast` and `planner_link`. No account and no sign-in.
- **Skill** `ireland-outdoors`: tells Claude when to use those tools and how to answer: restrictions
  first, never calling a beach "safe", choosing days from the forecast, linking each place, and
  crediting the open-data sources.

## What it runs, sends and fetches

The plugin runs no code on your device. When Claude uses a tool, it sends only that tool's inputs (for
example a county name, a search word, or a town's coordinates) to `https://winsomeplanet.com/api/mcp`
and receives the results. Winsome Planet does not store those inputs. In Claude, the results include
an interactive view that loads photos from Fáilte Ireland's image host and Claude's own font, and
makes no other network requests. Links open the place's page on winsomeplanet.com or the source's
website.

## Data and credits

Sport Ireland, the EPA, Coillte, the National Monuments Service, the Heritage Council, Fáilte
Ireland, Logainm and Tailte Éireann (all CC BY 4.0), and Met Éireann (Met Éireann Open Data
Licence). Full credits: https://winsomeplanet.com/licensing

## Documentation, privacy and support

- Documentation: https://winsomeplanet.com/claude
- Privacy: https://winsomeplanet.com/privacy-policy#claude-connector
- Support: https://winsomeplanet.com/contact
