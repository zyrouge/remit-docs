# Remit Protocol

## Base Components

- Master Server + Master-Slave Connection
- Slave Server + Slave-Master Connection

## Master Server

### Connection Request

Route: `/connection/request`

Body:

| Key | Type | Description |
| --- | ---- | ----------- |
| `client` | `object` | Client information. |
| `client.username` | `string` | Client username. |
| `client.host` | `string` | Client server host. |
| `client.port` | `integer` | Client server port. |

## Master-Slave Connection

## Slave Server

## Slave-Master Connection
