# Product-variant
- [Product-variant](#product-variant)
  - [`Product-variant`](#product-variant-1)
    - [`/v1/product-variants:browse-list-sku`](#v1product-variantsbrowse-list-sku)
      - [`POST`](#post)
        - [`Summary`:](#summary)
        - [`Parameters`](#parameters)
        - [`Responses`](#responses)
    - [`/v1/product-variants:search`](#v1product-variantssearch)
      - [`GET`](#get)
        - [`Summary`:](#summary-1)
        - [`Parameters`](#parameters-1)
        - [`Responses`](#responses-1)
    - [`Models`](#models)
      - [`protobufAny`](#protobufany)
      - [`rpcStatus`](#rpcstatus)
      - [`v1Brand`](#v1brand)
      - [`v1Category`](#v1category)
      - [`v1ProductVariant`](#v1productvariant)
      - [`v1SearchProductVariantsRequestEqual`](#v1searchproductvariantsrequestequal)
      - [`v1SearchProductVariantsRequestLike`](#v1searchproductvariantsrequestlike)
      - [`v1SearchProductVariantsRequestQuery`](#v1searchproductvariantsrequestquery)
      - [`v1SearchProductVariantsResponse`](#v1searchproductvariantsresponse)
      - [`v1SearchProductVariantsResponsePagination`](#v1searchproductvariantsresponsepagination)
      - [`v1Supplier`](#v1supplier)
## `Product-variant`

### `/v1/product-variants:browse-list-sku`

#### `POST`
##### `Summary`:

Cho phép người dùng tìm kiếm và lọc các sản phẩm theo điều kiện [Được đồng bộ từ bên thứ 3]

##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v1SearchProductVariantsRequestQuery](#v1SearchProductVariantsRequestQuery) |
| equal.active | query |  | No | boolean |
| equal.company_id | query |  | No | string |
| equal.supplier_id | query |  | No | string |
| like.name | query |  | No | string |
| like.sku | query |  | No | string |
| like.brand | query |  | No | string |
| like.category | query |  | No | string |
| like.vendor | query |  | No | string |
| page_number | query |  | No | integer |
| page_size | query |  | No | integer |
| order_by | query |  | No | string |
| company_id | query | company_id. | No | string |
| product_variant_ids | query |  | No | [ string ] |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v1SearchProductVariantsResponse](#v1SearchProductVariantsResponse) |
| default | An unexpected error response. | [rpcStatus](#rpcStatus) |

### `/v1/product-variants:search`

#### `GET`
##### `Summary`:

Cho phép người dùng tìm kiếm và lọc các sản phẩm theo điều kiện [Được đồng bộ từ bên thứ 3]

##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| equal.active | query |  | No | boolean |
| equal.company_id | query |  | No | string |
| equal.supplier_id | query |  | No | string |
| like.name | query |  | No | string |
| like.sku | query |  | No | string |
| like.brand | query |  | No | string |
| like.category | query |  | No | string |
| like.vendor | query |  | No | string |
| page_number | query |  | No | integer |
| page_size | query |  | No | integer |
| order_by | query |  | No | string |
| company_id | query | company_id. | No | string |
| query.product_variant_skus | query |  | No | [ string ] |
| product_variant_ids | query |  | No | [ string ] |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v1SearchProductVariantsResponse](#v1SearchProductVariantsResponse) |
| default | An unexpected error response. | [rpcStatus](#rpcStatus) |

### `Models`


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

#### `v1Category`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| category_id | integer |  | No |
| name | string |  | No |
| image | string |  | No |
| icon | string |  | No |
| is_root | boolean |  | No |
| parent_id | string |  | No |
| active | boolean |  | No |
| childs | [ [v1Category](#v1Category) ] |  | No |
| create_time | dateTime |  | No |
| update_time | dateTime |  | No |
| have_childs | boolean |  | No |
| sync_histories | [ dateTime ] |  | No |

#### `v1ProductVariant`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| name | string |  | No |
| sku | string |  | No |
| active | boolean |  | No |
| barcode | string |  | No |
| brand | [v1Brand](#v1Brand) |  | No |
| brand_id | string |  | No |
| category | [v1Category](#v1Category) |  | No |
| category_id | string |  | No |
| create_time | dateTime |  | No |
| update_time | dateTime |  | No |
| supplier_id | string |  | No |
| image | string |  | No |
| product_code | string |  | No |
| supplier | [v1Supplier](#v1Supplier) |  | No |
| sync_histories | [ dateTime ] |  | No |

#### `v1SearchProductVariantsRequestEqual`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| active | boolean |  | No |
| company_id | string |  | No |
| supplier_id | string |  | No |

#### `v1SearchProductVariantsRequestLike`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| name | string |  | No |
| sku | string |  | No |
| brand | string |  | No |
| category | string |  | No |
| vendor | string |  | No |

#### `v1SearchProductVariantsRequestQuery`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| product_variant_skus | [ string ] |  | No |

#### `v1SearchProductVariantsResponse`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| product_variants | [ [v1ProductVariant](#v1ProductVariant) ] |  | No |
| pagination | [v1SearchProductVariantsResponsePagination](#v1SearchProductVariantsResponsePagination) |  | No |

#### `v1SearchProductVariantsResponsePagination`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| page_number | integer |  | No |
| page_size | integer |  | No |
| total_size | integer |  | No |

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