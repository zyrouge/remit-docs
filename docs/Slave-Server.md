# Slave Server

## Ping

Route: `POST /ping`

Request Body:

| Key             | Type     | Description               |
| --------------- | -------- | ------------------------- |
| `server_secret` | `string` | Master connection secret. |

Response Body (200):

| Key       | Type      | Description      |
| --------- | --------- | ---------------- |
| `success` | `boolean` | Response status. |

## Connection Accepted

Route: `POST /connection/accept`

Request Body:

| Key               | Type      | Description               |
| ----------------- | --------- | ------------------------- |
| `server_username` | `string`  | Master username.          |
| `server_host`     | `string`  | Master server host.       |
| `server_port`     | `integer` | Master server port.       |
| `client_secret`   | `integer` | Master connection secret. |

Response Body (200):

| Key       | Type      | Description      |
| --------- | --------- | ---------------- |
| `success` | `boolean` | Response status. |

## Connection Closed

Route: `POST /connection/close`

Request Body:

| Key             | Type     | Description              |
| --------------- | -------- | ------------------------ |
| `cleint_secret` | `string` | Slave connection secret. |

Response Body (200):

| Key       | Type      | Description      |
| --------- | --------- | ---------------- |
| `success` | `boolean` | Response status. |
