# Lab 03 Verification Summary

- Service: `camera-stream`
- Contract: `contracts/camera-stream.openapi.yaml`
- Collection: `postman/collections/FIT4110_lab03_camera_stream.postman_collection.json`
- Environments: mock and local use `baseUrl` and `authToken` variables.
- Coverage: health, valid frame upload, list frames, auth failure, invalid image payload, motion boundary, dependency/analyze behavior, local latency.
- OpenAPI validation: valid with intentional localhost warnings for Prism/local lab workflow.
