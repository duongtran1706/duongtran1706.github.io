# BusinessType
- [BusinessType](#businesstype)
  - [`BusinessType`](#businesstype-1)
    - [`/v1/business-types:browse-list-id`](#v1business-typesbrowse-list-id)
      - [`POST`](#post)
        - [`Parameters`](#parameters)
        - [`Responses`](#responses)
    - [`/v1/business-types:search`](#v1business-typessearch)
      - [`GET`](#get)
        - [`Parameters`](#parameters-1)
        - [`Responses`](#responses-1)
    - [`Models`](#models)
      - [`masterdatav1Pagination`](#masterdatav1pagination)
      - [`protobufAny`](#protobufany)
      - [`rpcStatus`](#rpcstatus)
      - [`v1BusinessType`](#v1businesstype)
      - [`v1SearchBusinessTypesRequestLike`](#v1searchbusinesstypesrequestlike)
      - [`v1SearchBusinessTypesRequestQuery`](#v1searchbusinesstypesrequestquery)
      - [`v1SearchBusinessTypesResponse`](#v1searchbusinesstypesresponse)

## `BusinessType`

### `/v1/business-types:browse-list-id`

#### `POST`
##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v1SearchBusinessTypesRequestQuery](#v1SearchBusinessTypesRequestQuery) |
| like.name | query |  | No | string |
| like.code | query |  | No | string |
| page_number | query |  | No | integer |
| page_size | query |  | No | integer |
| order_by | query |  | No | string |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v1SearchBusinessTypesResponse](#v1SearchBusinessTypesResponse) |
| default | An unexpected error response. | [rpcStatus](#rpcStatus) |

### `/v1/business-types:search`

#### `GET`
##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| like.name | query |  | No | string |
| like.code | query |  | No | string |
| page_number | query |  | No | integer |
| page_size | query |  | No | integer |
| order_by | query |  | No | string |
| query.list_id | query |  | No | [ string ] |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v1SearchBusinessTypesResponse](#v1SearchBusinessTypesResponse) |
| default | An unexpected error response. | [rpcStatus](#rpcStatus) |

### `Models`


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

#### `v1BusinessType`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| name | string |  | No |
| code | string |  | No |
| create_time | dateTime |  | No |
| update_time | dateTime |  | No |
| business_type_id | integer |  | No |
| sync_histories | [ dateTime ] |  | No |

#### `v1SearchBusinessTypesRequestLike`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| name | string |  | No |
| code | string |  | No |

#### `v1SearchBusinessTypesRequestQuery`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| list_id | [ string ] |  | No |

#### `v1SearchBusinessTypesResponse`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| pagination | [masterdatav1Pagination](#masterdatav1Pagination) |  | No |
| business_types | [ [v1BusinessType](#v1BusinessType) ] |  | No |