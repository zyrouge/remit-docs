# Slave Server

## Routes

### Ping

Route: `POST /ping`

Request Body:

| Key             | Type     | Description               |
| --------------- | -------- | ------------------------- |
| `server_secret` | `string` | Master connection secret. |

Response Body (200):

| Key       | Type      | Description      |
| --------- | --------- | ---------------- |
| `success` | `boolean` | Response status. |

### Connection Accepted

Route: `POST /connection/accept`

Request Body:

| Key               | Type      | Description               |
| ----------------- | --------- | ------------------------- |
| `server_username` | `string`  | Master username.          |
| `server_host`     | `string`  | Master server host.       |
| `server_port`     | `integer` | Master server port.       |
| `server_secret`   | `string`  | Master connection secret. |
| `client_secret`   | `integer` | Slave connection secret.  |
| `invite_code`     | `string`  | Invite code.              |

Response Body (200):

| Key       | Type      | Description      |
| --------- | --------- | ---------------- |
| `success` | `boolean` | Response status. |

### Connection Closed

Route: `POST /connection/close`

Request Body:

| Key             | Type     | Description               |
| --------------- | -------- | ------------------------- |
| `server_secret` | `string` | Master connection secret. |

Response Body (200):

| Key       | Type      | Description      |
| --------- | --------- | ---------------- |
| `success` | `boolean` | Response status. |
