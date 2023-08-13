# Master Server

## Ping

Route: `POST /ping`

Request Body:

| Key             | Type     | Description    |
| --------------- | -------- | -------------- |
| `client_secret` | `string` | Client secret. |

Response Body (200):

| Key       | Type      | Description      |
| --------- | --------- | ---------------- |
| `success` | `boolean` | Response status. |

## Connection Request

Route: `POST /connection/request`

Request Body:

| Key               | Type      | Description         |
| ----------------- | --------- | ------------------- |
| `client_username` | `string`  | Client username.    |
| `client_host`     | `string`  | Client server host. |
| `client_port`     | `integer` | Client server port. |

Response Body (200):

| Key       | Type      | Description      |
| --------- | --------- | ---------------- |
| `success` | `boolean` | Response status. |