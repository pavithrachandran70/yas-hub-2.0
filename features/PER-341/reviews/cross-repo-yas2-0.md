## ADLC cross-repo check

This PR changes files in **yas2-0** that provide contracts other services use. If a contract below changes or goes away, check its users before merging.

**Services outside this feature that use them:** yas2-0/recommendation, yas2-0/search, yas2-0/webhook

- `broker::kafka` (broker), provided at `docker-compose.yml:550`
  - used by **yas2-0/recommendation** at `recommendation/src/main/resources/application.properties:49`
  - used by **yas2-0/search** at `search/src/main/resources/application.properties:28`
  - used by **yas2-0/webhook** at `webhook/src/main/java/com/yas/webhook/integration/inbound/OrderEventInbound.java:16`
  - used by **yas2-0/webhook** at `webhook/src/main/java/com/yas/webhook/integration/inbound/ProductEventInbound.java:16`
  - used by **yas2-0/webhook** at `webhook/src/main/resources/application.properties:32`

_From the repo graph of the base branch. A warning only: it does not block the merge._
