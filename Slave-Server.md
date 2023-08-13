# Slave Server

## Ping

Route: `POST /ping`

Request Body:

| Key             | Type     | Description    |
| --------------- | -------- | -------------- |
| `server_secret` | `string` | Server secret. |

Response Body (200):

| Key       | Type      | Description      |
| --------- | --------- | ---------------- |
| `success` | `boolean` | Response status. |
