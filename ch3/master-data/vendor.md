# Vendor
- [Vendor](#vendor)
  - [`Vendor`](#vendor-1)
    - [`/v1/data-sync/vendors/{vendor_id}`](#v1data-syncvendorsvendor_id)
      - [`DELETE`](#delete)
        - [`Parameters`](#parameters)
        - [`Responses`](#responses)
    - [`/v1/vendors/{id}`](#v1vendorsid)
      - [`GET`](#get)
        - [`Parameters`](#parameters-1)
        - [`Responses`](#responses-1)
    - [`/v1/vendors:browse-list-id`](#v1vendorsbrowse-list-id)
      - [`POST`](#post)
        - [`Summary`:](#summary)
        - [`Parameters`](#parameters-2)
        - [`Responses`](#responses-2)
    - [`/v1/vendors:search`](#v1vendorssearch)
      - [`GET`](#get-1)
        - [`Summary`:](#summary-1)
        - [`Parameters`](#parameters-3)
        - [`Responses`](#responses-3)
    - [`Models`](#models)
      - [`masterdatav1District`](#masterdatav1district)
      - [`masterdatav1Pagination`](#masterdatav1pagination)
      - [`protobufAny`](#protobufany)
      - [`rpcStatus`](#rpcstatus)
      - [`v1DistrictProvince`](#v1districtprovince)
      - [`v1ListVendorsResponse`](#v1listvendorsresponse)
      - [`v1SearchVendorsRequestEqual`](#v1searchvendorsrequestequal)
      - [`v1SearchVendorsRequestLike`](#v1searchvendorsrequestlike)
      - [`v1SearchVendorsRequestQuery`](#v1searchvendorsrequestquery)
      - [`v1SearchVendorsResponse`](#v1searchvendorsresponse)
      - [`v1Supplier`](#v1supplier)
      - [`v1Vendor`](#v1vendor)
## `Vendor`
### `/v1/data-sync/vendors/{vendor_id}`

#### `DELETE`
##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| vendor_id | path |  | Yes | string |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. |  |
| default | An unexpected error response. | [rpcStatus](#rpcStatus) |

### `/v1/vendors/{id}`

#### `GET`
##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path |  | Yes | string |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v1Vendor](#v1Vendor) |
| default | An unexpected error response. | [rpcStatus](#rpcStatus) |

### `/v1/vendors:browse-list-id`

#### `POST`
##### `Summary`:

Cho phép người dùng xem danh sách các nhà phân phối [Được đồng bộ từ bên thứ 3]

##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v1SearchVendorsRequestQuery](#v1SearchVendorsRequestQuery) |
| like.name | query |  | No | string |
| like.code | query |  | No | string |
| like.phone | query |  | No | string |
| page_number | query |  | No | integer |
| page_size | query |  | No | integer |
| order_by | query |  | No | string |
| equal.active | query |  | No | boolean |
| equal.supplier_id | query |  | No | string |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v1SearchVendorsResponse](#v1SearchVendorsResponse) |
| default | An unexpected error response. | [rpcStatus](#rpcStatus) |

### `/v1/vendors:search`

#### `GET`
##### `Summary`:

Cho phép người dùng xem danh sách các nhà phân phối [Được đồng bộ từ bên thứ 3]

##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| like.name | query |  | No | string |
| like.code | query |  | No | string |
| like.phone | query |  | No | string |
| query.list_id | query |  | No | [ string ] |
| query.list_phone | query |  | No | [ string ] |
| page_number | query |  | No | integer |
| page_size | query |  | No | integer |
| order_by | query |  | No | string |
| equal.active | query |  | No | boolean |
| equal.supplier_id | query |  | No | string |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v1SearchVendorsResponse](#v1SearchVendorsResponse) |
| default | An unexpected error response. | [rpcStatus](#rpcStatus) |

### `Models`


#### `masterdatav1District`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| district_id | integer |  | No |
| province_id | string |  | No |
| name | string |  | No |
| code | string |  | No |
| create_time | dateTime |  | No |
| update_time | dateTime |  | No |
| province | [v1DistrictProvince](#v1DistrictProvince) |  | No |
| sync_histories | [ dateTime ] |  | No |

#### `masterdatav1Pagination`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| page_number | integer |  | No |
| page_size | integer |  | No |
| total_size | integer |  | No |

#### `protobufAny`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| type_url | string |  | No |
| value | byte |  | No |

#### `rpcStatus`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| code | integer |  | No |
| message | string |  | No |
| details | [ [protobufAny](#protobufAny) ] |  | No |

#### `v1DistrictProvince`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| name | string |  | No |

#### `v1ListVendorsResponse`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| vendors | [ [v1Vendor](#v1Vendor) ] |  | No |

#### `v1SearchVendorsRequestEqual`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| active | boolean |  | No |
| supplier_id | string |  | No |

#### `v1SearchVendorsRequestLike`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| name | string |  | No |
| code | string |  | No |
| phone | string |  | No |

#### `v1SearchVendorsRequestQuery`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| list_id | [ string ] |  | No |
| list_phone | [ string ] |  | No |

#### `v1SearchVendorsResponse`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| vendors | [ [v1Vendor](#v1Vendor) ] |  | No |
| pagination | [masterdatav1Pagination](#masterdatav1Pagination) |  | No |

#### `v1Supplier`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| supplier_id | integer |  | No |
| name | string |  | No |
| status | string |  | No |
| create_time | dateTime |  | No |
| update_time | dateTime |  | No |
| phone | string |  | No |
| code | string |  | No |
| sync_histories | [ dateTime ] |  | No |

#### `v1Vendor`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| company_id | string |  | No |
| create_by | string |  | No |
| name | string |  | No |
| image | string |  | No |
| active | boolean |  | No |
| code | string |  | No |
| phone | string |  | No |
| create_time | dateTime |  | No |
| update_time | dateTime |  | No |
| supplier_ids | [ string ] |  | No |
| district_id | string |  | No |
| address | string |  | No |
| sync_histories | [ dateTime ] |  | No |
| district | [masterdatav1District](#masterdatav1District) |  | No |
| suppliers | [ [v1Supplier](#v1Supplier) ] |  | No |