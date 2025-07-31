---
layout: page
stoplight-id: jgp44l663ex6d
---

# Welcome 

Verisk Synergy Studio is a risk modeling platform wholly developed, operated, and delivered as a cloud-based 
software as a service (SAAS) product. This platform unifies the core capabilities of industry-leading catastrophe management solutions Touchstone and Touchstone Re along with functionality from AnalyzeRe, Exposure Enterprise Management, and other Verisk applications into a single cloud-managed solution. The platform will be released 
in multiple iterations, starting with a preview release in 2025 and a general availability release 
in 2026.

## About Verisk Synergy Studio APIs

The Synergy Studio APIs are a set of RESTful endpoints that you can use to assess and manage the risks associated with catastrophic events. They enable you to harness the power of the Synergy Studio platform within your applications. You can
tap into the core elements of Synergy Studio and access our risk modeling platform in unique and 
advanced ways.

## Purpose

This content is for informational reference only and provides insight into our progress toward the 
Client Preview release. These APIs are being developed in phases and are subject to change, including URLs, names, and specifications. A finalized version, including the API Reference 
and OpenAPI specification, will be shared upon release. We have organized this posting into two main categories including the: 

- List of API functions
- Technical documentation 
 
Our technical documentation provides API reference, including the request objects and response codes for the endpoints, a mapping table between the Touchstone (Re) SOAP APIs and Synergy Studio REST APIs, and a core workflow to help you 
orient with the Synergy Studio APIs. The documentation is provisional as the APIs are still under development and the reference information is subject to change. 

## What to expect in APIs in the upcoming Client Preview Release 

The initial release of our APIs will mark the transition from the Simple Object Access Protocol (SOAP) to Representational State Transfer (REST) API transformation. Thereby, providing a more efficient, scalable, and modern integration experience. At a high-level, you can expect the following key differences in Synergy Studio APIs:

Aspect | Touchstone & Touchstone Re | Synergy Studio
---------|----------|---------
 Protocol |APIs strictly follow the SOAP protocol | Uses HTTP with standard methods (GET, POST, etc.)
 Payload | The XML payloads are verbose and larger in size. | The JSON payloads are lightweight and compact, reducing bandwidth usage.
 Authentication | The NTLM stateful authentication process requires multiple request-response handshakes. | The JWT Bearer mechanism uses stateless, token-based authentication.
 Response handling | Uses SOAP Faults inside the response body (typically with HTTP 500). | Uses standard HTTP status codes (e.g., 200, 400, 500).

## Early look: 2025 Synergy Studio APIs 

Highlights of APIs for the Client Preview release.

### Activity management

| Function | Operation | URL
|----| ----|----|	
Get activities |	GET |	/api/activity-management/v1/activities
Get activity (includes status) |	GET	| /api/activity-management/v1/activities/{sid}
Get activity status only |	GET	| /api/activity-management/v1/activities/{sid}/status
Cancel activity | POST | /api/activity-management/v1/activities/{sid}/actions/cancel

### Detailed loss 

| Function | Operation | URL
|----| ----|----|
Submit detailed loss analysis |	POST |	/api/detailed-loss-analysis/v1/detailed-loss

### Event set management	

| Function | Operation | URL
|----| ----|----|
Get event sets	| GET |	/api/exposure-management/v1/event-sets
Get event set |	GET | 	/api/exposure-management/v1/event-sets/{sid}

### Loss modification

| Function | Operation | URL
|----| ----|----|
Get loss modification templates |	GET | /api/loss-modification/v1/templates
Get loss modification template	| GET | /api/loss-modification/v1/templates/{sid}

### Loss set management	

| Function | Operation | URL
|----| ----|----|
Create new loss set |	POST	| /api/loss-set-management/v1/loss-sets

### Program management

| Function | Operation | URL
|----| ----|----|
List programs |	GET 	| /api/program-management/v1/programs
Create program |	POST	| /api/program-management/v1/programs
Create layer	| POST	| /api/program-management/v1/programs/{sid}/layers
Create scenario	| POST | /api/program-management/v1/programs/{sid}/scenarios

### Reference

| Function | Operation | URL
|----| ----|----|
Retrieve currencies |	GET |	/api/reference/v1/currencies
Retrieve perils |	GET |	/api/reference/v1/perils
Retrieve analysis types |	GET |	/api/reference/v1/analysis-types
Retrieve analysis target types |	GET |	/api/reference/v1/analysis-target-types
Retrieve geographic levels |	GET |	/api/reference/v1/geo-levels

### Reinsurance loss

| Function | Operation | URL
|----| ----|----|
Submit reinsurance loss analysis |	POST |	/api/reinsurance-analysis/v1/program-analyses
Get reinsurance analyses |	GET | 	/api/reinsurance-analysis/v1/program-analyses/{sid}
Get reinsurance loss analysis |	GET |	/api/reinsurance-analysis/v1/program-analyses/{sid}
Delete reinsurance loss analysis |	DELETE |	/api/reinsurance-analysis/v1/program-analyses/{sid}

## Useful links

- [Touchstone API Reference](https://docs.air-worldwide.com/APIs/Touchstone/12.0/api-reference/webframe.html)
- [Touchstone Re API Reference](https://docs.air-worldwide.com/APIs/TouchstoneRe/12.0/api-reference/webframe.html)
- [Graphene API Reference](https://graphene.analyzere.net/index.html)

## Support

Any questions? [Contact us](https://www.verisk.com/company/contact/extreme-event-risk-solutions-support/)
