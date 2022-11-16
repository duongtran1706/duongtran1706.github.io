# Code
- [Code](#code)
  - [`Code`](#code-1)
    - [Miêu tả](#miêu-tả)
    - [`/v2/codes/{code_id}/agents:histories-used`](#v2codescode_idagentshistories-used)
      - [`GET`](#get)
        - [`Summary`:](#summary)
        - [`Parameters`](#parameters)
        - [`Responses`](#responses)
    - [`/v2/codes/{code_id}/publish-codes`](#v2codescode_idpublish-codes)
      - [`GET`](#get-1)
        - [`Summary`:](#summary-1)
        - [`Parameters`](#parameters-1)
        - [`Responses`](#responses-1)
    - [`/v2/codes::count`](#v2codescount)
      - [`GET`](#get-2)
        - [`Parameters`](#parameters-2)
        - [`Responses`](#responses-2)
    - [`/v2/codes:allocate`](#v2codesallocate)
      - [`POST`](#post)
        - [`Summary`:](#summary-2)
        - [`Parameters`](#parameters-3)
        - [`Responses`](#responses-3)
    - [`/v2/codes:publish`](#v2codespublish)
      - [`POST`](#post-1)
        - [`Summary`:](#summary-3)
        - [`Parameters`](#parameters-4)
        - [`Responses`](#responses-4)
    - [`/v2/codes:search`](#v2codessearch)
      - [`GET`](#get-3)
        - [`Summary`:](#summary-4)
        - [`Parameters`](#parameters-5)
        - [`Responses`](#responses-5)
    - [`/v2/promotions/{promotion_id}/codes:search`](#v2promotionspromotion_idcodessearch)
      - [`GET`](#get-4)
        - [`Summary`:](#summary-5)
        - [`Parameters`](#parameters-6)
        - [`Responses`](#responses-6)
    - [`/v2/{promotion_id}/codes:allocated`](#v2promotion_idcodesallocated)
      - [`GET`](#get-5)
        - [`Parameters`](#parameters-7)
        - [`Responses`](#responses-7)
    - [`Models`](#models)
      - [`AllocateCodesRequestAllocate`](#allocatecodesrequestallocate)
      - [`CodeSettingCodeType`](#codesettingcodetype)
      - [`CodeSettingTypeCode`](#codesettingtypecode)
      - [`ConditionUsageMaxTimesPerPerson`](#conditionusagemaxtimesperperson)
      - [`ConditionUsageMaxTimesPerPersonPerTime`](#conditionusagemaxtimesperpersonpertime)
      - [`ConditionUsageMaxTimesUsage`](#conditionusagemaxtimesusage)
      - [`ContentEvent`](#contentevent)
      - [`DistrictProvince`](#districtprovince)
      - [`ListHistoriesUsedCodeResponseHistory`](#listhistoriesusedcoderesponsehistory)
      - [`MaxTimesPerPersonPerTimeTimeType`](#maxtimesperpersonpertimetimetype)
      - [`PublishCodePublishStatus`](#publishcodepublishstatus)
      - [`googlerpcStatus`](#googlerpcstatus)
      - [`masterdatav1Agent`](#masterdatav1agent)
      - [`promotionv2MaxTimes`](#promotionv2maxtimes)
      - [`protobufAny`](#protobufany)
      - [`v1BusinessType`](#v1businesstype)
      - [`v1District`](#v1district)
      - [`v1LocationType`](#v1locationtype)
      - [`v1Supplier`](#v1supplier)
      - [`v1Vendor`](#v1vendor)
      - [`v2AllocateCodesRequest`](#v2allocatecodesrequest)
      - [`v2AllocateCodesResponse`](#v2allocatecodesresponse)
      - [`v2Code`](#v2code)
      - [`v2CodeCodeStatus`](#v2codecodestatus)
      - [`v2CodeMaxTimes`](#v2codemaxtimes)
      - [`v2CodeSetting`](#v2codesetting)
      - [`v2ConditionUsage`](#v2conditionusage)
      - [`v2Content`](#v2content)
      - [`v2CountCodeResponse`](#v2countcoderesponse)
      - [`v2CountCodeResponseStatus`](#v2countcoderesponsestatus)
      - [`v2ListAllocateCodesRequestEqual`](#v2listallocatecodesrequestequal)
      - [`v2ListAllocateCodesResponse`](#v2listallocatecodesresponse)
      - [`v2ListAllocateCodesResponsePagination`](#v2listallocatecodesresponsepagination)
      - [`v2ListHistoriesUsedCodeResponse`](#v2listhistoriesusedcoderesponse)
      - [`v2ListPublishCodesResponse`](#v2listpublishcodesresponse)
      - [`v2ListPublishCodesResponsePagination`](#v2listpublishcodesresponsepagination)
      - [`v2Promotion`](#v2promotion)
      - [`v2PromotionBelongTo`](#v2promotionbelongto)
      - [`v2PromotionBelongToType`](#v2promotionbelongtotype)
      - [`v2PromotionKind`](#v2promotionkind)
      - [`v2PromotionMethod`](#v2promotionmethod)
      - [`v2PromotionStatus`](#v2promotionstatus)
      - [`v2PromotionType`](#v2promotiontype)
      - [`v2PublishCode`](#v2publishcode)
      - [`v2PublishCodeBody`](#v2publishcodebody)
      - [`v2PublishCodesRequest`](#v2publishcodesrequest)
      - [`v2PublishCodesResponse`](#v2publishcodesresponse)
      - [`v2PublishDestinationType`](#v2publishdestinationtype)
      - [`v2PublishMethod`](#v2publishmethod)
      - [`v2ResourceAllocated`](#v2resourceallocated)
      - [`v2SearchCodesRequestCodeStatus`](#v2searchcodesrequestcodestatus)
      - [`v2SearchCodesRequestEqual`](#v2searchcodesrequestequal)
      - [`v2SearchCodesRequestLike`](#v2searchcodesrequestlike)
      - [`v2SearchCodesResponse`](#v2searchcodesresponse)
      - [`v2SearchCodesResponsePagination`](#v2searchcodesresponsepagination)
## `Code`
 ### Miêu tả 
  - entity này sử lý việc voucher code hoạt động như nào.
  - 
### `/v2/codes/{code_id}/agents:histories-used`

#### `GET`
##### `Summary`:

Cho phép người dùng lấy danh sách lịch sử sử dụng của mã khuyến mãi

##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| code_id | path |  | Yes | string |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v2ListHistoriesUsedCodeResponse](#v2ListHistoriesUsedCodeResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

### `/v2/codes/{code_id}/publish-codes`

#### `GET`
##### `Summary`:

Cho phép người dùng lấy danh sách lịch sử phát mã khuyến mãi ở tab quản lí mã khuyến mãi

##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| code_id | path |  | Yes | string |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v2ListPublishCodesResponse](#v2ListPublishCodesResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

### `/v2/codes::count`

#### `GET`
##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| promotion_id | query |  | No | string |
| equal.status | query |  | No | string |
| equal.number_of_use | query |  | No | integer |
| like.code | query |  | No | string |
| page_number | query |  | No | integer |
| page_size | query |  | No | integer |
| order_by | query |  | No | string |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v2CountCodeResponse](#v2CountCodeResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

### `/v2/codes:allocate`

#### `POST`
##### `Summary`:

Cho phép người dùng phát mã khuyến mãi

##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v2AllocateCodesRequest](#v2AllocateCodesRequest) |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v2AllocateCodesResponse](#v2AllocateCodesResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

### `/v2/codes:publish`

#### `POST`
##### `Summary`:

Cho phép người dùng phát mã khuyến mãi

##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v2PublishCodesRequest](#v2PublishCodesRequest) |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v2PublishCodesResponse](#v2PublishCodesResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

### `/v2/codes:search`

#### `GET`
##### `Summary`:

Cho phép người dùng tìm kiếm mã theo điều kiện

##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| promotion_id | query |  | No | string |
| equal.status | query |  | No | string |
| equal.number_of_use | query |  | No | integer |
| like.code | query |  | No | string |
| page_number | query |  | No | integer |
| page_size | query |  | No | integer |
| order_by | query |  | No | string |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v2SearchCodesResponse](#v2SearchCodesResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

### `/v2/promotions/{promotion_id}/codes:search`

#### `GET`
##### `Summary`:

Cho phép người dùng tìm kiếm mã theo điều kiện

##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| promotion_id | path |  | Yes | string |
| equal.status | query |  | No | string |
| equal.number_of_use | query |  | No | integer |
| like.code | query |  | No | string |
| page_number | query |  | No | integer |
| page_size | query |  | No | integer |
| order_by | query |  | No | string |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v2SearchCodesResponse](#v2SearchCodesResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

### `/v2/{promotion_id}/codes:allocated`

#### `GET`
##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| promotion_id | path |  | Yes | string |
| page_number | query |  | No | integer |
| page_size | query |  | No | integer |
| order_by | query |  | No | string |
| equal.phone | query |  | No | string |
| equal.code | query |  | No | string |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v2ListAllocateCodesResponse](#v2ListAllocateCodesResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

### `Models`


#### `AllocateCodesRequestAllocate`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| promotion_id | string |  | Yes |
| phone | string |  | Yes |
| number_of_codes_allocate | integer |  | Yes |

#### `CodeSettingCodeType`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| CodeSettingCodeType | string |  |  |

#### `CodeSettingTypeCode`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| CodeSettingTypeCode | string |  |  |

#### `ConditionUsageMaxTimesPerPerson`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| is_limit | boolean |  | No |
| count | integer |  | No |

#### `ConditionUsageMaxTimesPerPersonPerTime`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| is_limit | boolean |  | No |
| count | integer |  | No |
| time_type | [MaxTimesPerPersonPerTimeTimeType](#MaxTimesPerPersonPerTimeTimeType) |  | No |

#### `ConditionUsageMaxTimesUsage`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| is_limit | boolean |  | No |
| count | integer |  | No |

#### `ContentEvent`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| type | string |  | No |
| params | string |  | No |

#### `DistrictProvince`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| name | string |  | No |

#### `ListHistoriesUsedCodeResponseHistory`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| name | string |  | No |
| phone | string |  | No |
| used_time | dateTime |  | No |
| order_codes | [ string ] |  | No |

#### `MaxTimesPerPersonPerTimeTimeType`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| MaxTimesPerPersonPerTimeTimeType | string |  |  |

#### `PublishCodePublishStatus`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| PublishCodePublishStatus | string |  |  |

#### `googlerpcStatus`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| code | integer |  | No |
| message | string |  | No |
| details | [ [protobufAny](#protobufAny) ] |  | No |

#### `masterdatav1Agent`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| name | string |  | No |
| phone | string |  | No |
| status | string |  | No |
| business_type_id | string |  | No |
| location_type_id | string |  | No |
| vendor_ids | [ string ] |  | No |
| district_id | string |  | No |
| create_time | dateTime |  | No |
| update_time | dateTime |  | No |
| business_type | [v1BusinessType](#v1BusinessType) |  | No |
| location_type | [v1LocationType](#v1LocationType) |  | No |
| vendors | [ [v1Vendor](#v1Vendor) ] |  | No |
| asset_status | string |  | No |
| total_ordered | integer |  | No |
| supplier_ids | [ string ] |  | No |
| agent_id | string |  | No |
| district | [v1District](#v1District) |  | No |
| suppliers | [ [v1Supplier](#v1Supplier) ] |  | No |
| sync_histories | [ dateTime ] |  | No |

#### `promotionv2MaxTimes`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| is_limit | boolean |  | No |
| count | integer |  | No |

#### `protobufAny`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| type_url | string |  | No |
| value | byte |  | No |

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

#### `v1District`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| district_id | integer |  | No |
| province_id | string |  | No |
| name | string |  | No |
| code | string |  | No |
| create_time | dateTime |  | No |
| update_time | dateTime |  | No |
| province | [DistrictProvince](#DistrictProvince) |  | No |
| sync_histories | [ dateTime ] |  | No |

#### `v1LocationType`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| name | string |  | No |
| code | string |  | No |
| create_time | dateTime |  | No |
| update_time | dateTime |  | No |
| location_type_id | integer |  | No |
| sync_histories | [ dateTime ] |  | No |

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
| district | [v1District](#v1District) |  | No |
| suppliers | [ [v1Supplier](#v1Supplier) ] |  | No |

#### `v2AllocateCodesRequest`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| allocates | [ [AllocateCodesRequestAllocate](#AllocateCodesRequestAllocate) ] |  | Yes |
| content | string |  | Yes |
| title | string |  | Yes |

#### `v2AllocateCodesResponse`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| codes_allocated | [ [v2ResourceAllocated](#v2ResourceAllocated) ] |  | No |

#### `v2Code`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| code | string |  | No |
| number_of_use | integer |  | No |
| status | [v2CodeCodeStatus](#v2CodeCodeStatus) |  | No |
| create_time | dateTime |  | No |
| update_time | dateTime |  | No |
| start_time | dateTime |  | No |
| expire_time | dateTime |  | No |
| max_times_per_code | [v2CodeMaxTimes](#v2CodeMaxTimes) |  | No |
| max_times_per_person | [v2CodeMaxTimes](#v2CodeMaxTimes) |  | No |
| promotion | [v2Promotion](#v2Promotion) |  | No |
| agents_receive_code | [ string ] |  | No |

#### `v2CodeCodeStatus`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v2CodeCodeStatus | string |  |  |

#### `v2CodeMaxTimes`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| is_limit | boolean |  | No |
| count | integer |  | No |

#### `v2CodeSetting`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| is_use_code | boolean |  | No |
| code_type | [CodeSettingCodeType](#CodeSettingCodeType) |  | No |
| max_times_per_person | [promotionv2MaxTimes](#promotionv2MaxTimes) |  | No |
| count | integer |  | No |
| max_times_per_code | [promotionv2MaxTimes](#promotionv2MaxTimes) |  | No |
| type | [CodeSettingTypeCode](#CodeSettingTypeCode) |  | No |
| prefix | string |  | No |
| postfix | string |  | No |
| code_length | integer |  | No |

#### `v2ConditionUsage`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| max_times_usage | [ConditionUsageMaxTimesUsage](#ConditionUsageMaxTimesUsage) |  | No |
| max_times_per_person | [ConditionUsageMaxTimesPerPerson](#ConditionUsageMaxTimesPerPerson) |  | No |
| max_times_per_person_per_time | [ConditionUsageMaxTimesPerPersonPerTime](#ConditionUsageMaxTimesPerPersonPerTime) |  | No |

#### `v2Content`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| conditions | string |  | No |
| event | [ContentEvent](#ContentEvent) |  | No |

#### `v2CountCodeResponse`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| statuses | [ [v2CountCodeResponseStatus](#v2CountCodeResponseStatus) ] |  | No |

#### `v2CountCodeResponseStatus`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| status | string |  | No |
| number | integer |  | No |

#### `v2ListAllocateCodesRequestEqual`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| phone | string |  | No |
| code | string |  | No |

#### `v2ListAllocateCodesResponse`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| codes_allocated | [ [v2ResourceAllocated](#v2ResourceAllocated) ] |  | No |
| pagination | [v2ListAllocateCodesResponsePagination](#v2ListAllocateCodesResponsePagination) |  | No |

#### `v2ListAllocateCodesResponsePagination`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| page_number | integer |  | No |
| page_size | integer |  | No |
| total_size | integer |  | No |

#### `v2ListHistoriesUsedCodeResponse`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| histories | [ [ListHistoriesUsedCodeResponseHistory](#ListHistoriesUsedCodeResponseHistory) ] |  | No |

#### `v2ListPublishCodesResponse`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| publish_codes | [ [v2PublishCode](#v2PublishCode) ] |  | No |
| pagination | [v2ListPublishCodesResponsePagination](#v2ListPublishCodesResponsePagination) |  | No |

#### `v2ListPublishCodesResponsePagination`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| page_number | integer |  | No |
| page_size | integer |  | No |
| total_size | integer |  | No |

#### `v2Promotion`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| name | string |  | No |
| start_time | dateTime |  | No |
| expire_time | dateTime |  | No |
| type | [v2PromotionType](#v2PromotionType) |  | No |
| status | [v2PromotionStatus](#v2PromotionStatus) |  | No |
| creator | string |  | No |
| create_time | dateTime |  | No |
| update_time | dateTime |  | No |
| content | string |  | No |
| description | string |  | No |
| detail | string |  | No |
| company_id | string |  | No |
| vendor_name | string |  | No |
| contents | [ [v2Content](#v2Content) ] |  | No |
| priority | integer |  | No |
| method | [v2PromotionMethod](#v2PromotionMethod) |  | No |
| condition_usage | [v2ConditionUsage](#v2ConditionUsage) |  | No |
| targets | string |  | No |
| code_setting | [v2CodeSetting](#v2CodeSetting) |  | No |
| belong_to | [v2PromotionBelongTo](#v2PromotionBelongTo) |  | No |
| channels | [ string ] |  | No |
| kind | [v2PromotionKind](#v2PromotionKind) |  | No |
| detail_name | string |  | No |
| number_of_use | integer |  | No |

#### `v2PromotionBelongTo`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| name | string |  | No |
| type | [v2PromotionBelongToType](#v2PromotionBelongToType) |  | No |
| id | string |  | No |

#### `v2PromotionBelongToType`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v2PromotionBelongToType | string |  |  |

#### `v2PromotionKind`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v2PromotionKind | string |  |  |

#### `v2PromotionMethod`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v2PromotionMethod | string |  |  |

#### `v2PromotionStatus`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v2PromotionStatus | string |  |  |

#### `v2PromotionType`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v2PromotionType | string |  |  |

#### `v2PublishCode`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| publish_time | dateTime |  | No |
| published_time | dateTime |  | No |
| methods | [ [v2PublishMethod](#v2PublishMethod) ] |  | No |
| content | string |  | No |
| agents | [ [masterdatav1Agent](#masterdatav1Agent) ] |  | No |
| destination_type | [v2PublishDestinationType](#v2PublishDestinationType) |  | No |
| code | [v2Code](#v2Code) |  | No |
| create_time | dateTime |  | No |
| update_time | dateTime |  | No |
| status | [PublishCodePublishStatus](#PublishCodePublishStatus) |  | No |
| title | string |  | No |

#### `v2PublishCodeBody`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| publish_time | dateTime |  | No |
| methods | [ [v2PublishMethod](#v2PublishMethod) ] |  | No |
| content | string |  | No |
| phones | [ string ] |  | No |
| destination_type | [v2PublishDestinationType](#v2PublishDestinationType) |  | No |
| code_id | string |  | No |
| title | string |  | No |

#### `v2PublishCodesRequest`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| publish_codes | [ [v2PublishCodeBody](#v2PublishCodeBody) ] |  | No |

#### `v2PublishCodesResponse`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| publish_codes | [ [v2PublishCode](#v2PublishCode) ] |  | No |

#### `v2PublishDestinationType`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v2PublishDestinationType | string |  |  |

#### `v2PublishMethod`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v2PublishMethod | string |  |  |

#### `v2ResourceAllocated`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| phone | string |  | No |
| code | string |  | No |
| promotion_id | string |  | No |
| allocated_time | dateTime |  | No |

#### `v2SearchCodesRequestCodeStatus`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v2SearchCodesRequestCodeStatus | string |  |  |

#### `v2SearchCodesRequestEqual`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| status | [v2SearchCodesRequestCodeStatus](#v2SearchCodesRequestCodeStatus) |  | No |
| number_of_use | integer |  | No |

#### `v2SearchCodesRequestLike`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| code | string |  | No |

#### `v2SearchCodesResponse`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| codes | [ [v2Code](#v2Code) ] |  | No |
| pagination | [v2SearchCodesResponsePagination](#v2SearchCodesResponsePagination) |  | No |

#### `v2SearchCodesResponsePagination`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| page_number | integer |  | No |
| page_size | integer |  | No |
| total_size | integer |  | No |