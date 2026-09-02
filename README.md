
# ClicknPay Integration

Replaces Paynow with ClicknPay (openapi.africa) for gwkeyslocksmiths.jh.frappe.cloud

## Install

bench new-app clicknpay_integration --no-git (then copy these files over)
bench --site gwkeyslocksmiths.jh.frappe.cloud install-app clicknpay_integration
bench --site gwkeyslocksmiths.jh.frappe.cloud migrate

## Config

In site_config.json add:

{
  "clicknpay_public_id": "HQGVaTYJihldpvzsw"
}

For live, replace with live ID from openapi.africa dashboard.

## Endpoints

- POST /api/method/clicknpay_integration.api.initiate_payment?reference=SINV-0001
- GET /api/method/clicknpay_integration.api.check_status?reference=SINV-0001
- GET /api/method/clicknpay_integration.api.clicknpay_callback?clientReference=SINV-0001

