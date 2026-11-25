# Sayod 111 n8n Automation Templates

[![Listed on mcpservers.org](https://mcpservers.org/badge.svg)](https://mcpservers.org/servers/sayod111/sayod111-mcp-servers)
[![mcptry](https://mcptry.com/badge/io.github.sayod111/sayod111-intelligence-mcp)](https://mcptry.com/servers/io.github.sayod111/sayod111-intelligence-mcp)

Ready-to-import n8n workflows powered by Sayod 111 pure async HTTP/2 commercial data engines on Apify Cloud. Every workflow uses n8n's built-in HTTP Request node with Bearer header authentication and writes flat, schema-validated columns straight to Google Sheets.

## Included Workflows (11 total)
1. `01_shopify_pixel_klaviyo_audit.json`: Audits Shopify storefronts for active Meta/TikTok/Google pixels, Klaviyo adoption, SEO/CRO defects, and DNS MX-verified merchant contacts. Engine: https://apify.com/sayod111/shopify-klaviyo-pixel-auditor
2. `02_b2b_dmarc_tech_stack_audit.json`: Runs bulk DNS MX/SPF/DMARC security posture audits plus 110+ technology fingerprints and corporate contacts. Engine: https://apify.com/sayod111/dmarc-spf-mx-deliverability-auditor
3. `03_ashby_greenhouse_hiring_alerts.json`: Tracks live open roles and 6 B2B buying intent categories across Ashby and Greenhouse career boards. Engine: https://apify.com/sayod111/ashby-greenhouse-hiring-intent

## SEC adviser and trust center workflows

These four templates require access to their Apify Actors while Store publication is pending.

- [Sayod 111 WealthPulse V3 - Weekly Updated $100M-$1B RIAs -> DMARC Audit](01_weekly_new_and_updated_rias_to_dmarc_audit.json)
- [Sayod 111 WealthPulse V3 - Boutique Longevity M&A Research Upsert](02_ria_ma_boutique_longevity_upsert_sheets.json)
- [Sayod 111 WealthPulse V3 - New Breakaway RIA Radar (Last 90 Days)](03_new_ria_radar_90d_upsert_sheets.json)
- [Sayod 111 - Weekly SEC RIA -> SaaS Trust Center & Security Audit](01_wealthpulse_to_trust_center_audit.json)

## Healthcare and public procurement workflows

These templates require access to the corresponding Apify Actor.

- [Sayod 111 - Weekly MedTech KOL & Medicare Compliance Radar](01_weekly_medtech_kol_medicare_radar.json)

- [Sayod 111 - Daily 07:00 AM US SLED Government Bids & RFP Radar](01_daily_sled_gov_bids_radar.json)

## Quick Import
1. In n8n, open Workflows -> Import from File and select any JSON file above.
2. Add your Apify API token as `APIFY_API_TOKEN` in n8n environment variables (or directly in the Authorization Bearer header).
3. Connect Google Sheets and execute.

Full suite documentation: https://sayod111.github.io | Apify Store: https://apify.com/sayod111

## Wave 3 Flagship Workflows (Added Nov 25, 2026)
- `10_daily_ucc1_refinance_radar.json`: Daily commercial UCC-1 lien and refinance trigger radar (`sayod111/us-ucc-1-secured-loan-leads`, deduplicated by `ucc_uid`).
- `11_weekly_biotech_nih_trials_fda_radar.json`: Weekly NIH RePORTER grants, ClinicalTrials.gov studies, and openFDA 510(k) radar (`sayod111/us-biotech-grants-trials-fda510k`, deduplicated by `signal_uid`).

## Quick-Start: Shopify Klaviyo & Ad Pixel Audit (`01_shopify_pixel_klaviyo_audit.json`)

**Workflow Nodes:** `When clicking Execute Workflow` -> `Run Sayod 111 (shopify-klaviyo-pixel-auditor)` -> `Append Flat Columns to Google Sheets` (plus standalone `Setup Instructions` note).

**1. Exact Input Payload (`storeUrls`):**
```json
{
  "storeUrls": [
    "https://hexclad.com",
    "https://ourplace.com"
  ]
}
```

**2. Google Sheets `Sheet1` Headers (`autoMapInputData`):**
`domain | platform | has_klaviyo | klaviyo_company_id | meta_pixel_id | tiktok_pixel_id | google_ads_id | apps_detected_csv | http_status`

Run directly on Apify Store: https://apify.com/sayod111/shopify-klaviyo-pixel-auditor

## Workflow 12: Compound B2B Radar Weekly Delta (`12_sayod111_compound_radar_weekly_delta.json`)

Fetches pre-enriched weekly buying signals (Shopify Paid Ads + Missing Klaviyo + ATS Hiring, Cyber/GRC Trust Center, or 12,019 SEC Form ADV RIAs) directly from Cloudflare Edge D1 in a single HTTP node.

- Live Zero-Login Auditors: https://sayod111-radar.pages.dev/
- OpenAPI 3.1 & Integration Docs: https://sayod111-radar.pages.dev/docs.html
