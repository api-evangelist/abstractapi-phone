# Abstract API Phone Validation (abstractapi-phone)

Abstract API's Phone Number Validation & Verification API validates and verifies a phone number in a single REST request. Given a number (ideally in E.164 format) it returns whether the number is valid, its local and international formats, the country, the registered location, the line type (mobile, landline, VoIP, and more), and the carrier - useful for form validation, lead scoring, fraud prevention, and cleaning phone data.

**Access model:** Abstract API offers a **free tier** (100 requests/month, no credit card required) plus **paid monthly/annual plans** scaled by request volume. Every request is authenticated with an API key passed as the `api_key` query parameter, and the free and paid tiers share a **3 requests/second** throughput limit. Phone Validation is one product in the broader Abstract API suite (email validation, IP geolocation, company enrichment, and more); each product has its own host and its own API key.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/abstractapi-phone/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/abstractapi-phone/refs/heads/main/apis.yml)

## Tags

- Number Verification
- Phone Validation
- Phone Number
- Phone Number Lookup
- Verification
- Carrier Lookup
- Line Type
- Data Validation

## Timestamps

- **Created:** 2026-07-12
- **Modified:** 2026-07-12

## APIs

### Abstract API Phone Validation API

Single GET endpoint that validates and verifies a phone number and returns validity, local and international formats, country, registered location, line type, and carrier. Authenticated with an `api_key` query parameter; the number is supplied via the `phone` query parameter in E.164 format (for example `+14152007986`).

```
GET https://phonevalidation.abstractapi.com/v1/?api_key=YOUR_API_KEY&phone=+14152007986
```

The endpoint path, HTTP method (GET only), and API-key-by-query-parameter authentication were **live-confirmed on 2026-07-12** against the production host. The response field set below is grounded in Abstract API's published documentation and official SDKs; example values are illustrative.

- **Human URL:** [https://www.abstractapi.com/api/phone-validation-api](https://www.abstractapi.com/api/phone-validation-api)
- **Base URL:** `https://phonevalidation.abstractapi.com/v1`

#### Tags

- Phone Validation
- Number Verification
- Carrier Lookup
- Line Type

#### Properties

- [Documentation](https://www.abstractapi.com/api/phone-validation-api)
- [API Reference](https://www.abstractapi.com/api/phone-validation-api)
- [OpenAPI](openapi/abstractapi-phone-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/abstractapi-phone.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/abstractapi-phone.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

#### Example Response

```json
{
  "phone": "14152007986",
  "valid": true,
  "format": {
    "international": "+14152007986",
    "local": "(415) 200-7986"
  },
  "country": {
    "code": "US",
    "name": "United States",
    "prefix": "+1"
  },
  "location": "California",
  "type": "mobile",
  "carrier": "T-Mobile USA, Inc."
}
```

## Common Properties

- [GitHub Organization](https://github.com/abstractapi)
- [LinkedIn](https://www.linkedin.com/company/abstract-api)
- [Website](https://www.abstractapi.com)
- [Documentation](https://www.abstractapi.com/api/phone-validation-api)
- [Plans](plans/abstractapi-phone-plans-pricing.yml)
- [Rate Limits](rate-limits/abstractapi-phone-rate-limits.yml)
- [Fin Ops](finops/abstractapi-phone-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
