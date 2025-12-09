---
layout: default
title: "Template: E-Commerce"
---

# Template: E-Commerce Projects

*Starter memory edits for e-commerce and online store projects.*

---

## Core Template (5 edits)

Copy and customize these:

```
1. "Platform: [Shopify/WooCommerce/Custom/Magento]"
2. "Payment: [Stripe/PayPal/Square] primary processor"
3. "Inventory: [Real-time sync/Batch updates/Manual]"
4. "Shipping: [Integration with Shippo/EasyPost/Custom]"
5. "Stack: [Headless/Traditional] architecture"
```

---

## Filled Example

```
1. "Platform: Custom Next.js storefront, headless architecture" (59 chars)
2. "Payment: Stripe only, no PayPal (dispute rate concerns)" (56 chars)
3. "Inventory: Real-time sync with warehouse via webhook" (53 chars)
4. "Shipping: Shippo API for rates, EasyPost for labels" (52 chars)
5. "Stack: Headless with Medusa.js backend" (38 chars)
```

---

## Extended Template (10 edits)

For more complex projects:

```
6. "CMS: [Sanity/Contentful/Strapi] for product content"
7. "Search: [Algolia/Elasticsearch/Meilisearch]"
8. "Email: [SendGrid/Postmark/Resend] for transactional"
9. "Analytics: [GA4/Segment/Plausible]"
10. "Tax: [TaxJar/Avalara] for compliance"
```

---

## Business Model Additions

### Subscription Commerce
```
"Billing: Stripe Subscriptions with usage metering" (50 chars)
"Plans: Free, Pro ($29/mo), Enterprise (custom)" (46 chars)
"Trial: 14 days, no credit card required" (39 chars)
```

### Marketplace
```
"Payments: Stripe Connect for seller payouts" (43 chars)
"Commission: 15% platform fee on all sales" (41 chars)
"Escrow: Hold funds 7 days before release" (40 chars)
```

### B2B Commerce
```
"Pricing: Net-30 terms for approved accounts" (43 chars)
"Quotes: Custom pricing via quote request flow" (45 chars)
"Minimum order: $500 for wholesale accounts" (42 chars)
```

---

## Compliance & Tax

```
"Tax: TaxJar for US sales tax, manual for EU VAT" (47 chars)
"GDPR: Cookie consent required, data export available" (53 chars)
"PCI: Stripe handles all card data, never stored locally" (56 chars)
```

---

## How to Use

1. Copy the core template
2. Fill in the brackets with your specifics
3. Add using: `memory_user_edits add control="..."`
4. Test with relevant questions
5. Refine based on results

---

*Template from [Claude Memory User Edits Guide](https://github.com/frmoretto/claude-memory-user-edits-guide) — CC BY 4.0*
