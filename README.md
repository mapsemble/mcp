# Mapsemble MCP server

Build interactive maps for your website from a conversation with Claude, ChatGPT or any MCP client:
add places, routes and photos, color the pins, add filters, design the cards and get the embed code.

**Server URL:** `https://app.mapsemble.com/mcp` (Streamable HTTP, OAuth 2.1)

This is a hosted server. You don't install anything: add the URL to your client and sign in with
your Mapsemble account (or create one while connecting). The server's source code is not public;
this repository holds its public listing and connection instructions.

## Connect

| Client | How |
|---|---|
| Claude (claude.ai, Desktop) | Settings → Connectors → Add custom connector → `https://app.mapsemble.com/mcp` |
| ChatGPT | Settings → Plugins → Add → Add custom MCP server → `https://app.mapsemble.com/mcp` |
| Claude Code | `claude mcp add --transport http mapsemble https://app.mapsemble.com/mcp` |

Sign-in uses OAuth 2.1 with client ID metadata documents (CIMD). Clients that only support
dynamic client registration (DCR) can't connect yet.

## What you can ask

- "Make a map of the best coffee spots in Amsterdam, with a photo for each"
- "Turn this Google Sheet of our locations into a map I can put on my website: <link>"
- "Color the pins on my map by category and let visitors filter by it"
- "Import the hiking routes from this GeoJSON file and color them by difficulty"

A live preview shows the map in the chat after each round of changes. Every change is also in the
Mapsemble builder, where you can carry on.

## Tools

| Tool | What it does |
|---|---|
| `list_maps`, `get_map` | Your maps, and one map's fields, filters and settings |
| `create_map` | A new map with the fields your locations need |
| `add_locations`, `update_locations`, `delete_locations`, `find_locations` | Places, lines and areas (address, coordinates, GeoJSON or WKT), with photos |
| `import_csv` | Hundreds of rows from CSV text |
| `preview_google_sheet`, `connect_google_sheet` | A public Google Sheet that keeps the map in sync |
| `preview_data_url`, `import_data_url` | A GeoJSON file, WFS service or CSV on the web |
| `add_fields`, `edit_fields` | The map's fields |
| `update_filters` | Filters and a name search for visitors |
| `set_feature_style` | Pin colors, icons, photo markers, line and area styles |
| `update_map_design`, `find_settings`, `update_map_config` | Map style and settings |
| `get_card_design`, `update_card_design` | The cards and popups |
| `show_map` | The live map in the chat |
| `get_embed_code` | The embed snippet for your website, WordPress, Framer, Webflow or any page |

The assistant works only on your own maps, within your plan's limits. Maps aren't deleted from the chat.

## Links

- Website: https://mapsemble.com
- Documentation: https://mapsemble.com/docs/claude-and-chatgpt
- Privacy: https://mapsemble.com/privacy · Terms: https://mapsemble.com/terms
- Support: support@mapsemble.com
- MCP Registry: `com.mapsemble/mapsemble`

Published by Nuez Web Solutions SLU.
