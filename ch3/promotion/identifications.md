# Identification
- [Identification](#identification)
  - [`Identification`](#identification-1)
    - [`Miêu tả `](#miêu-tả-)
    - [Struct data](#struct-data)
    - [`/v2/identification:phone/{phone}`](#v2identificationphonephone)
      - [`GET`](#get)
        - [`Parameters`](#parameters)
        - [`Responses`](#responses)
    - [`/v2/identifications`](#v2identifications)
      - [`POST`](#post)
        - [`Summary`:](#summary)
        - [`Parameters`](#parameters-1)
        - [`Responses`](#responses-1)
    - [`/v2/identifications:phone/{phone}`](#v2identificationsphonephone)
      - [`PUT`](#put)
        - [`Parameters`](#parameters-2)
        - [`Responses`](#responses-2)
    - [`/v2/identifications:searc`h](#v2identificationssearch)
      - [`GET`](#get-1)
        - [`Summary`:](#summary-1)
        - [`Parameters`](#parameters-3)
        - [`Responses`](#responses-3)
    - [`Models`](#models)
      - [`CodeSettingCodeType`](#codesettingcodetype)
      - [`CodeSettingTypeCode`](#codesettingtypecode)
      - [`ConditionUsageMaxTimesPerPerson`](#conditionusagemaxtimesperperson)
      - [`ConditionUsageMaxTimesPerPersonPerTime`](#conditionusagemaxtimesperpersonpertime)
      - [`ConditionUsageMaxTimesUsage`](#conditionusagemaxtimesusage)
      - [`ContentEvent`](#contentevent)
      - [`MaxTimesPerPersonPerTimeTimeType`](#maxtimesperpersonpertimetimetype)
      - [`SearchIdentificationsRequestGroup`](#searchidentificationsrequestgroup)
      - [`SearchIdentificationsResponseAgents`](#searchidentificationsresponseagents)
      - [`googlerpcStatus`](#googlerpcstatus)
      - [`promotionv2Agent`](#promotionv2agent)
      - [`promotionv2Identification`](#promotionv2identification)
      - [`promotionv2MaxTimes`](#promotionv2maxtimes)
      - [`protobufAny`](#protobufany)
      - [`v2CodeSetting`](#v2codesetting)
      - [`v2ConditionUsage`](#v2conditionusage)
      - [`v2Content`](#v2content)
      - [`v2CreateIdentificationsRequest`](#v2createidentificationsrequest)
      - [`v2CreateIdentificationsRequestIdentification`](#v2createidentificationsrequestidentification)
      - [`v2CreateIdentificationsResponse`](#v2createidentificationsresponse)
      - [`v2IdentificationsResponse`](#v2identificationsresponse)
      - [`v2Promotion`](#v2promotion)
      - [`v2PromotionBelongTo`](#v2promotionbelongto)
      - [`v2PromotionBelongToType`](#v2promotionbelongtotype)
      - [`v2PromotionKind`](#v2promotionkind)
      - [`v2PromotionMethod`](#v2promotionmethod)
      - [`v2PromotionStatus`](#v2promotionstatus)
      - [`v2PromotionType`](#v2promotiontype)
      - [`v2SearchIdentificationsRequestEqual`](#v2searchidentificationsrequestequal)
      - [`v2SearchIdentificationsResponse`](#v2searchidentificationsresponse)
      - [`v2SearchIdentificationsResponsePagination`](#v2searchidentificationsresponsepagination)
      - [`v2UpdateIdentification`](#v2updateidentification)
      - [`v2UpdateIdentificationResponse`](#v2updateidentificationresponse)

## `Identification`
### `Miêu tả `
  - entity này sử lý việc voucher code hoạt động như nào.
### Struct data
  | Name         | Type                        | Description |
  | ------------ | --------------------------- | ----------- |
  | id           | string                      |             |
  | phone        | string                      |             |
  | promotion_id | string                      |             |
  | start_time   | dateTime                    |             |
  | expire_time  | dateTime                    |             |
  | create_time  | dateTime                    |             |
  | update_time  | dateTime                    |             |
  | creator      | string                      |             |
  | promotion    | [v2Promotion](#v2Promotion) |             |
  | status       | string                      |             |

### `/v2/identification:phone/{phone}`

#### `GET`
##### `Parameters`

| Name  | Located in | Description | Required | Schema |
| ----- | ---------- | ----------- | -------- | ------ |
| phone | path       |             | Yes      | string |

##### `Responses`

| Code    | Description                   | Schema                                                  |
| ------- | ----------------------------- | ------------------------------------------------------- |
| 200     | A successful response.        | [v2IdentificationsResponse](#v2IdentificationsResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus)                     |

### `/v2/identifications`

#### `POST`
##### `Summary`:

Thêm danh sách sđt vô danh sách CTKM

##### `Parameters`

| Name | Located in | Description | Required | Schema                                                            |
| ---- | ---------- | ----------- | -------- | ----------------------------------------------------------------- |
| body | body       |             | Yes      | [v2CreateIdentificationsRequest](#v2CreateIdentificationsRequest) |

##### `Responses`

| Code    | Description                   | Schema                                                              |
| ------- | ----------------------------- | ------------------------------------------------------------------- |
| 200     | A successful response.        | [v2CreateIdentificationsResponse](#v2CreateIdentificationsResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus)                                 |

### `/v2/identifications:phone/{phone}`

#### `PUT`
##### `Parameters`

| Name  | Located in | Description | Required | Schema |
| ----- | ---------- | ----------- | -------- | ------ |
| phone | path       |             | Yes      | string |
| body  | body       |             | Yes      | object |

##### `Responses`

| Code    | Description                   | Schema                                                            |
| ------- | ----------------------------- | ----------------------------------------------------------------- |
| 200     | A successful response.        | [v2UpdateIdentificationResponse](#v2UpdateIdentificationResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus)                               |

### `/v2/identifications:searc`h

#### `GET`
##### `Summary`:

Cho phép người dùng tìm kiếm chương trình khuyến mãi định danh theo các điều kiện

##### `Parameters`

| Name               | Located in | Description | Required | Schema  |
| ------------------ | ---------- | ----------- | -------- | ------- |
| equal.phone        | query      |             | No       | string  |
| keywords           | query      |             | No       | string  |
| page_number        | query      |             | No       | integer |
| page_size          | query      |             | No       | integer |
| order_by           | query      |             | No       | string  |
| group.is_promotion | query      |             | No       | boolean |

##### `Responses`

| Code    | Description                   | Schema                                                              |
| ------- | ----------------------------- | ------------------------------------------------------------------- |
| 200     | A successful response.        | [v2SearchIdentificationsResponse](#v2SearchIdentificationsResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus)                                 |

### `Models`


#### `CodeSettingCodeType`

| Name                | Type   | Description | Required |
| ------------------- | ------ | ----------- | -------- |
| CodeSettingCodeType | string |             |          |

#### `CodeSettingTypeCode`

| Name                | Type   | Description | Required |
| ------------------- | ------ | ----------- | -------- |
| CodeSettingTypeCode | string |             |          |

#### `ConditionUsageMaxTimesPerPerson`

| Name     | Type    | Description | Required |
| -------- | ------- | ----------- | -------- |
| is_limit | boolean |             | No       |
| count    | integer |             | No       |

#### `ConditionUsageMaxTimesPerPersonPerTime`

| Name      | Type                                                                  | Description | Required |
| --------- | --------------------------------------------------------------------- | ----------- | -------- |
| is_limit  | boolean                                                               |             | No       |
| count     | integer                                                               |             | No       |
| time_type | [MaxTimesPerPersonPerTimeTimeType](#MaxTimesPerPersonPerTimeTimeType) |             | No       |

#### `ConditionUsageMaxTimesUsage`

| Name     | Type    | Description | Required |
| -------- | ------- | ----------- | -------- |
| is_limit | boolean |             | No       |
| count    | integer |             | No       |

#### `ContentEvent`

| Name   | Type   | Description | Required |
| ------ | ------ | ----------- | -------- |
| type   | string |             | No       |
| params | string |             | No       |

#### `MaxTimesPerPersonPerTimeTimeType`

| Name                             | Type   | Description | Required |
| -------------------------------- | ------ | ----------- | -------- |
| MaxTimesPerPersonPerTimeTimeType | string |             |          |

#### `SearchIdentificationsRequestGroup`

| Name         | Type    | Description | Required |
| ------------ | ------- | ----------- | -------- |
| is_promotion | boolean |             | No       |

#### `SearchIdentificationsResponseAgents`

| Name  | Type                                  | Description | Required |
| ----- | ------------------------------------- | ----------- | -------- |
| phone | string                                |             | No       |
| agent | [promotionv2Agent](#promotionv2Agent) |             | No       |

#### `googlerpcStatus`

| Name    | Type                            | Description | Required |
| ------- | ------------------------------- | ----------- | -------- |
| code    | integer                         |             | No       |
| message | string                          |             | No       |
| details | [ [protobufAny](#protobufAny) ] |             | No       |

#### `promotionv2Agent`

| Name             | Type       | Description | Required |
| ---------------- | ---------- | ----------- | -------- |
| id               | string     |             | No       |
| name             | string     |             | No       |
| phone            | string     |             | No       |
| status           | string     |             | No       |
| business_type_id | string     |             | No       |
| location_type_id | string     |             | No       |
| vendor_ids       | [ string ] |             | No       |
| district_id      | string     |             | No       |
| total_ordered    | integer    |             | No       |
| supplier_ids     | [ string ] |             | No       |

#### `promotionv2Identification`

| Name         | Type                        | Description | Required |
| ------------ | --------------------------- | ----------- | -------- |
| id           | string                      |             | No       |
| phone        | string                      |             | No       |
| promotion_id | string                      |             | No       |
| start_time   | dateTime                    |             | No       |
| expire_time  | dateTime                    |             | No       |
| create_time  | dateTime                    |             | No       |
| update_time  | dateTime                    |             | No       |
| creator      | string                      |             | No       |
| promotion    | [v2Promotion](#v2Promotion) |             | No       |
| status       | string                      |             | No       |

#### `promotionv2MaxTimes`

| Name     | Type    | Description | Required |
| -------- | ------- | ----------- | -------- |
| is_limit | boolean |             | No       |
| count    | integer |             | No       |

#### `protobufAny`

| Name     | Type   | Description | Required |
| -------- | ------ | ----------- | -------- |
| type_url | string |             | No       |
| value    | byte   |             | No       |

#### `v2CodeSetting`

| Name                 | Type                                        | Description | Required |
| -------------------- | ------------------------------------------- | ----------- | -------- |
| is_use_code          | boolean                                     |             | No       |
| code_type            | [CodeSettingCodeType](#CodeSettingCodeType) |             | No       |
| max_times_per_person | [promotionv2MaxTimes](#promotionv2MaxTimes) |             | No       |
| count                | integer                                     |             | No       |
| max_times_per_code   | [promotionv2MaxTimes](#promotionv2MaxTimes) |             | No       |
| type                 | [CodeSettingTypeCode](#CodeSettingTypeCode) |             | No       |
| prefix               | string                                      |             | No       |
| postfix              | string                                      |             | No       |
| code_length          | integer                                     |             | No       |

#### `v2ConditionUsage`

| Name                          | Type                                                                              | Description | Required |
| ----------------------------- | --------------------------------------------------------------------------------- | ----------- | -------- |
| max_times_usage               | [ConditionUsageMaxTimesUsage](#ConditionUsageMaxTimesUsage)                       |             | No       |
| max_times_per_person          | [ConditionUsageMaxTimesPerPerson](#ConditionUsageMaxTimesPerPerson)               |             | No       |
| max_times_per_person_per_time | [ConditionUsageMaxTimesPerPersonPerTime](#ConditionUsageMaxTimesPerPersonPerTime) |             | No       |

#### `v2Content`

| Name       | Type                          | Description | Required |
| ---------- | ----------------------------- | ----------- | -------- |
| id         | string                        |             | No       |
| conditions | string                        |             | No       |
| event      | [ContentEvent](#ContentEvent) |             | No       |

#### `v2CreateIdentificationsRequest`

| Name            | Type                                                                                              | Description | Required |
| --------------- | ------------------------------------------------------------------------------------------------- | ----------- | -------- |
| identifications | [ [v2CreateIdentificationsRequestIdentification](#v2CreateIdentificationsRequestIdentification) ] |             | No       |

#### `v2CreateIdentificationsRequestIdentification`

| Name         | Type     | Description | Required |
| ------------ | -------- | ----------- | -------- |
| phone        | string   |             | Yes      |
| promotion_id | string   |             | Yes      |
| start_time   | dateTime |             | Yes      |
| expire_time  | dateTime |             | Yes      |

#### `v2CreateIdentificationsResponse`

| Name            | Type                                                        | Description | Required |
| --------------- | ----------------------------------------------------------- | ----------- | -------- |
| identifications | [ [promotionv2Identification](#promotionv2Identification) ] |             | No       |

#### `v2IdentificationsResponse`

| Name            | Type                                                        | Description | Required |
| --------------- | ----------------------------------------------------------- | ----------- | -------- |
| phone           | string                                                      |             | No       |
| identifications | [ [promotionv2Identification](#promotionv2Identification) ] |             | No       |

#### `v2Promotion`

| Name            | Type                                        | Description | Required |
| --------------- | ------------------------------------------- | ----------- | -------- |
| id              | string                                      |             | No       |
| name            | string                                      |             | No       |
| start_time      | dateTime                                    |             | No       |
| expire_time     | dateTime                                    |             | No       |
| type            | [v2PromotionType](#v2PromotionType)         |             | No       |
| status          | [v2PromotionStatus](#v2PromotionStatus)     |             | No       |
| creator         | string                                      |             | No       |
| create_time     | dateTime                                    |             | No       |
| update_time     | dateTime                                    |             | No       |
| content         | string                                      |             | No       |
| description     | string                                      |             | No       |
| detail          | string                                      |             | No       |
| company_id      | string                                      |             | No       |
| vendor_name     | string                                      |             | No       |
| contents        | [ [v2Content](#v2Content) ]                 |             | No       |
| priority        | integer                                     |             | No       |
| method          | [v2PromotionMethod](#v2PromotionMethod)     |             | No       |
| condition_usage | [v2ConditionUsage](#v2ConditionUsage)       |             | No       |
| targets         | string                                      |             | No       |
| code_setting    | [v2CodeSetting](#v2CodeSetting)             |             | No       |
| belong_to       | [v2PromotionBelongTo](#v2PromotionBelongTo) |             | No       |
| channels        | [ string ]                                  |             | No       |
| kind            | [v2PromotionKind](#v2PromotionKind)         |             | No       |
| detail_name     | string                                      |             | No       |
| number_of_use   | integer                                     |             | No       |

#### `v2PromotionBelongTo`

| Name | Type                                                | Description | Required |
| ---- | --------------------------------------------------- | ----------- | -------- |
| name | string                                              |             | No       |
| type | [v2PromotionBelongToType](#v2PromotionBelongToType) |             | No       |
| id   | string                                              |             | No       |

#### `v2PromotionBelongToType`

| Name                    | Type   | Description | Required |
| ----------------------- | ------ | ----------- | -------- |
| v2PromotionBelongToType | string |             |          |

#### `v2PromotionKind`

| Name            | Type   | Description | Required |
| --------------- | ------ | ----------- | -------- |
| v2PromotionKind | string |             |          |

#### `v2PromotionMethod`

| Name              | Type   | Description | Required |
| ----------------- | ------ | ----------- | -------- |
| v2PromotionMethod | string |             |          |

#### `v2PromotionStatus`

| Name              | Type   | Description | Required |
| ----------------- | ------ | ----------- | -------- |
| v2PromotionStatus | string |             |          |

#### `v2PromotionType`

| Name            | Type   | Description | Required |
| --------------- | ------ | ----------- | -------- |
| v2PromotionType | string |             |          |

#### `v2SearchIdentificationsRequestEqual`

| Name  | Type   | Description | Required |
| ----- | ------ | ----------- | -------- |
| phone | string |             | No       |

#### `v2SearchIdentificationsResponse`

| Name            | Type                                                                                    | Description | Required |
| --------------- | --------------------------------------------------------------------------------------- | ----------- | -------- |
| identifications | [ [SearchIdentificationsResponseAgents](#SearchIdentificationsResponseAgents) ]         |             | No       |
| pagination      | [v2SearchIdentificationsResponsePagination](#v2SearchIdentificationsResponsePagination) |             | No       |

#### `v2SearchIdentificationsResponsePagination`

| Name        | Type    | Description | Required |
| ----------- | ------- | ----------- | -------- |
| page_number | integer |             | No       |
| page_size   | integer |             | No       |
| total_size  | integer |             | No       |

#### `v2UpdateIdentification`

| Name              | Type     | Description | Required |
| ----------------- | -------- | ----------- | -------- |
| identification_id | string   |             | Yes      |
| start_time        | dateTime |             | No       |
| expire_time       | dateTime |             | No       |

#### `v2UpdateIdentificationResponse`

| Name            | Type                                                  | Description | Required |
| --------------- | ----------------------------------------------------- | ----------- | -------- |
| identifications | [ [v2UpdateIdentification](#v2UpdateIdentification) ] |             | No       |