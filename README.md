# Brek.com Hotel Search

Find hotels by city, neighborhood, or landmark, or check room options at a named hotel for your dates and guests. Brek helps travelers compare public hotel prices with private wholesale offers and continue to Brek.com to review and book a stay.

This plugin teaches Claude the Brek hotel-research workflow. It supports destination searches, direct hotel-name room queries, amenities, refundable-room preferences, and full-stay price comparisons when the returned data supplies them. You do not need a partner API key or a developer account for traveler research.

## Add and use

Add the plugin in Claude, then connect its Brek connector if it is not already connected. The plugin uses the same `https://mcp.brek.com/mcp` endpoint as the existing Brek Hotel Wholesale Booking connector. If you already use that connector, Claude can reuse it. Skills work in supported Claude chat, Cowork, and Claude Code sessions; the current Claude incognito experience does not provide the code execution environment skills require.

Describe your destination or hotel, check-in, check-out, guests, rooms, and any preferences. Claude can use the skill automatically for relevant hotel questions. Public HTML research can also use Claude's built-in webpage tools without a connector. A stored-prices-only request uses read-only pages and does not initiate a live supplier check.

## Example questions

Replace example dates with the dates of your intended future trip.

- Find the lowest hotel stay totals in Seattle for November 20–22, 2026, two adults, one room, in USD. Compare public and wholesale offers.
- What room options and full-stay prices does The Beverly Hilton have for November 27–December 2, 2026, two adults, one room?
- Find pet-friendly hotels with a kitchen in Portland, Oregon, for November 20–22, 2026, two adults, one room, in USD.
- Read saved wholesale hotel prices in Redmond for November 20–27, 2026, two adults, one room. Do not start a live-price check.

## Price coverage

Exact selling totals can be reported when a matching response or public HTML page supplies them. Saved observations keep their original timestamps and are not current availability. The current connector advertises masked wholesale bands; the skill can use a permitted matching HTML quote where one exists. It does not reconstruct hidden digits or substitute a different date or occupancy. Public comparisons are attributed to the provider named by the data, such as Expedia.com or Booking.com. Brek cannot guarantee the lowest price across the entire market. Final availability, terms, and prices are reviewed on Brek before booking.

## Data and permissions

The plugin consists only of Markdown instructions and JSON configuration. It contains no executable scripts, hooks, credential headers, local MCP servers, or payment tools. Hotel research sends the trip inputs needed for the query to Brek's declared connector or Brek's public website; independent public sources may also be read when the traveler requests a comparison. Do not include unrelated conversation contents, card details, or credentials. This plugin itself has no database or background data collection; Brek's services and the Claude host have their own data handling policies.

Research does not authorize the plugin to make a booking, pay, cancel a stay, or change account settings. Review and book on [Brek.com](https://www.brek.com). Connector information and support are available at [Brek Help](https://www.brek.com/help/connectors) or support@reply.brek.com.

## License

The plugin's instruction and configuration files are released under the MIT License. This license covers this repository's files; Brek's hosted services retain their own terms.
