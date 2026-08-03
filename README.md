# Abstract API Phone Validation (abstractapi-phone)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
