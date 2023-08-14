# Master Server

## Routes

### Ping

Route: `POST /ping`

Request Body:

| Key             | Type     | Description              |
| --------------- | -------- | ------------------------ |
| `client_secret` | `string` | Slave connection secret. |

Response Body (200):

| Key       | Type      | Description      |
| --------- | --------- | ---------------- |
| `success` | `boolean` | Response status. |

### Connection Request

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

### Connection Closed

Route: `POST /connection/close`

Request Body:

| Key             | Type     | Description               |
| --------------- | -------- | ------------------------- |
| `client_secret` | `string` | Master connection secret. |

Response Body (200):

| Key       | Type      | Description      |
| --------- | --------- | ---------------- |
| `success` | `boolean` | Response status. |

### All Listings

Route: `POST /listings/all`

Request Body:

| Key             | Type     | Description               |
| --------------- | -------- | ------------------------- |
| `client_secret` | `string` | Master connection secret. |

Response Body (200):

| Key              | Type      | Description                     |
| ---------------- | --------- | ------------------------------- |
| `success`        | `boolean` | Response status.                |
| `listings_count` | `integer` | Number of listings.             |
| `listings`       | `array`   | All listings.                   |
| `listings.id`    | `string`  | Listing ID.                     |
| `listings.name`  | `string`  | Listing name.                   |
| `listings.type`  | `string`  | Listing type. (`file`/`folder`) |
| `listings.size`  | `integer` | Listing size in `kb`.           |

### Get Listing Folder

Route: `POST /listings/get-folder`

Request Body:

| Key             | Type     | Description               |
| --------------- | -------- | ------------------------- |
| `client_secret` | `string` | Master connection secret. |
| `listing_id`    | `string` | Listing ID.               |

Response Body (200):

| Key              | Type      | Description                     |
| ---------------- | --------- | ------------------------------- |
| `success`        | `boolean` | Response status.                |
| `listings_count` | `integer` | Number of listings.             |
| `listings`       | `array`   | All listings.                   |
| `listings.id`    | `string`  | Listing ID.                     |
| `listings.name`  | `string`  | Listing name.                   |
| `listings.type`  | `string`  | Listing type. (`file`/`folder`) |
| `listings.size`  | `integer` | Listing size in `kb`.           |

### Get Listing File

Route: `POST /listings/get-file`

Request Body:

| Key             | Type     | Description               |
| --------------- | -------- | ------------------------- |
| `client_secret` | `string` | Master connection secret. |
| `listing_id`    | `string` | Listing ID.               |

Response Body (200): Stream of binary data.
