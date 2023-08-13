# Remit Protocol

## Base Components

- Master Server + Master-Slave Connection
- Slave Server + Slave-Master Connection

## Master Server

### Public Key

### Connection Request

Route: `POST /connection/request`

Request Body:

| Key | Type | Description |
| --- | ---- | ----------- |
| `client` | `object` | Client information. |
| `client.username` | `string` | Client username. |
| `client.host` | `string` | Client server host. |
| `client.port` | `integer` | Client server port. |

Response Body (200):

| Key | Type | Description |
| --- | ---- | ----------- |
| `success` | `boolean` | Response status. |

## Master-Slave Connection

## Slave Server

## Slave-Master Connection
