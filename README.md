# AgentMade Print on Demand

Print on demand for AI agents. Your agent puts a design, words or a logo on a T-shirt, hoodie, sweatshirt or tote bag, and ships it.

- No account and no API key.
- The print is checked at real size.
- One delivered price: product, shipping and VAT where AgentMade collects it.
- The person pays on a secure payment page. Production starts after the payment is confirmed.

This repository contains the registry manifest (`server.json`) and setup notes. The service runs at https://pod.agentmade.dev.

## Connect

Remote MCP server (Streamable HTTP, no authentication):

```
https://pod.agentmade.dev/mcp/pay
```

Claude Code:

```bash
claude mcp add --transport http agentmade https://pod.agentmade.dev/mcp/pay
```

Other clients: see https://pod.agentmade.dev/agents.

REST API: the OpenAPI description is linked from https://pod.agentmade.dev/.well-known/api-catalog.

## Tools

| Tool | What it does |
|---|---|
| `search_products` | Finds T-shirts, hoodies, sweatshirts and tote bags |
| `get_product` | Gives colours, sizes, print areas and photos |
| `validate_artwork` | Checks the design at real size |
| `create_mockup` | Shows the design on the product |
| `quote` | Gives one delivered price |
| `purchase` | Creates the order and the payment link |
| `get_order` | Gives the order status |
| `track_order` | Gives the tracking link |
| `cancel_order` | Cancels the order before production |

## Example

> Print this SVG on a heavyweight black XL T-shirt and ship it to Prague.

## Limits

Not for mugs, posters, caps or embroidery. Orders to the United Kingdom are not open yet.

## Support

https://pod.agentmade.dev/contact
