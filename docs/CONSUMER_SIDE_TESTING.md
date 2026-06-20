# Consumer-Side Testing - Camera Stream

Camera Stream is a consumer of two partner services:

- AI Vision: `POST /api/v1/detect`
- Analytics: `POST /api/v1/events`

The Vision request carries `request_id`, `camera_id`, `timestamp`, `location`, `motion_score`, and `image_base64`. This matches the 7-service rule that Camera sends one preprocessed motion snapshot, not the full stream.

The Lab 03 collection includes `Analyze frame handles Vision and Analytics dependency`.

This request checks that Camera Stream either:

- completes the analyze flow when dependencies are available, or
- returns a controlled `502` or `503` Problem Details response when a dependency is unavailable.

This is the expected Buoi 6 behavior: the service must not hang forever when another team service is offline.
