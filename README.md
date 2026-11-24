# Sayod 111 n8n Automation Templates

Ready-to-import n8n workflows powered by Sayod 111 pure async HTTP/2 commercial data engines on Apify Cloud. Every workflow uses n8n's built-in HTTP Request node with Bearer header authentication and writes flat, schema-validated columns straight to Google Sheets.

## Included Workflows
1. `01_shopify_pixel_klaviyo_audit.json`: Audits Shopify storefronts for active Meta/TikTok/Google pixels, Klaviyo adoption, SEO/CRO defects, and DNS MX-verified merchant contacts. Engine: https://apify.com/sayod111/shopify-klaviyo-pixel-auditor
2. `02_b2b_dmarc_tech_stack_audit.json`: Runs bulk DNS MX/SPF/DMARC security posture audits plus 110+ technology fingerprints and corporate contacts. Engine: https://apify.com/sayod111/dmarc-spf-mx-deliverability-auditor
3. `03_ashby_greenhouse_hiring_alerts.json`: Tracks live open roles and 6 B2B buying intent categories across Ashby and Greenhouse career boards. Engine: https://apify.com/sayod111/ashby-greenhouse-hiring-intent

## Quick Import
1. In n8n, open Workflows -> Import from File and select any JSON file above.
2. Add your Apify API token as `APIFY_API_TOKEN` in n8n environment variables (or directly in the Authorization Bearer header).
3. Connect Google Sheets and execute.

Full suite documentation: https://sayod111.github.io | Apify Store: https://apify.com/sayod111
