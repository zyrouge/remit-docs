# Master Server

## Ping

Route: `POST /ping`

Request Body:

| Key             | Type     | Description              |
| --------------- | -------- | ------------------------ |
| `client_secret` | `string` | Slave connection secret. |

Response Body (200):

| Key       | Type      | Description      |
| --------- | --------- | ---------------- |
| `success` | `boolean` | Response status. |

## Connection Request

Route: `POST /connection/request`

Request Body:

| Key               | Type      | Description        |
| ----------------- | --------- | ------------------ |
| `client_username` | `string`  | Slave username.    |
| `client_host`     | `string`  | Slave server host. |
| `client_port`     | `integer` | Slave server port. |

Response Body (200):

| Key       | Type      | Description      |
| --------- | --------- | ---------------- |
| `success` | `boolean` | Response status. |

## Connection Closed

Route: `POST /connection/close`

Request Body:

| Key             | Type     | Description               |
| --------------- | -------- | ------------------------- |
| `server_secret` | `string` | Master connection secret. |

Response Body (200):

| Key       | Type      | Description      |
| --------- | --------- | ---------------- |
| `success` | `boolean` | Response status. |
