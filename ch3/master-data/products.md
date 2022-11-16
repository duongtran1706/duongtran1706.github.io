# Products
- [Products](#products)
  - [`Products`](#products-1)
    - [/`v1/products/{id}`](#v1productsid)
      - [`GET`](#get)
        - [`Parameters`](#parameters)
        - [`Responses`](#responses)
    - [`/v1/products:browse-list-id`](#v1productsbrowse-list-id)
      - [`POST`](#post)
        - [`Summary`:](#summary)
        - [`Parameters`](#parameters-1)
        - [`Responses`](#responses-1)
    - [`/v1/products:search`](#v1productssearch)
      - [`GET`](#get-1)
        - [`Summary`:](#summary-1)
        - [`Parameters`](#parameters-2)
        - [`Responses`](#responses-2)
    - [`Models`](#models)
      - [`ListProductsResponsePromotion`](#listproductsresponsepromotion)
      - [`UpdateProductRequestUpdateMask`](#updateproductrequestupdatemask)
      - [`masterdatav1District`](#masterdatav1district)
      - [`masterdatav1Pagination`](#masterdatav1pagination)
      - [`masterdatav1Product`](#masterdatav1product)
      - [`protobufAny`](#protobufany)
      - [`rpcStatus`](#rpcstatus)
      - [`v1Brand`](#v1brand)
      - [`v1Category`](#v1category)
      - [`v1DistrictProvince`](#v1districtprovince)
      - [`v1ListProductsRequestProduct`](#v1listproductsrequestproduct)
      - [`v1ListProductsResponse`](#v1listproductsresponse)
      - [`v1ListProductsResponseProduct`](#v1listproductsresponseproduct)
      - [`v1SearchProductsRequestEqual`](#v1searchproductsrequestequal)
      - [`v1SearchProductsRequestLike`](#v1searchproductsrequestlike)
      - [`v1SearchProductsRequestQuery`](#v1searchproductsrequestquery)
      - [`v1SearchProductsResponse`](#v1searchproductsresponse)
      - [`v1Supplier`](#v1supplier)
      - [`v1Vendor`](#v1vendor)
## `Products`

### /`v1/products/{id}`

#### `GET`
##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path |  | Yes | string |
| sku | query |  | No | string |
| company_id | query | company_id. | No | string |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [masterdatav1Product](#masterdatav1Product) |
| default | An unexpected error response. | [rpcStatus](#rpcStatus) |

### `/v1/products:browse-list-id`

#### `POST`
##### `Summary`:

Cho phép người dùng tìm kiếm và lọc các sản phẩm theo điều kiện [Được đồng bộ từ bên thứ 3]

##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v1SearchProductsRequestQuery](#v1SearchProductsRequestQuery) |
| equal.active | query |  | No | boolean |
| equal.company_id | query |  | No | string |
| equal.vendor_id | query |  | No | string |
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

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v1SearchProductsResponse](#v1SearchProductsResponse) |
| default | An unexpected error response. | [rpcStatus](#rpcStatus) |

### `/v1/products:search`

#### `GET`
##### `Summary`:

Cho phép người dùng tìm kiếm và lọc các sản phẩm theo điều kiện [Được đồng bộ từ bên thứ 3]

##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| equal.active | query |  | No | boolean |
| equal.company_id | query |  | No | string |
| equal.vendor_id | query |  | No | string |
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
| query.list_id | query |  | No | [ string ] |
| query.list_sku | query |  | No | [ string ] |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v1SearchProductsResponse](#v1SearchProductsResponse) |
| default | An unexpected error response. | [rpcStatus](#rpcStatus) |

### `Models`


#### `ListProductsResponsePromotion`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| contents | [ string ] |  | No |

#### `UpdateProductRequestUpdateMask`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| active | boolean |  | No |
| name | string |  | No |
| image | string |  | No |
| category_id | string |  | No |
| brand_id | string |  | No |
| vendor_id | string |  | No |
| product_code | string |  | No |
| sku | string |  | No |
| price | double |  | No |
| special_price | double |  | No |
| barcode | string |  | No |
| company_id | string |  | No |

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

#### `masterdatav1Product`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| name | string |  | No |
| image | string |  | No |
| sku | string |  | No |
| price | double |  | No |
| active | boolean |  | No |
| brand | [v1Brand](#v1Brand) |  | No |
| category | [v1Category](#v1Category) |  | No |
| product_code | string |  | No |
| vendor | [v1Vendor](#v1Vendor) |  | No |
| special_price | double |  | No |
| barcode | string |  | No |
| company_id | string |  | No |
| create_time | dateTime |  | No |
| update_time | dateTime |  | No |
| brand_id | string |  | No |
| category_id | string |  | No |
| vendor_id | string |  | No |
| supplier_id | string |  | No |
| sync_histories | [ dateTime ] |  | No |

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

#### `v1DistrictProvince`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| name | string |  | No |

#### `v1ListProductsRequestProduct`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| sku | string |  | No |
| company_id | string |  | No |

#### `v1ListProductsResponse`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| products | [ [v1ListProductsResponseProduct](#v1ListProductsResponseProduct) ] |  | No |

#### `v1ListProductsResponseProduct`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| sku | string |  | No |
| price | double |  | No |
| company_id | string |  | No |
| brand_id | string |  | No |
| category_id | string |  | No |
| vendor_id | string |  | No |
| supplier_id | string |  | No |
| promotions | [ [ListProductsResponsePromotion](#ListProductsResponsePromotion) ] |  | No |
| invalid_promotions | [ string ] |  | No |

#### `v1SearchProductsRequestEqual`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| active | boolean |  | No |
| company_id | string |  | No |
| vendor_id | string |  | No |
| supplier_id | string |  | No |

#### `v1SearchProductsRequestLike`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| name | string |  | No |
| sku | string |  | No |
| brand | string |  | No |
| category | string |  | No |
| vendor | string |  | No |

#### `v1SearchProductsRequestQuery`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| list_id | [ string ] |  | No |
| list_sku | [ string ] |  | No |

#### `v1SearchProductsResponse`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| products | [ [masterdatav1Product](#masterdatav1Product) ] |  | No |
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