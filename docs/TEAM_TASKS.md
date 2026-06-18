# Team Camera Tasks

## Service

`team-camera` implements Camera Stream.

## Required Endpoints

- `GET /health`
- `POST /api/v1/frames`
- `GET /api/v1/frames`
- `GET /api/v1/frames/{frame_id}`
- `POST /api/v1/frames/{frame_id}/analyze`

## Lab 03 Deliverables

- Camera OpenAPI contract.
- Prism mock server from the contract.
- Postman/Newman collection for mock and local environments.
- Tests for functional, auth, negative, boundary, consumer-side smoke, and local-only latency behavior.

## Partner Contracts

- Camera Stream calls AI Vision at `POST /api/v1/detect`.
- Camera Stream sends camera events to Analytics at `POST /api/v1/events`.
