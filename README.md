# FIT4110 Lab 03 - Camera Stream Contract Testing

This repository submits Lab 03 for `team-camera` in the Smart Campus Operations Platform.

## Service Scope

Camera Stream receives camera frames, validates metadata, exposes frame history, and verifies the consumer-side integration path toward AI Vision and Analytics.

## Main Files

```text
contracts/camera-stream.openapi.yaml
postman/collections/FIT4110_lab03_camera_stream.postman_collection.json
postman/environments/FIT4110_lab03_mock.postman_environment.json
postman/environments/FIT4110_lab03_local.postman_environment.json
mock-data/camera-frame-valid.json
mock-data/camera-frame-invalid-short-image.json
mock-data/camera-frame-boundary-motion.json
templates/test-case-matrix.csv
reports/verification-summary.md
```

The legacy classroom template names have been replaced in runnable scripts and submission artifacts.

## Commands

```bash
npm install
npm run mock:camera
npm run test:mock
npm run test:local
```

Mock server:

```text
http://localhost:4010
```

Local service URL:

```text
http://localhost:8000
```

## Test Coverage

- Health endpoint.
- Valid frame upload.
- Frame listing.
- Missing token.
- Invalid image payload.
- Motion score boundary.
- Consumer-side smoke for analyze/dependency behavior.

## Integration Notes For Buoi 6

- Camera Stream exposes `GET /health`.
- Partner URLs must be configured through environment variables.
- Dependency failures must return a controlled `502` or `503`, not hang the service.
