# Brand
- [Brand](#brand)
    - [`/v1/brands:browse-list-id`](#v1brandsbrowse-list-id)
      - [`POST`](#post)
        - [`Parameters`](#parameters)
        - [`Responses`](#responses)
    - [`/v1/brands:search`](#v1brandssearch)
      - [`GET`](#get)
        - [`Parameters`](#parameters-1)
        - [`Responses`](#responses-1)
    - [`Models`](#models)
      - [`masterdatav1Pagination`](#masterdatav1pagination)
      - [`protobufAny`](#protobufany)
      - [`rpcStatus`](#rpcstatus)
      - [`v1Brand`](#v1brand)
      - [`v1SearchBrandsRequestEqual`](#v1searchbrandsrequestequal)
      - [`v1SearchBrandsRequestLike`](#v1searchbrandsrequestlike)
      - [`v1SearchBrandsRequestQuery`](#v1searchbrandsrequestquery)
      - [`v1SearchBrandsResponse`](#v1searchbrandsresponse)
  
### `/v1/brands:browse-list-id`

#### `POST`
##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v1SearchBrandsRequestQuery](#v1SearchBrandsRequestQuery) |
| equal.active | query |  | No | boolean |
| like.name | query |  | No | string |
| like.code | query |  | No | string |
| page_number | query |  | No | integer |
| page_size | query |  | No | integer |
| order_by | query |  | No | string |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v1SearchBrandsResponse](#v1SearchBrandsResponse) |
| default | An unexpected error response. | [rpcStatus](#rpcStatus) |

### `/v1/brands:search`

#### `GET`
##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| equal.active | query |  | No | boolean |
| like.name | query |  | No | string |
| like.code | query |  | No | string |
| page_number | query |  | No | integer |
| page_size | query |  | No | integer |
| order_by | query |  | No | string |
| query.list_id | query |  | No | [ string ] |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v1SearchBrandsResponse](#v1SearchBrandsResponse) |
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

#### `v1Brand`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| brand_id | integer |  | No |
| name | string |  | No |
| image | string |  | No |
| create_time | dateTime |  | No |
| update_time | dateTime |  | No |
| sync_histories | [ dateTime ] |  | No |

#### `v1SearchBrandsRequestEqual`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| active | boolean |  | No |

#### `v1SearchBrandsRequestLike`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| name | string |  | No |
| code | string |  | No |

#### `v1SearchBrandsRequestQuery`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| list_id | [ string ] |  | No |

#### `v1SearchBrandsResponse`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| brands | [ [v1Brand](#v1Brand) ] |  | No |
| pagination | [masterdatav1Pagination](#masterdatav1Pagination) |  | No |